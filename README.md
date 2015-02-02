# Grunt Shopify Transactional Emails
Prebuilt template workflow for generating styled HTML emails for all of Shopify's transactional emails. 

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

default.hbs is the layout that comes with the original worflow. branded.hbs is slightly different. Here we've moved the header and the footer outside of the individual email templates so you only need to edit the layout once. This allowed us to focus specifically on each email's content in the individual templates.

## How it Works

If you haven't used [Grunt](http://gruntjs.com/) before check out Chris Coyier's post on [getting started with Grunt](http://24ways.org/2013/grunt-is-not-weird-and-hard/).

Make sure you've read the [grunt-email-design](https://github.com/leemunroe/grunt-email-design) getting started guide. This will teach you the Grunt workflow used here.

Once you're familiar with the workflow, you can use these templates (the src folder) to generate all your Shopify Transactional emails easily.

### Resources

These templates were based off of Mailgun's Transactional Email Templates, and the content pulled from the default Shopify Transactional Emails

1. [Shopify Email Variable Reference](http://docs.shopify.com/manual/settings/notifications/email-variables)
2. [Mailgun's Transactional Email Templates](http://blog.mailgun.com/transactional-html-email-templates/)
