---
title: Fonctions d’administration RAS
description: Cette documentation décrit les fonctions RRAS utilisées pour développer des logiciels afin d’administrer les connexions d’accès à distance RAS.
ms.assetid: 27cf63e2-9dd3-4bc1-98af-e93055d89492
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec0a18f6c49964d89c308b065289dd4de9fc22c5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311062"
---
# <a name="ras-administration-functions"></a>Fonctions d’administration RAS

Cette documentation décrit les fonctions RRAS utilisées pour développer des logiciels afin d’administrer les connexions d’accès à distance RAS. Ces fonctions sont les suivantes :

-   [**MprAdminConnectionClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionclearstats)
-   [**MprAdminConnectionEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenum)
-   [**MprAdminConnectionEnumEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionenumex)
-   [**MprAdminConnectionGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfo)
-   [**MprAdminConnectionGetInfoEx**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectiongetinfoex)
-   [**MprAdminConnectionRemoveQuarantine**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminconnectionremovequarantine)
-   [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats)
-   [**MprAdminPortDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportdisconnect)
-   [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum)
-   [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo)
-   [**MprAdminPortReset**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportreset)

Des fonctions supplémentaires sont utilisées pour l’administration RAS et l’administration du routeur. Les fonctions suivantes décrites dans la référence [fonctions d’administration du routeur](router-administration-functions.md) :

-   [**MprAdminBufferFree**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminbufferfree)
-   [**MprAdminGetErrorString**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingeterrorstring)
-   [**MprAdminIsServiceRunning**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminisservicerunning)
-   [**MprAdminServerConnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverconnect)
-   [**MprAdminServerDisconnect**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminserverdisconnect)

Pour implémenter une DLL d’administration RAS, utilisez les fonctions décrites dans la rubrique suivante :

-   [Fonctions de la DLL d’administration RAS](ras-admin-dll-functions.md)

Pour gérer les utilisateurs d’un serveur RAS, utilisez les fonctions décrites dans la rubrique suivante :

-   [Fonctions d’administration d’utilisateur RAS](ras-user-administration-functions.md)

 

 




