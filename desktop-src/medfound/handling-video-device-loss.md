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
# <a name="handling-video-device-loss"></a>Gestion de la perte de l’appareil vidéo

Cette rubrique explique comment détecter la perte d’appareil lors de l’utilisation d’un périphérique de capture vidéo. Il contient les sections suivantes :

-   [S’inscrire pour la notification de l’appareil](#register-for-device-notification)
-   [Obtient le lien symbolique de l’appareil](#get-the-symbolic-link-of-the-device)
-   [Gérer WM \_ DEVICECHANGE](/windows)
-   [Annuler l’inscription pour la notification](#unregister-for-notification)
-   [Rubriques connexes](#related-topics)

## <a name="register-for-device-notification"></a>S’inscrire pour la notification de l’appareil

Avant de commencer la capture à partir de l’appareil, appelez la fonction [**RegisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-registerdevicenotificationa) pour vous inscrire aux notifications de l’appareil. Inscrivez-vous à la classe **KSCATEGORY \_ capture** Device, comme indiqué dans le code suivant.


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



## <a name="get-the-symbolic-link-of-the-device"></a>Obtient le lien symbolique de l’appareil

Énumérez les périphériques vidéo du système, comme décrit dans [énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md). Choisissez un appareil dans la liste, puis interrogez l’objet d’activation pour l’attribut de [ \_ \_ \_ \_ \_ \_ \_ liaison symbolique VIDCAP du type de source de l’attribut MF DEVSOURCE](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) , comme indiqué dans le code suivant.


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



## <a name="handle-wm_devicechange"></a>Gérer WM \_ DEVICECHANGE

Dans votre boucle de message, écoutez les messages [**WM \_ DEVICECHANGE**](../devio/wm-devicechange.md) . Le paramètre de message *lParam* est un pointeur vers une structure [**\_ \_ HDR de diffusion dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) .


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



Ensuite, comparez le message de notification de l’appareil au lien symbolique de votre appareil, comme suit :

1.  Vérifiez le membre **dbch \_ DeviceType** de la structure [**\_ \_ HDR de diffusion dev**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_hdr) . Si la valeur est **DBT \_ DEVTYP \_ DEVICEINTERFACE**, effectuez un cast du pointeur de structure en une structure de [**\_ \_ DEVICEINTERFACE de diffusion de développement**](/windows/win32/api/dbt/ns-dbt-dev_broadcast_deviceinterface_a) .
2.  Comparez le membre de **\_ nom DBCC** de cette structure au lien symbolique de l’appareil.


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



## <a name="unregister-for-notification"></a>Annuler l’inscription pour la notification

Avant de quitter l’application, appelez [**UnregisterDeviceNotification**](/windows/win32/api/winuser/nf-winuser-unregisterdevicenotification) pour annuler l’inscription des notifications de l’appareil/


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



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Énumération des périphériques de capture vidéo](enumerating-video-capture-devices.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> </dl>

 

 
