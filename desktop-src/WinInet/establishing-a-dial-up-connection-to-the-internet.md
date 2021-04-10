---
title: Établissement d’une connexion d’accès à distance à Internet
description: Les fonctions suivantes sont utilisées pour gérer les connexions de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031722"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a>Établissement d’une connexion d’accès à distance à Internet

Les fonctions suivantes sont utilisées pour gérer les connexions de modem.

-   [**InternetAutodial**](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [**InternetAutodialHangup**](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [**InternetDial**](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [**InternetGetConnectedState**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [**InternetGetConnectedStateEx**](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [**InternetHangUp**](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [**InternetGoOnline**](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> Les fonctions d’accès distant WinINet ne prennent pas en charge les connexions à double numérotation, l’authentification par carte à puce ou les connexions nécessitant une certification basée sur le registre.

 

> [!Note]  
> À compter de Windows Vista et de Windows Server 2008, les fonctions d’accès distant WinINet utilisent les [fonctions RAS](/windows/desktop/RRAS/remote-access-service-functions) pour établir une connexion d’accès à distance. WinINet prend en charge les fonctionnalités documentées dans la fonction [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 