# NAME

WebService::GialloZafferano - Perl interface to GialloZafferano.it website to find cooking recipes

# SYNOPSIS

```perl
use WebService::GialloZafferano;
my $Cook = WebService::GialloZafferano->new();
my @recipes = $Cook->search("Spaghetti"); # It returns a list of WebService::GialloZafferano::Recipe 
my $spaghetti_recipe= $recipes[0]->text; #i wanna knew more about that recipe
my @Ingredients = $recipes[0]->ingredients(); # i'm not happy, wanna know the ingredients of the next one 
# @Ingredients is a list of WebService::GialloZafferano::Ingredient
```

# DESCRIPTION

WebService::GialloZafferano is a Perl interface to the site GialloZafferano.it, it allows to query the cooking recipes and get the ingredients

# METHODS

## search()

Takes input terms and process the GialloZafferano.it research.
It returns a list of WebService::GialloZafferano::Recipe.

returns undef on error

#ATTRIBUTES

## ua

Returns the Mojo::UserAgent instance

# AUTHOR

mudler <mudler@dark-lab.net>

# COPYRIGHT

Copyright 2014- mudler

# LICENSE

This library is free software; you can redistribute it and/or modify
it under the same terms as Perl itself.
