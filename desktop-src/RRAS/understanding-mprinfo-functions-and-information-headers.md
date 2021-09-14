---
title: Comprendre les fonctions et les en-têtes d’informations MprInfo
description: Les fonctions suivantes requièrent que l’appelant passe une structure ou un en-tête d’informations comme l’un des paramètres.
ms.assetid: 389002c9-2d24-4b35-ab5b-801fe2091db9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 001c39bf28500d7261b3eb99abf0266470daf3d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127416633"
---
# <a name="understanding-mprinfo-functions-and-information-headers"></a>Comprendre les fonctions et les en-têtes d’informations MprInfo

Les fonctions suivantes requièrent que l’appelant passe une structure ou un *en-tête* d’informations comme l’un des paramètres.



| Fonction d’administration                                                        | Fonction de configuration                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| Aucune fonction d’administration                                                     | [**MprConfigTransportCreate**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportcreate)                     |
| [**MprAdminTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportsetinfo)                   | [**MprConfigTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportsetinfo)                   |
| [**MprAdminInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportsetinfo) | [**MprConfigInterfaceTransportSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportsetinfo) |
| [**MprAdminInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportadd)         | [**MprConfigInterfaceTransportAdd**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportadd)         |



 

De même, les fonctions suivantes retournent des en-têtes d’informations.



| Fonction d’administration                                                        | Fonction de configuration                                                           |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [**MprAdminTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmintransportgetinfo)                   | [**MprConfigTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfigtransportgetinfo)                   |
| [**MprAdminInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacetransportgetinfo) | [**MprConfigInterfaceTransportGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mprconfiginterfacetransportgetinfo) |



 

Pour les fonctions de transport, l’en-tête d’informations contient des informations globales pour le transport. Pour les fonctions client (InterfaceTransport), l’en-tête contient des informations spécifiques au client (par exemple, OSPF) en cours de gestion.

Les en-têtes d’informations et leur contenu doivent être manipulés uniquement à l’aide des fonctions [MprInfo](router-information-functions.md) . Les développeurs ne doivent pas tenter de manipuler directement le contenu des en-têtes d’informations.

Les fonctions d’interface uniquement, telles que [**MprAdminInterfaceSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmininterfacesetinfo) , ne nécessitent pas l’utilisation de fonctions MprInfo. Les informations qui sont passées et retournées avec ces fonctions sont toujours sous la forme d’une structure d' [**\_ interface MPR**](/windows/desktop/api/Mprapi/ns-mprapi-mpr_interface_0) .

 

 




