---
Order: 50
xref: ccm-faq
Title: FAQs
---

## Timezone FAQs

### Why Doesn't Chocolatey Central Management Have My Timezone?

Chocolatey Central Management uses the Windows install of its host to determine if a timezone is valid. If Windows does not know of a timezone, then it will not be made available.

Some examples of timezones that may not appear:

* `Qyzylorda Standard Time` does not appear in Windows Server 2016 until you install Windows Update [5031362](https://support.microsoft.com/en-us/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c) or later.
* `Yukon Standard Time` does not appear in Windows Server 2016 until you install Windows Update [5031362](https://support.microsoft.com/en-us/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c) or later.
* `South Sudan Standard Time` does not appear in Windows Server 2016 until you install [5031362](https://support.microsoft.com/en-us/topic/october-10-2023-kb5031362-os-build-14393-6351-0c6e713e-3d6a-4593-8a75-af0a605f249c) or later.

### Why Did I Get a Notification That My Chosen Timezone is Invalid?

Starting in Chocolatey Central Management version 0.12.0, if the chosen timezone is detected to be invalid, we will set it back to the default timezone and alert you through a notification. If you are an Administrator, you may additionally receive a notification that the system timezone was invalid.

#### User Account Timezone is Invalid

If you received the below notification, then it means that the timezone used for your user account was invalid, and has been set back to the default system timezone. You can pick your own default by clicking the user menu in the top right and selecting `My Settings`.


![Example notification for a user configured timezone being invalid](/assets/images/ccm/administration/settings/user-timezone-invalid-notification.png)


#### System Timezone is Invalid

If you received the below notification, then it means that the system timezone was invalid, and has been set back to the default of `UTC`. You can adjust the default through the [Settings page](xref:ccm-administration-settings-general).

![Example notification for a Chocolatey Central Management configured timezone being invalid](/assets/images/ccm/administration/settings/ccm-timezone-invalid-notification.png)
