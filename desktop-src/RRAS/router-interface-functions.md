---
title: Fonctions de l’interface du routeur
description: Utilisez les fonctions suivantes pour administrer les interfaces sur le routeur.
ms.assetid: e988753e-908a-4c42-aad3-dd9f641c90a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3a5318eedfbc3a04c13549012fda3bd4d93b4d9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127239502"
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

 

 




