---
title: Messages communiqués par le biais des interfaces utilisateur
description: Cette rubrique répertorie les messages qu’un service d’annuaire peut envoyer à partir d’une interface utilisateur.
ms.assetid: c81a3c44-c01d-4029-8a7d-6e0911d4f5ab
ms.tgt_platform: multiple
keywords:
- Messages communiqués par le biais des interfaces utilisateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b20b2706ae9f03109064c459ce494fb38da3f4579ca8f5b03ade970fcb0391f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118186571"
---
# <a name="messages-communicated-through-user-interfaces"></a>Messages communiqués par le biais des interfaces utilisateur

Cette rubrique répertorie les messages qu’un service d’annuaire peut envoyer à partir d’une interface utilisateur.

## <a name="common-query-page-messages"></a>Messages de page de requête communs

Les messages suivants sont envoyés à une page d’extension de formulaire de requête du service d’annuaire dans la fonction de rappel [**CQPageProc**](/windows/desktop/api/Cmnquery/nc-cmnquery-lpcqpageproc) :

-   [**CQPM \_ CLEARFORM**](cqpm-clearform.md)
-   [**CQPM \_ activer**](cqpm-enable.md)
-   [**CQPM \_ GETPARAMETERS**](cqpm-getparameters.md)
-   [**CQPM \_ HANDLERSPECIFIC**](cqpm-handlerspecific.md)
-   [**aide de CQPM \_**](cqpm-help.md)
-   [**initialisation de CQPM \_**](cqpm-initialize.md)
-   [**CQPM \_ persistant**](cqpm-persist.md)
-   [**version de CQPM \_**](cqpm-release.md)
-   [**CQPM \_ SETDEFAULTPARAMETERS**](cqpm-setdefaultparameters.md)

## <a name="miscellaneous-messages"></a>Messages divers

Le tableau suivant répertorie les messages qu’un service d’annuaire peut envoyer.



| Message                  | Valeur                     | Description                                                                                                                                                                                                                                   |
|--------------------------|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_message ATTRCHANGED \_ DSPROP | "DsPropAttrChanged"       | Message envoyé pour synchroniser les pages de propriétés et les outils d’administration de service d’annuaire, déclarés dans dsclient. h.                                                                                                                       |
| DSQPM \_ GETCLASSLIST      | CQPM \_ HANDLERSPECIFIC + 0   | Message de page envoyé aux pages de formulaire pour récupérer une liste de classes pour la requête, utilisé par le sélecteur de champ et la propriété bien pour générer sa liste de classes d’affichage. wParam = Flags et lParam = LPLPDSQUERYCLASSLIST, déclarés dans dsquery. h. |
| DSQPM \_ HELPTOPICS        | (CQPM \_ HANDLERSPECIFIC + 1) | Message de page envoyé aux pages de formulaire pour gérer la demande de « rubriques d’aide ». wParam = 0, lParam = hWndParent, déclaré dans dsquery. h.                                                                                                         |



 

 

 




