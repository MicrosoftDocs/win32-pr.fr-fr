---
title: Fonctions d’administration d’utilisateur RAS
description: Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance
ms.assetid: e58fa4a6-16d3-4953-bf21-887d08e25af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf8c1e7df962eff2064dac06da256f3a78e8ed17
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463586"
---
# <a name="ras-user-administration-functions"></a>Fonctions d’administration d’utilisateur RAS

Utilisez les fonctions suivantes pour gérer les utilisateurs d’accès à distance :

-   [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver)
-   [**MprAdminSendUserMessage**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminsendusermessage)
-   [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)
-   [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)

Pour obtenir la liste des utilisateurs actuels sur un domaine particulier, utilisez la fonction [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) . Le prototype de cette fonction se trouve dans le fichier d’en-tête lmaccess. h.

 

 