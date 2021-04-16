---
description: Windows 8, Windows Server 2012 et versions ultérieures incluent une nouvelle fonctionnalité de gestionnaire de connexions qui permet aux utilisateurs de se connecter facilement à Internet et à d’autres réseaux (par exemple, des réseaux professionnels et personnels).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API d’interface utilisateur sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5814ea8daa55ab3ec1bf431543174cf57fdfa7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530297"
---
# <a name="wireless-user-interface-apis"></a><span data-ttu-id="491e6-103">API d’interface utilisateur sans fil</span><span class="sxs-lookup"><span data-stu-id="491e6-103">Wireless User Interface APIs</span></span>

<span data-ttu-id="491e6-104">Windows 8, Windows Server 2012 et versions ultérieures incluent une nouvelle fonctionnalité de gestionnaire de connexions qui permet aux utilisateurs de se connecter facilement à Internet et à d’autres réseaux (par exemple, des réseaux professionnels et personnels).</span><span class="sxs-lookup"><span data-stu-id="491e6-104">Windows 8, Windows Server 2012, and later include a new Connection Manager feature that allows users to easily connect to the Internet and to other networks (work and home networks, for example).</span></span> <span data-ttu-id="491e6-105">Cette nouvelle fonctionnalité du gestionnaire de connexions remplace l’ancienne **connexion à un réseau** et gère les interfaces utilisateur des **réseaux sans fil** incluses avec les anciennes versions de Windows pour la gestion des connexions WiFi natives.</span><span class="sxs-lookup"><span data-stu-id="491e6-105">This new Connection Manager feature replaces the older **Connect to a network** and **Manage Wireless Networks** user interfaces included with older versions of Windows for managing Native Wifi connections.</span></span>

<span data-ttu-id="491e6-106">Sur Windows 7, Windows Server 2008 et Windows Vista, il existe un certain nombre d’interfaces utilisateur utilisées pour se connecter à un réseau sans fil ou le configurer.</span><span class="sxs-lookup"><span data-stu-id="491e6-106">On Windows 7, Windows Server 2008, and Windows Vista, there are a number of user interfaces (UIs) used to connect to or configure a wireless network.</span></span> <span data-ttu-id="491e6-107">Ces interfaces utilisateur peuvent être démarrées dans une application à l’aide des fonctions Wi-Fi et Windows Shell natives.</span><span class="sxs-lookup"><span data-stu-id="491e6-107">These UIs can be started in an application using Native Wifi and Windows Shell functions.</span></span> <span data-ttu-id="491e6-108">Ces interfaces utilisateur ne sont pas disponibles sur Windows 8, Windows Server 2012 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="491e6-108">These UIs are not available on Windows 8, Windows Server 2012, and later.</span></span>

<span data-ttu-id="491e6-109">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Vous ne pouvez pas démarrer une interface utilisateur utilisée pour se connecter ou configurer un réseau sans fil dans une application par programme.</span><span class="sxs-lookup"><span data-stu-id="491e6-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** You cannot start any UI used to connect to or configure a wireless network in an application programmatically.</span></span>

## <a name="connect-to-a-network"></a><span data-ttu-id="491e6-110">Se connecter à un réseau</span><span class="sxs-lookup"><span data-stu-id="491e6-110">Connect to a network</span></span>

<span data-ttu-id="491e6-111">Sur Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 et Windows Vista, l’Assistant **connexion à un réseau** peut être utilisé pour établir une connexion à un réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="491e6-111">On Windows 8, Windows Server 2012, Windows 7, Windows Server 2008, and Windows Vista, the **Connect to a network** wizard can be used to establish a connection to a wireless network.</span></span> <span data-ttu-id="491e6-112">Vous pouvez utiliser la fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour démarrer l’Assistant **connexion à un réseau** .</span><span class="sxs-lookup"><span data-stu-id="491e6-112">You can use the [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function to start the **Connect to a network** wizard.</span></span>

<span data-ttu-id="491e6-113">Le code suivant illustre un appel [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) qui démarre l’Assistant **connexion à un réseau** .</span><span class="sxs-lookup"><span data-stu-id="491e6-113">The following code shows a [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) call that starts the **Connect to a network** wizard.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

void wmain()
{
   ShellExecute(
      NULL, 
      L"open", 
      L"shell:::{21EC2020-3AEA-1069-A2DD-08002B30309D}\\::{38a98528-6cbf-4ca9-8dc0-b1e1d10f7b1b}",
      NULL,
      NULL,
      SW_SHOWNORMAL);
}
```



## <a name="manage-wireless-networks"></a><span data-ttu-id="491e6-114">**Gérer les réseaux sans fil**</span><span class="sxs-lookup"><span data-stu-id="491e6-114">**Manage Wireless Networks**</span></span>

<span data-ttu-id="491e6-115">Sur Windows 7, Windows Server 2008 et Windows Vista, l’élément **gérer les réseaux sans fil** du panneau de configuration permet de gérer les profils de réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="491e6-115">On Windows 7, Windows Server 2008, and Windows Vista, the **Manage Wireless Networks** Control Panel item is used to manage wireless network profiles.</span></span> <span data-ttu-id="491e6-116">La fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) peut également être utilisée pour démarrer l’élément **gérer les réseaux sans fil** .</span><span class="sxs-lookup"><span data-stu-id="491e6-116">The [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) function can also be used to start the **Manage Wireless Networks** item.</span></span> <span data-ttu-id="491e6-117">Le chemin d’accès à utiliser lors de l’appel de **ShellExecute** sur Windows 7 et Windows Vista est le suivant :</span><span class="sxs-lookup"><span data-stu-id="491e6-117">The path to use when calling **ShellExecute** on Windows 7 and Windows Vista is the following:</span></span>

<span data-ttu-id="491e6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span><span class="sxs-lookup"><span data-stu-id="491e6-118">`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.</span></span>

<span data-ttu-id="491e6-119">L’exemple de code suivant montre comment utiliser [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour démarrer l’Assistant **réseaux sans fil gérés** à partir d’une application.</span><span class="sxs-lookup"><span data-stu-id="491e6-119">The following sample code shows how to use [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) to start the **Managed Wireless Networks** wizard from an application.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <shellapi.h>
#include <stdio.h>

// Need to link with shell32.lib
#pragma comment(lib, "shell32.lib")

int wmain()
{

    //-----------------------------------------
    // Declare and initialize variables
    HINSTANCE nResult;

    PCWSTR lpOperation = L"open";    
    PCWSTR lpFile= 
        L"shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\\3\\::{1fa9085f-25a2-489b-85d4-86326eedcd87}";

    nResult = ShellExecute(
        NULL,   // Hwnd
        lpOperation, // do not request elevation unless needed
        lpFile,
        NULL, // no parameters 
        NULL, // use current working directory 
        SW_SHOWNORMAL);

    if((int)nResult == SE_ERR_ACCESSDENIED)
    {
        wprintf(L"ShellExecute returned access denied\n");
        wprintf(L"  Executing the ShellExecute command elevated\n"); 

        nResult = ShellExecute(
            NULL,
            L"runas", // Trick for requesting elevation
            lpFile,
            NULL, // no parameters 
            NULL, // use current working directory 
            SW_HIDE);
    }

    if ( (int) nResult < 32) {
        wprintf(L" ShellExecute failed with error %d\n", (int) nResult);
        return 1;
    }    
    else {    
        wprintf(L" ShellExecute succeeded and returned value %d\n", (int) nResult);
        return 0;
    }
}

```



## <a name="advanced-settings-for-wireless-network-profiles"></a><span data-ttu-id="491e6-120">Paramètres avancés pour les profils de réseau sans fil</span><span class="sxs-lookup"><span data-stu-id="491e6-120">Advanced Settings for Wireless Network Profiles</span></span>

<span data-ttu-id="491e6-121">Windows Vista et versions ultérieures incluent une interface utilisateur avancée qui permet d’afficher et de modifier les paramètres avancés d’un profil de réseau sans fil.</span><span class="sxs-lookup"><span data-stu-id="491e6-121">Windows Vista and later include an advanced user interface that is used to view and edit advanced settings of a wireless network profile.</span></span> <span data-ttu-id="491e6-122">Vous pouvez démarrer cette interface utilisateur avancée en appelant la fonction [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .</span><span class="sxs-lookup"><span data-stu-id="491e6-122">You can start this advanced UI by calling the [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="491e6-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="491e6-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="491e6-124">Utilisation de la WiFi Native</span><span class="sxs-lookup"><span data-stu-id="491e6-124">Using Native Wifi</span></span>](using-native-wifi.md)
</dt> <dt>

[<span data-ttu-id="491e6-125">Exemples de profils sans fil</span><span class="sxs-lookup"><span data-stu-id="491e6-125">Wireless Profile Samples</span></span>](wireless-profile-samples.md)
</dt> <dt>

[<span data-ttu-id="491e6-126">**ShellExecute**</span><span class="sxs-lookup"><span data-stu-id="491e6-126">**ShellExecute**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[<span data-ttu-id="491e6-127">**WlanUIEditProfile**</span><span class="sxs-lookup"><span data-stu-id="491e6-127">**WlanUIEditProfile**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
