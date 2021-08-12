---
description: Windows 8, Windows Server 2012 et versions ultérieures incluent une nouvelle fonctionnalité de gestionnaire de connexions qui permet aux utilisateurs de se connecter facilement à Internet et à d’autres réseaux (par exemple, des réseaux professionnels et personnels).
ms.assetid: 6b2f5a50-fabd-4c80-acc8-a0883c939632
title: API d’interface utilisateur sans fil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e2b2af7faccc5452163ad89ed28d12e7de917f4b872011165e0cfb1760657dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118619926"
---
# <a name="wireless-user-interface-apis"></a>API d’interface utilisateur sans fil

Windows 8, Windows Server 2012 et versions ultérieures incluent une nouvelle fonctionnalité de gestionnaire de connexions qui permet aux utilisateurs de se connecter facilement à Internet et à d’autres réseaux (par exemple, des réseaux professionnels et personnels). cette nouvelle fonctionnalité de gestionnaire de connexions remplace l’ancienne **Connecter sur un réseau** et gère les interfaces utilisateur de **réseaux sans fil** incluses avec les anciennes versions de Windows pour gérer les connexions Wifi natives.

sur Windows 7, Windows Server 2008 et Windows Vista, un certain nombre d’interfaces utilisateur sont utilisées pour se connecter à un réseau sans fil ou le configurer. ces interfaces utilisateur peuvent être démarrées dans une application à l’aide des fonctions Wifi Native et Windows Shell. ces interfaces utilisateur ne sont pas disponibles sur Windows 8, Windows Server 2012 et versions ultérieures.

**Windows xp avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Vous ne pouvez pas démarrer une interface utilisateur utilisée pour se connecter ou configurer un réseau sans fil dans une application par programme.

## <a name="connect-to-a-network"></a>Se connecter à un réseau

sur Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 et Windows Vista, l’assistant **Connecter à un réseau** peut être utilisé pour établir une connexion à un réseau sans fil. vous pouvez utiliser la fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour démarrer le **Connecter à un assistant réseau** .

le code suivant illustre un appel [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) qui démarre l' **Connecter à un assistant réseau** .


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



## <a name="manage-wireless-networks"></a>**Gérer les réseaux sans fil**

sur Windows 7, Windows Server 2008 et Windows Vista, l’élément **gérer les réseaux sans fil** du panneau de configuration est utilisé pour gérer les profils de réseau sans fil. La fonction [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) peut également être utilisée pour démarrer l’élément **gérer les réseaux sans fil** . le chemin d’accès à utiliser lors de l’appel de **ShellExecute** sur Windows 7 et Windows Vista est le suivant :

`shell:::{26EE0668-A00A-44D7-9371-BEB064C98683}\3\::{1fa9085f-25a2-489b-85d4-86326eedcd87}  `.

L’exemple de code suivant montre comment utiliser [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) pour démarrer l’Assistant **réseaux sans fil gérés** à partir d’une application.


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



## <a name="advanced-settings-for-wireless-network-profiles"></a>Paramètres avancé pour les profils de réseau sans fil

Windows Vista et versions ultérieures incluent une interface utilisateur avancée qui permet d’afficher et de modifier les paramètres avancés d’un profil de réseau sans fil. Vous pouvez démarrer cette interface utilisateur avancée en appelant la fonction [**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de la WiFi Native](using-native-wifi.md)
</dt> <dt>

[Exemples de profils sans fil](wireless-profile-samples.md)
</dt> <dt>

[**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea)
</dt> <dt>

[**WlanUIEditProfile**](/windows/desktop/api/wlanapi/nf-wlanapi-wlanuieditprofile)
</dt> </dl>

 

 
