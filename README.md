# Module Process Settings

This module is a generic template for the business pattern where we need to associate to a record a set of configuration options for additional work that needs to be done. The typical example is the commission rules that need to be applied to an invoice. Depending on the type of invoice and the people who participate in the sale we can have different commission settings, so we define a module where we save all the different commission distributions that we can have and then relate the correct record with each invoice when it is created. Then a post process can read these settings and setup the necessary records for payments and accounting.

So this would be a module where we could define any combination of settings that any invoice may need. This idea can be extended to any other module, like Potentials where we could define different patterns of calling and following up each business opportunity based on any conditions we may require.

Defined in this way the business pattern doesn't sound very exicting. You can already do this in many ways inside coreBOS. You can use workflows, custom functions, hooks, business actions, ...

This pattern brings a few additional features with it that could make it an interesting option in some cases, albeit I have to admit that I don't quite see it, but I'm not UI/UX oriented at all :-)

This module has some fields that must be present with the exact names they are defined with in this template. These fields:

- the module the settings are for
- the field filter map that can be applied
- the field dependency map that can be applied
- the validation map that can be applied
- an active checkbox to mark the settings are active or not

and that is where the extra functionality of this pattern appears. coreBOS is capable of finding the correct setting record to apply on each main record, either directly from a field dependency map or through a business rule and then automatically reload the screen applying the defined maps to make the user experience more adapted to each type of record.

In the video you can see below I try to explain what this may look like.
