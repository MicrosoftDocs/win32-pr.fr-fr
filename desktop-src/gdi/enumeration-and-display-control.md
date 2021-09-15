---
description: Pour énumérer tous les périphériques de l’ordinateur, appelez la fonction EnumDisplayDevices. Les informations retournées indiquent également quelle analyse fait partie du bureau.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Énumération et contrôle d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127531344"
---
# <a name="enumeration-and-display-control"></a>Énumération et contrôle d’affichage

Pour énumérer tous les périphériques de l’ordinateur, appelez la fonction [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) . Les informations retournées indiquent également quelle analyse fait partie du bureau.

Pour énumérer les périphériques sur le bureau qui croisent une zone de découpage, appelez [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors). Cela retourne le descripteur HMONITOR à chaque analyse, qui est utilisé avec [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa). Pour énumérer tous les appareils de l’écran virtuel, utilisez **EnumDisplayMonitors**. comme indiqué dans le code suivant :


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



Pour obtenir des informations sur un périphérique d’affichage, utilisez [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) ou [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).

La fonction [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) est utilisée pour contrôler les périphériques d’affichage sur l’ordinateur. Il peut modifier la configuration des appareils, tels que la spécification de la position d’une analyse sur le bureau virtuel et la modification de la profondeur de bit de n’importe quel affichage. En règle générale, une application n’utilise pas cette fonction. Pour ajouter par programme un moniteur d’affichage à un système à plusieurs écrans, définissez **DEVMODE. dmFields** sur \_ position DM et spécifiez une position (à l’aide de **DEVMODE. dmPosition** ) pour l’analyse que vous ajoutez qui est adjacente à au moins un pixel de la zone d’affichage d’une analyse existante. Pour détacher le moniteur, définissez **DEVMODE. dmFields** sur \_ position DM et définissez **DEVMODE. DmPelsWidth** et **DEVMODE. dmPelsHeight** sur zéro.

Le code suivant montre comment détacher tous les périphériques d’affichage secondaires du Bureau :


```
void DetachDisplay()
{
    BOOL            FoundSecondaryDisp = FALSE;
    DWORD           DispNum = 0;
    DISPLAY_DEVICE  DisplayDevice;
    LONG            Result;
    TCHAR           szTemp[200];
    int             i = 0;
    DEVMODE   defaultMode;

    // initialize DisplayDevice
    ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
    DisplayDevice.cb = sizeof(DisplayDevice);

    // get all display devices
    while (EnumDisplayDevices(NULL, DispNum, &DisplayDevice, 0))
        {
        ZeroMemory(&defaultMode, sizeof(DEVMODE));
        defaultMode.dmSize = sizeof(DEVMODE);
        if ( !EnumDisplaySettings((LPSTR)DisplayDevice.DeviceName, ENUM_REGISTRY_SETTINGS, &defaultMode) )
                  OutputDebugString("Store default failed\n");

        if ((DisplayDevice.StateFlags & DISPLAY_DEVICE_ATTACHED_TO_DESKTOP) &&
            !(DisplayDevice.StateFlags & DISPLAY_DEVICE_PRIMARY_DEVICE))
            {
            DEVMODE    DevMode;
            ZeroMemory(&DevMode, sizeof(DevMode));
            DevMode.dmSize = sizeof(DevMode);
            DevMode.dmFields = DM_PELSWIDTH | DM_PELSHEIGHT | DM_BITSPERPEL | DM_POSITION
                        | DM_DISPLAYFREQUENCY | DM_DISPLAYFLAGS ;
            Result = ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName, 
                                            &DevMode,
                                            NULL,
                                            CDS_UPDATEREGISTRY,
                                            NULL);

            //The code below shows how to re-attach the secondary displays to the desktop

            //ChangeDisplaySettingsEx((LPSTR)DisplayDevice.DeviceName,
            //                       &defaultMode,
            //                       NULL,
            //                       CDS_UPDATEREGISTRY,
            //                       NULL);

            }

        // Reinit DisplayDevice just to be extra clean

        ZeroMemory(&DisplayDevice, sizeof(DisplayDevice));
        DisplayDevice.cb = sizeof(DisplayDevice);
        DispNum++;
        } // end while for all display devices
}
```



Pour chaque périphérique d’affichage, l’application peut enregistrer des informations dans le Registre qui décrivent les paramètres de configuration de l’appareil, ainsi que des paramètres d’emplacement. L’application peut également déterminer les affichages qui font partie du bureau, et ceux qui ne le sont pas, par le biais du périphérique d’affichage \_ \_ attaché \_ à l’indicateur de \_ Bureau dans la structure du [**\_ périphérique d’affichage**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) . Une fois que toutes les informations de configuration sont stockées dans le registre, l’application peut appeler de nouveau [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) pour modifier dynamiquement les paramètres, sans redémarrage nécessaire.

 

 



