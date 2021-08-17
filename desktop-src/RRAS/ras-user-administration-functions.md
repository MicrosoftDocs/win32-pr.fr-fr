---
title: Fonctions d’administration d’utilisateur RAS
description: Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be0965a2befbe8a52ff91c2a1323a0455072fbe696d29f5a3cbb15e40e3b7c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789131"
---
# <a name="ras-user-administration-functions"></a>Fonctions d’administration d’utilisateur RAS

Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance :

-   [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

Pour obtenir la liste des utilisateurs actuels sur un domaine particulier, utilisez la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) . Le prototype de cette fonction se trouve dans le fichier d’en-tête lmaccess. h.

 

 