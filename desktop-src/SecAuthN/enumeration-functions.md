---
description: Si votre fournisseur de réseau doit prendre en charge l’exploration de ses ressources réseau, il doit implémenter les fonctions suivantes. MPR appelle ces fonctions pour énumérer les ressources.
ms.assetid: 9f7c0e5b-1358-43f8-84e4-26e84a2275ba
title: Fonctions d’énumération
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08f119256c4976e393795b45caf2fab9e7cec5353fed54718ef0be8db994ef2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008237"
---
# <a name="enumeration-functions"></a>Fonctions d’énumération

Si votre fournisseur de réseau doit prendre en charge l’exploration de ses ressources réseau, il doit implémenter les fonctions suivantes. MPR appelle ces fonctions pour énumérer les ressources.

Un fournisseur réseau n’est pas tenu d’implémenter les fonctions d’énumération. Toutefois, si un fournisseur de réseau implémente [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum), [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)ou [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum), il doit également implémenter les deux autres fonctions d’énumération.



| Fonction                                                     | Description                                                                                                                                                         |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum)                             | Ouvre une énumération des ressources réseau ou des connexions existantes.                                                                                                  |
| [**NPEnumResource**](/windows/desktop/api/Npapi/nf-npapi-npenumresource)                     | Effectue une énumération sur un handle retourné par [**NPOpenEnum**](/windows/desktop/api/Npapi/nf-npapi-npopenenum).                                                                                   |
| [**NPCloseEnum**](/windows/desktop/api/Npapi/nf-npapi-npcloseenum)                           | Ferme une énumération.                                                                                                                                              |
| [**NPGetResourceInformation**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceinformation) | Détermine si le fournisseur est le fournisseur correct pour répondre à une demande pour une ressource réseau spécifiée et retourne des informations sur le type de la ressource. |
| [**NPGetResourceParent**](/windows/desktop/api/Npapi/nf-npapi-npgetresourceparent)           | Retourne le parent d’une ressource réseau spécifiée dans la hiérarchie de navigation.                                                                                         |



 

 

 



