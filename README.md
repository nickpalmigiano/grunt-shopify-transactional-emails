# Grunt Shopify Transactional Emails
Grunt workflow for generating Shopify transactional emails.

This repo was forked from [leemunroe/grunt-email-design](https://github.com/leemunroe/grunt-email-design)

The layouts and emails have been updated to include all the standard Shopify HTML transactional emails.

## Included Emails

1. Abandoned Checkout Notification
2. Customer Account Activation
3. Customer Account Welcome
4. Customer Password Reset
5. Fulfillment Request
6. GiftCard Notifications
7. New Order Notification
8. Order Cancelled
9. Order Confirmation
10. Refund Notification
11. Shipping Confirmation
12. Shipping Update

These two templates were not included since they are always sent in plaintext.

1. Contact Buyer
2. New Order Notification (mobile)

## Included Layouts

1. default.hbs
2. branded.hbs

default.hbs is the layout that comes with the original workflow. branded.hbs is slightly different. Here we've moved the header and the footer outside of the individual email templates so you only need to edit the layout once. This allowed us to focus specifically on each email's content in the individual templates.

## How it Works

Familiarize yourself with [Grunt](http://gruntjs.com/) before you get started. You can read Chris Coyier's post on [getting started with Grunt](http://24ways.org/2013/grunt-is-not-weird-and-hard/).

Make sure you've read the [grunt-email-design](https://github.com/leemunroe/grunt-email-design) getting started guide. This will teach you the Grunt workflow used here.

Once you're familiar with the workflow, you can use these templates (`/src`) to generate all your Shopify Transactional emails easily.


## Escaping Liquid Variables

Since both Assemble and Shopify's liquid variables use double brackets for variable declaration we have to escape the liquid variables before we assemble the emails. You'll see that we can do this by prefixing each variable with a backslash. ex: `\{{ shop.name }}`


## Notes

If you get this when running your workflow:

```
warning: possible EventEmitter memory leak detected. 11 listeners added. Use emitter.setMaxListeners() to increase limit.
```

Your templates will still render, however the watch task might not work exactly as expected. This is a node limit set to warn against possible recursion and infinite loops. However since we have more than 10 templates we're working with, this error often gets thrown. [You can checkout this fix in premailer](https://github.com/dwightjack/grunt-premailer/blob/master/tasks/premailer.js#L95).


### Resources

These templates were based off of Mailgun's Transactional Email Templates, and the content pulled from the default Shopify Transactional Emails

1. [Shopify Email Variable Reference](http://docs.shopify.com/manual/settings/notifications/email-variables)
2. [Mailgun's Transactional Email Templates](http://blog.mailgun.com/transactional-html-email-templates/)
