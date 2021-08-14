---
title: Fonctions de l’interface du routeur
description: Utilisez les fonctions suivantes pour administrer les interfaces sur le routeur.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bcaaf257e31623036a075c21da66d4665b3afe7e821f8f246f6a225e02b8272
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117787835"
---
# <a name="router-interface-functions"></a>Fonctions de l’interface du routeur

Utilisez les fonctions suivantes pour administrer les interfaces sur le routeur.



| Fonction d’administration                                          | Fonction de configuration                                             |
|------------------------------------------------------------------|--------------------------------------------------------------------|
| [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate)       | [**MprConfigInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacecreate)       |
| [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete)       | [**MprConfigInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacedelete)       |
| [**MprAdminInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfaceenum)           | [**MprConfigInterfaceEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfaceenum)           |
| [**MprAdminInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegethandle) | [**MprConfigInterfaceGetHandle**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegethandle) |
| [**MprAdminInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacegetinfo)     | [**MprConfigInterfaceGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacegetinfo)     |
| [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo)     | [**MprConfigInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacesetinfo)     |



 

Ces fonctions affectent les interfaces elles-mêmes, pas les clients qui s’exécutent sur les interfaces. Pour cette raison, aucune des fonctions n’impose à l’appelant de spécifier un transport particulier (IP ou IPX); Bien que les clients (tels que les protocoles de routage) soient associés à des transports particuliers, les interfaces elles-mêmes ne le sont pas.

Ces fonctions sont gérées directement par DIM. Ils n’utilisent pas les gestionnaires de routeur.

Les fonctions [**MprAdminInterfaceCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacecreate) et [**MprAdminInterfaceDelete**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacedelete) ne peuvent pas créer ou supprimer des interfaces LAN. Ils peuvent uniquement créer ou supprimer des interfaces de connexion à la demande. Pour obtenir la liste des types d’interfaces, consultez [**\_ \_ type d’interface de routeur**](/windows/desktop/api/Mprapi/ne-mprapi-router_interface_type) .

 

 




