---
title: Restrictions sur l’extension de schéma
description: Afin de réduire le risque de modifications du schéma d’une application qui a pour but de réduire les autres applications et de préserver la cohérence du schéma, Active Directory Domain Services appliquer des restrictions sur le type de modifications de schéma qu’une application ou un utilisateur est autorisé à effectuer.
ms.assetid: 26254eb9-5dd9-414b-a398-be2a7f3b0279
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94db3c3c96f5c9b4e96cff923e70501a8977669defbc03b95fd2df019886a138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118184302"
---
# <a name="restrictions-on-schema-extension"></a>Restrictions sur l’extension de schéma

Afin de réduire le risque de modifications du schéma d’une application qui a pour but de réduire les autres applications et de préserver la cohérence du schéma, Active Directory Domain Services appliquer des restrictions sur le type de modifications de schéma qu’une application ou un utilisateur est autorisé à effectuer.

Les restrictions sont imposées uniquement lors de la modification d’objets de schéma existants. Le schéma est classé en deux catégories. les objets de schéma fournis avec Windows 2000 dans le schéma de base appartiennent à la catégorie 1. Tous les objets de schéma ajoutés ultérieurement par d’autres applications ou utilisateurs via l’extension de schéma dynamique appartiennent à la catégorie 2. La catégorie d’un objet de schéma peut être déterminée par le bit 0x10 défini dans l’attribut **systemFlags** de l’objet **classSchema** . Ce bit n’est défini que sur les objets de catégorie 1 et ne peut pas être modifié, ni défini sur un objet de catégorie 2.

L’attribut **systemFlags** est utilisé en interne par Active Directory Domain Services pour identifier les caractéristiques spéciales des objets « infrastructure » dans le schéma de base. Outre l’identification des objets catégorie 1, **systemFlags** détermine si un objet peut être déplacé, supprimé ou renommé. ces opérations sont empêchées pour les objets qui Windows 2000 dépendent de l’exécution.

Sur tous les objets de schéma, catégorie 1 ou 2, Active Directory Domain Services imposer les restrictions suivantes :

-   Vous ne pouvez pas ajouter un nouveau **mustContain** à une classe (directement ou par héritage en ajoutant une classe auxiliaire).
-   Vous ne pouvez pas supprimer de **mustContain** de la classe (directement ou par héritage).

En outre, les restrictions supplémentaires suivantes sont imposées sur les objets de schéma de catégorie 1 :

-   Vous ne pouvez pas modifier les attributs suivants d’un attribut Category 1 :

    -   **rangeLower** et **rangeUpper** (plage de valeurs).
    -   **attributeSecurityGuid** (détermine le jeu de propriétés auquel l’attribut appartient, le cas échéant).

-   Vous ne pouvez pas modifier le **defaultObjectCategory** d’une classe de catégorie 1.
-   Vous ne pouvez pas modifier l' **objectCategory** d’une instance d’une classe de catégorie 1.
-   Vous ne pouvez pas rendre obsolète une classe ou un attribut de catégorie 1.
-   Vous ne pouvez pas modifier le **lDAPDisplayName** d’une classe ou d’un attribut Category 1.
-   Vous ne pouvez pas renommer une classe ou un attribut Category 1.

 

 




