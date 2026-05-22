# UrbanEase Multi-Product Admin Guide

## Live product

Mini Projector - Basic
PayPal link:
https://www.paypal.com/ncp/payment/KXY58L7QKEFU2

## Google Form

https://docs.google.com/forms/d/e/1FAIpQLSdwrCcalI5Bu1o_-EzkTglRPx7d62i7YNWFizYzhPmZItX-aw/viewform?usp=publish-editor

## Products staged

The other products are listed in `products.js`. They are not live until you create PayPal payment links for them.

## How to make a product live

1. Go to PayPal payment links/buttons.
2. Create product link:
   - Product name exactly as in `products.js`
   - USD price exactly as in `products.js`
   - Quantity maximum: 10
   - Shipping address: ON
   - Customer note: Delivery instructions or WhatsApp number
3. Copy the PayPal link.
4. Open `products.js`.
5. Replace the relevant placeholder:
   - PAYPAL_MOTION_LIGHT_LINK_HERE
   - PAYPAL_LAPTOP_STAND_LINK_HERE
   - PAYPAL_CABLE_ORGANIZER_LINK_HERE
   - PAYPAL_CAR_HOLDER_LINK_HERE
   - PAYPAL_PET_GLOVE_LINK_HERE
6. Commit/upload the updated file to GitHub.

## Profit formula

If you mean 50% markup:
Selling price = supplier landed cost × 1.5

If you mean true 50% gross margin:
Selling price = supplier landed cost ÷ 0.5

The second formula is safer because PayPal fees, refunds, and ads reduce profit.

## Supplier links

Supplier links are inside `products.js` under the `supplier` field. They are not displayed to customers.

## Fulfillment flow

1. Customer pays through PayPal.
2. Customer submits delivery details form.
3. Google Sheet receives order.
4. You verify PayPal payment.
5. You order from supplier using customer address.
6. You update tracking and notify customer.

## Automation route

Static website cannot fully auto-purchase from AliExpress by itself.
For stronger automation:
- Use DSers free plan first
- Map products to AliExpress suppliers
- Use bulk order when orders arrive
- Upgrade only after sales are proven
