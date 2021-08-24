---
title: Établissement d’une connexion d’accès à distance à Internet
description: Les fonctions suivantes sont utilisées pour gérer les connexions de modem.
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ac81096d657453d1ebaa0182f39d31af0fe96c01e73122a2de6e0ba9a765e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955589"
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
> à compter de Windows Vista et Windows Server 2008, les fonctions d’accès distant WinINet utilisent les [fonctions RAS](/windows/desktop/RRAS/remote-access-service-functions) pour établir une connexion d’accès à distance. WinINet prend en charge les fonctionnalités documentées dans la fonction [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) .

 

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 