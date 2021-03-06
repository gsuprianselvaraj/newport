// Copyright (c) 2015-present, salesforce.com, inc. All rights reserved
// Licensed under BSD 3-Clause - see LICENSE.txt or git.io/sfdc-license

/**
A prompt uses the base modal component and then adds the class `.nds-modal_prompt` to the overall `.nds-modal`. The utilities > themes > colors class is placed on the `.nds-modal__head` to create the color of the header. In the example, we illustrate using `.nds-theme_error`. The class `.nds-theme_alert-texture` should be applied to create the striped gradient. The `.nds-modal__footer` receives the class `.nds-theme_default`.

## Accessibility

Prompt notifications are similar to modals, in that they are a focus trap, but they should take a slightly different `role` of `alertdialog` to indicate their severity. Like modals they should be labelled by their headings, but additonally they should be desscribed by the message details of the prompt.

The element containing the prompt message should be the target focus of the browser when it is displayed, which is why we add `tab-index="0"` to `nds-modal__container`.

There is no requirement for a close button, as the confirmation button should be used to dismiss the prompt, along with the usual Esc key dismissal.

**Expected markup (same as Modals, but with the following differences):**
- Modal has `role="alertdialog"`
- Modal has an `aria-describedby` attribute that matches the id of the modal message container.
- Modal message container container should have `tab-index="0"`

**Expected keyboard interaction (sme as Modal, with the addition of):**
- Modal message container should take initial focus

@summary Prompt notice grabs the user’s attention & alert them of system-related issues/updates.

@base
@name prompt
@selector .nds-modal_prompt
@support dev-ready
@category experience
@type messaging
@role alert
/
