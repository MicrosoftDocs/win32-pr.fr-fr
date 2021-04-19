---
description: Cette rubrique explique comment détecter la perte d’appareil lors de l’utilisation d’un périphérique de capture vidéo.
ms.assetid: 2bffe156-c507-437e-8f32-62aaebedd6f0
title: Gestion de la perte de l’appareil vidéo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0d083ebeb1203b0bba49a63745f62a4dff6b231
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527202"
---
# <a name="handling-video-device-loss"></a><span data-ttu-id="75acf-103">Gestion de la perte de l’appareil vidéo</span><span class="sxs-lookup"><span data-stu-id="75acf-103">Handling Video Device Loss</span></span>

<span data-ttu-id="75acf-104">Cette rubrique explique comment détecter la perte d’appareil lors de l’utilisation d’un périphérique de capture vidéo.</span><span class="sxs-lookup"><span data-stu-id="75acf-104">This topic describes how to detect device loss when using a video capture device.</span></span> <span data-ttu-id="75acf-105">Il contient les sections suivantes :</span><span class="sxs-lookup"><span data-stu-id="75acf-105">It contains the following sections:</span></span>

-   [<span data-ttu-id="75acf-106">S’inscrire pour la notification de l’appareil</span><span class="sxs-lookup"><span data-stu-id="75acf-106">Register For Device Notification</span></span>](#register-for-device-notification)
-   [<span data-ttu-id="75acf-107">Obtient le lien symbolique de l’appareil</span><span class="sxs-lookup"><span data-stu-id="75acf-107">Get the Symbolic Link of the Device</span></span>](#get-the-symbolic-link-of-the-device)
-   [<span data-ttu-id="75acf-108">Gérer WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="75acf-108">Handle WM\_DEVICECHANGE</span></span>](/windows)
-   [<span data-ttu-id="75acf-109">Annuler l’inscription pour la notification</span><span class="sxs-lookup"><span data-stu-id="75acf-109">Unregister For Notification</span></span>](#unregister-for-notification)
-   [<span data-ttu-id="75acf-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75acf-110">Related topics</span></span>](#related-topics)

## <a name="register-for-device-notification"></a><span data-ttu-id="75acf-111">S’inscrire pour la notification de l’appareil</span><span class="sxs-lookup"><span data-stu-id="75acf-111">Register For Device Notification</span></span>

<span data-ttu-id="75acf-112">Avant de commencer la capture à partir de l’appareil, appelez la fonction [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) pour vous inscrire aux notifications de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75acf-112">Before you start capturing from the device, call the [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) function to register for device notifications.</span></span> <span data-ttu-id="75acf-113">Inscrivez-vous à la classe **KSCATEGORY \_ capture** Device, comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="75acf-113">Register for the **KSCATEGORY\_CAPTURE** device class, as shown in the following code.</span></span>


```C++
#include <Dbt.h>
#include <ks.h>
#include <ksmedia.h>

HDEVNOTIFY  g_hdevnotify = NULL;

BOOL RegisterForDeviceNotification(HWND hwnd)
{
    DEV_BROADCAST_DEVICEINTERFACE di = { 0 };
    di.dbcc_size = sizeof(di);
    di.dbcc_devicetype  = DBT_DEVTYP_DEVICEINTERFACE;
    di.dbcc_classguid  = KSCATEGORY_CAPTURE; 

    g_hdevnotify = RegisterDeviceNotification(
        hwnd,
        &di,
        DEVICE_NOTIFY_WINDOW_HANDLE
        );

    if (g_hdevnotify == NULL)
    {
        return FALSE;
    }

    return TRUE;
}
```



## <a name="get-the-symbolic-link-of-the-device"></a><span data-ttu-id="75acf-114">Obtient le lien symbolique de l’appareil</span><span class="sxs-lookup"><span data-stu-id="75acf-114">Get the Symbolic Link of the Device</span></span>

<span data-ttu-id="75acf-115">Énumérez les périphériques vidéo du système, comme décrit dans [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="75acf-115">Enumerate the video devices on the system, as described in [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span> <span data-ttu-id="75acf-116">Choisissez un appareil dans la liste, puis interrogez l’objet d’activation pour l’attribut de [ \_ \_ \_ \_ \_ \_ \_ liaison symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , comme indiqué dans le code suivant.</span><span class="sxs-lookup"><span data-stu-id="75acf-116">Choose a device from the list, and then query the activation object for the [MF\_DEVSOURCE\_ATTRIBUTE\_SOURCE\_TYPE\_VIDCAP\_SYMBOLIC\_LINK](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) attribute, as shown in the following code.</span></span>


```C++
WCHAR      *g_pwszSymbolicLink = NULL;
UINT32     g_cchSymbolicLink = 0;

HRESULT GetSymbolicLink(IMFActivate *pActivate)
{
    return pActivate->GetAllocatedString(
        MF_DEVSOURCE_ATTRIBUTE_SOURCE_TYPE_VIDCAP_SYMBOLIC_LINK,
        &g_pwszSymbolicLink,
        &g_cchSymbolicLink
        );
}
```



## <a name="handle-wm_devicechange"></a><span data-ttu-id="75acf-117">Gérer WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="75acf-117">Handle WM\_DEVICECHANGE</span></span>

<span data-ttu-id="75acf-118">Dans votre boucle de message, écoutez les messages [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) .</span><span class="sxs-lookup"><span data-stu-id="75acf-118">In your message loop, listen for [**WM\_DEVICECHANGE**](../devio/wm-devicechange.md) messages.</span></span> <span data-ttu-id="75acf-119">Le paramètre de message *lParam* est un pointeur vers une structure [**\_ \_ HDR de diffusion dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="75acf-119">The *lParam* message parameter is a pointer to a [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span>


```C++
    case WM_DEVICECHANGE:
        if (lParam != 0)
        {
            HRESULT hr = S_OK;
            BOOL bDeviceLost = FALSE;

            hr = CheckDeviceLost((PDEV_BROADCAST_HDR)lParam, &bDeviceLost);

            if (FAILED(hr) || bDeviceLost)
            {
                CloseDevice();

                MessageBox(hwnd, L"Lost the capture device.", NULL, MB_OK);
            }
        }
        return TRUE;
```



<span data-ttu-id="75acf-120">Ensuite, comparez le message de notification de l’appareil au lien symbolique de votre appareil, comme suit :</span><span class="sxs-lookup"><span data-stu-id="75acf-120">Next, compare the device notification message against the symbolic link of your device, as follows:</span></span>

1.  <span data-ttu-id="75acf-121">Vérifiez le membre **dbch \_ DeviceType** de la structure [**\_ \_ HDR de diffusion dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .</span><span class="sxs-lookup"><span data-stu-id="75acf-121">Check the **dbch\_devicetype** member of the [**DEV\_BROADCAST\_HDR**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) structure.</span></span> <span data-ttu-id="75acf-122">Si la valeur est **DBT \_ DEVTYP \_ DEVICEINTERFACE**, effectuez un cast du pointeur de structure en une structure de [**\_ \_ DEVICEINTERFACE de diffusion de développement**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .</span><span class="sxs-lookup"><span data-stu-id="75acf-122">If the value is **DBT\_DEVTYP\_DEVICEINTERFACE**, cast the structure pointer to a [**DEV\_BROADCAST\_DEVICEINTERFACE**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) structure.</span></span>
2.  <span data-ttu-id="75acf-123">Comparez le membre de **\_ nom DBCC** de cette structure au lien symbolique de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="75acf-123">Compare the **dbcc\_name** member of this structure to the symbolic link of the device.</span></span>


```C++
HRESULT CheckDeviceLost(DEV_BROADCAST_HDR *pHdr, BOOL *pbDeviceLost)
{
    DEV_BROADCAST_DEVICEINTERFACE *pDi = NULL;

    if (pbDeviceLost == NULL)
    {
        return E_POINTER;
    }

    *pbDeviceLost = FALSE;
    
    if (g_pSource == NULL)
    {
        return S_OK;
    }
    if (pHdr == NULL)
    {
        return S_OK;
    }
    if (pHdr->dbch_devicetype != DBT_DEVTYP_DEVICEINTERFACE)
    {
        return S_OK;
    }

    // Compare the device name with the symbolic link.

    pDi = (DEV_BROADCAST_DEVICEINTERFACE*)pHdr;

    if (g_pwszSymbolicLink)
    {
        if (_wcsicmp(g_pwszSymbolicLink, pDi->dbcc_name) == 0)
        {
            *pbDeviceLost = TRUE;
        }
    }

    return S_OK;
}
```



## <a name="unregister-for-notification"></a><span data-ttu-id="75acf-124">Annuler l’inscription pour la notification</span><span class="sxs-lookup"><span data-stu-id="75acf-124">Unregister For Notification</span></span>

<span data-ttu-id="75acf-125">Avant de quitter l’application, appelez [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) pour annuler l’inscription des notifications de l’appareil/</span><span class="sxs-lookup"><span data-stu-id="75acf-125">Before the application exits, call [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) to unregister for device notifications/</span></span>


```C++
void OnClose(HWND /*hwnd*/)
{
    if (g_hdevnotify)
    {
        UnregisterDeviceNotification(g_hdevnotify);
    }

    PostQuitMessage(0);
}
```



## <a name="related-topics"></a><span data-ttu-id="75acf-126">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75acf-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="75acf-127">Énumération des périphériques de capture vidéo</span><span class="sxs-lookup"><span data-stu-id="75acf-127">Enumerating Video Capture Devices</span></span>](enumerating-video-capture-devices.md)
</dt> <dt>

[<span data-ttu-id="75acf-128">Capture vidéo</span><span class="sxs-lookup"><span data-stu-id="75acf-128">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 
