# Accessibility Priority

Each accessibility issue requires a priority to assist with determining the most important issues to fix.

To assess priority, it is important to consider the location of the issue, the user impact of the issue, and the frequency of the issue.

For example, a single image without an image description that is adjacent to related text but attached to a product listing is a P3 priority. In comparison, a page where all images are missing desciptions attached to product listings is P1 priority.

## Priority Levels

1. P1: the issue completely blocks a user from completing an essential or critical action.
2. P2: the issue blocks a user from completing an essential or critical action, or the issue has no possible workaround.
3. P3: the issue makes completing important actions difficult for the user, there may be a workaround for the issue.
4. P4: the issue makes completing actions frustrating for the user, there are often workarounds for the issue or the action is not essential.

### User Actions

The following are considered essential or critical user actions or flows for the product:

- Signing in or out
- Creating a new account
- Searching for items
- Viewing item details
- Adding items to cart
- Checking out
- Viewing purchase details and shipping confirmation
- Adding or editing payment information
- Adding or editing shipping information

## Examples

1. P1: The user is unable to sign in due to unlabelled email and password fields.
2. P4: The social media links in the footer are missing "opens in a new tab" labels.
3. P2: The "add to cart" button is a `<div>` with no click handler, preventing keyboard users from activating it.
4. P3: The `aria-label` for the "add to wishlist" button is not translated in France, Germany, and Italy.
