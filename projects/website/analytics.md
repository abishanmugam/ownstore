---
label: Analytics
title: Website Analytics
icon: graph
order: 0
---

## Google Analytics

GA is added as part of an integration but can be disabled. E-Commerce events have also been added for advanced analytics.

The following events have been added:

```ts
LOGIN = 'login',
LOGOUT = 'logout',
SIGNUP = 'sign_up',
SEARCH = 'search',
VIEW_SEARCH_RESULTS = 'view_search_results',
SHARE = 'share',
VIEW_CART = 'view_cart',
ADD_TO_CART = 'add_to_cart',
REMOVE_FROM_CART = 'remove_from_cart',
DELETE_CART_ITEM = 'delete_cart_item',
ADD_TO_WISHLIST = 'add_to_wishlist',
REMOVE_FROM_WISHLIST = 'remove_from_wishlist',
MOVE_TO_CART = 'move_to_cart',
BEGIN_CHECKOUT = 'begin_checkout',
PURCHASE = 'purchase',
FAILED_PAYMENT = 'failed_payment',
ADD_ADDRESS = 'add_address',
EDIT_ADDRESS = 'edit_address',
DEACTIVATE_ADDRESS = 'deactivate_address',
SELECT_ADDRESS_FOR_DELIVERY = 'select_address_for_delivery',
SELECT_PRODUCT = 'select_content',
VIEW_PRODUCT = 'view_item',
PWA_INSTALL_SUCCESS = 'pwa_install_success',
PWA_INSTALL_FAILED = 'pwa_install_failed',
EXCEPTION = 'exception',
CHANGE_PASSWORD = 'change_password',
UPDATE_PASSWORD_HINT = 'update_password_hint',
UPDATE_SECURITY_QUESTIONS = 'update_security_questions',
ANSWER_SECURITY_QUESTIONS = 'answer_security_questions',
RESET_PASSWORD = 'reset_password',
EDIT_PROFILE = 'edit_profile',
SCROLL_TO_TOP = 'scroll_to_top',
```

Can be found in `app/constants/analytics.ts`.
