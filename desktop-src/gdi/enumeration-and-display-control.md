---
description: Pour énumérer tous les périphériques de l’ordinateur, appelez la fonction EnumDisplayDevices. Les informations retournées indiquent également quelle analyse fait partie du bureau.
ms.assetid: 834dee04-66fa-42eb-adff-c08a74c6cea8
title: Énumération et contrôle d’affichage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8cdfd5e3b1c6ebb5ff0d4ebdfa1ab44b45c2c25
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034223"
---
# <a name="enumeration-and-display-control"></a><span data-ttu-id="64b57-104">Énumération et contrôle d’affichage</span><span class="sxs-lookup"><span data-stu-id="64b57-104">Enumeration and Display Control</span></span>

<span data-ttu-id="64b57-105">Pour énumérer tous les périphériques de l’ordinateur, appelez la fonction [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) .</span><span class="sxs-lookup"><span data-stu-id="64b57-105">To enumerate all the devices on the computer, call the [**EnumDisplayDevices**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaydevicesa) function.</span></span> <span data-ttu-id="64b57-106">Les informations retournées indiquent également quelle analyse fait partie du bureau.</span><span class="sxs-lookup"><span data-stu-id="64b57-106">The information that is returned also indicates which monitor is part of the desktop.</span></span>

<span data-ttu-id="64b57-107">Pour énumérer les périphériques sur le bureau qui croisent une zone de découpage, appelez [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span><span class="sxs-lookup"><span data-stu-id="64b57-107">To enumerate the devices on the desktop that intersect a clipping region, call [**EnumDisplayMonitors**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaymonitors).</span></span> <span data-ttu-id="64b57-108">Cela retourne le descripteur HMONITOR à chaque analyse, qui est utilisé avec [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span><span class="sxs-lookup"><span data-stu-id="64b57-108">This returns the HMONITOR handle to each monitor, which is used with [**GetMonitorInfo**](/windows/desktop/api/Winuser/nf-winuser-getmonitorinfoa).</span></span> <span data-ttu-id="64b57-109">Pour énumérer tous les appareils de l’écran virtuel, utilisez **EnumDisplayMonitors**.</span><span class="sxs-lookup"><span data-stu-id="64b57-109">To enumerate all the devices in the virtual screen, use **EnumDisplayMonitors**.</span></span> <span data-ttu-id="64b57-110">comme indiqué dans le code suivant :</span><span class="sxs-lookup"><span data-stu-id="64b57-110">as shown in the following code:</span></span>


```C++
EnumDisplayMonitors(NULL, NULL, MyInfoEnumProc, 0);  
```



<span data-ttu-id="64b57-111">Pour obtenir des informations sur un périphérique d’affichage, utilisez [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) ou [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span><span class="sxs-lookup"><span data-stu-id="64b57-111">To get information about a display device, use [**EnumDisplaySettings**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsa) or [**EnumDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-enumdisplaysettingsexa).</span></span>

<span data-ttu-id="64b57-112">La fonction [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) est utilisée pour contrôler les périphériques d’affichage sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="64b57-112">The [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) function is used to control the display devices on the computer.</span></span> <span data-ttu-id="64b57-113">Il peut modifier la configuration des appareils, tels que la spécification de la position d’une analyse sur le bureau virtuel et la modification de la profondeur de bit de n’importe quel affichage.</span><span class="sxs-lookup"><span data-stu-id="64b57-113">It can modify the configuration of the devices, such as specifying the position of a monitor on the virtual desktop and changing the bit depth of any display.</span></span> <span data-ttu-id="64b57-114">En règle générale, une application n’utilise pas cette fonction.</span><span class="sxs-lookup"><span data-stu-id="64b57-114">Typically, an application does not use this function.</span></span> <span data-ttu-id="64b57-115">Pour ajouter par programme un moniteur d’affichage à un système à plusieurs écrans, définissez **DEVMODE. dmFields** sur \_ position DM et spécifiez une position (à l’aide de **DEVMODE. dmPosition** ) pour l’analyse que vous ajoutez qui est adjacente à au moins un pixel de la zone d’affichage d’une analyse existante.</span><span class="sxs-lookup"><span data-stu-id="64b57-115">To add a display monitor to a multiple-monitor system programmatically, set **DEVMODE.dmFields** to DM\_POSITION and specify a position (using **DEVMODE.dmPosition** ) for the monitor you are adding that is adjacent to at least one pixel of the display area of an existing monitor.</span></span> <span data-ttu-id="64b57-116">Pour détacher le moniteur, définissez **DEVMODE. dmFields** sur \_ position DM et définissez **DEVMODE. DmPelsWidth** et **DEVMODE. dmPelsHeight** sur zéro.</span><span class="sxs-lookup"><span data-stu-id="64b57-116">To detach the monitor, set **DEVMODE.dmFields** to DM\_POSITION and set **DEVMODE.dmPelsWidth** and **DEVMODE.dmPelsHeight** to zero.</span></span>

<span data-ttu-id="64b57-117">Le code suivant montre comment détacher tous les périphériques d’affichage secondaires du Bureau :</span><span class="sxs-lookup"><span data-stu-id="64b57-117">The following code demonstrates how to detach all secondary display devices from the desktop:</span></span>


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



<span data-ttu-id="64b57-118">Pour chaque périphérique d’affichage, l’application peut enregistrer des informations dans le Registre qui décrivent les paramètres de configuration de l’appareil, ainsi que des paramètres d’emplacement.</span><span class="sxs-lookup"><span data-stu-id="64b57-118">For each display device, the application can save information in the registry that describes the configuration parameters for the device, as well as location parameters.</span></span> <span data-ttu-id="64b57-119">L’application peut également déterminer les affichages qui font partie du bureau, et ceux qui ne le sont pas, par le biais du périphérique d’affichage \_ \_ attaché \_ à l’indicateur de \_ Bureau dans la structure du [**\_ périphérique d’affichage**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) .</span><span class="sxs-lookup"><span data-stu-id="64b57-119">The application can also determine which displays are part of the desktop, and which are not, through the DISPLAY\_DEVICE\_ATTACHED\_TO\_DESKTOP flag in the [**DISPLAY\_DEVICE**](/windows/desktop/api/Wingdi/ns-wingdi-display_devicea) structure.</span></span> <span data-ttu-id="64b57-120">Une fois que toutes les informations de configuration sont stockées dans le registre, l’application peut appeler de nouveau [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) pour modifier dynamiquement les paramètres, sans redémarrage nécessaire.</span><span class="sxs-lookup"><span data-stu-id="64b57-120">Once all the configuration information is stored in the registry, the application can call [**ChangeDisplaySettingsEx**](/windows/desktop/api/Winuser/nf-winuser-changedisplaysettingsexa) again to dynamically change the settings, with no restart required.</span></span>

 

 



