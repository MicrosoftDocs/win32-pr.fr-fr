---
description: Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’objets
ms.assetid: 79dd4a45-c42c-4775-93ce-6e3206894d63
title: Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’objets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fddd5d78ff5b02bbbe4b9b7a7ce0b77d7be263f9fd3926f44411469af2bb3c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117785249"
---
# <a name="aces-to-control-access-to-an-objects-properties"></a>Entrées de contrôle d’accès pour contrôler l’accès aux propriétés d’un objet

La [*liste de contrôle d’accès discrétionnaire*](/windows/desktop/SecGloss/d-gly) (DACL) d’un objet de service d’annuaire peut contenir une hiérarchie d’entrées de contrôle d’accès (ACE, [*Access Control Entries*](/windows/desktop/SecGloss/a-gly) ), comme suit :

1.  ACE qui protègent l’objet lui-même
2.  [ACE spécifiques](object-specific-aces.md) à l’objet qui protègent un jeu de propriétés spécifié sur l’objet
3.  ACE spécifiques à l’objet qui protègent une propriété spécifiée sur l’objet

Au sein de cette hiérarchie, les droits accordés ou refusés à un niveau supérieur s’appliquent également aux niveaux inférieurs. Par exemple, si une entrée de contrôle d’accès spécifique à un objet sur un jeu de propriétés autorise un tiers de confiance \_ \_ à lire la propriété DS \_ Read \_ prop, le tiers de confiance dispose d’un accès en lecture implicite à toutes les propriétés de ce jeu de propriétés. De la même façon, une entrée de contrôle d’accès sur l’objet lui-même qui autorise les publicités \_ appropriées \_ pour l' \_ accès en lecture DS permet \_ au tiers de confiance d’accéder en lecture à toutes les propriétés de l’objet.

L’illustration suivante montre l’arborescence d’un objet de service d’annuaire hypothétique et de ses jeux de propriétés et propriétés.

![hiérarchie d’objets de service d’annuaire](images/accctrl2.png)

Supposons que vous souhaitez autoriser l’accès suivant aux propriétés de cet objet DS :

-   Autoriser le groupe A une autorisation de lecture/écriture sur toutes les propriétés de l’objet
-   Autoriser tout le monde à accéder en lecture/écriture à toutes les propriétés, à l’exception de la propriété D

Pour ce faire, définissez les ACE dans la liste DACL de l’objet, comme indiqué dans le tableau suivant.



| Tiers  | GUID de l’objet    | Type d’entrée de contrôle d’accès                  | Droits d’accès                                             |
|----------|----------------|---------------------------|-----------------------------------------------------------|
| Group A  | Aucun           | Accès-ACE autorisé        | droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop. |
| Tout le monde | Jeu de propriétés 1 | ACE de l’objet Access-allowed | droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop. |
| Tout le monde | Propriété C     | ACE de l’objet Access-allowed | droits \_ d' \_ \_ \_ \| \_ \_ \_ écriture DS \_ de lecture de la prop. |



 

L’entrée du contrôle d’accès pour le groupe A n’a pas de GUID d’objet, ce qui signifie qu’elle autorise l’accès à toutes les propriétés de l’objet. L’ACE spécifique à l’objet pour le jeu de propriétés 1 autorise tout le monde à accéder aux propriétés A et B. L’autre entrée du contrôle d’accès spécifique à l’objet permet à tout le monde d’accéder à la propriété C. Notez que même si cette liste DACL n’a pas d’ACE d’accès refusé, elle refuse implicitement l’accès à la propriété D à tout le monde, sauf le groupe A.

Lorsqu’un utilisateur tente d’accéder à la propriété d’un objet, le système vérifie les ACE, dans l’ordre, jusqu’à ce que l’accès demandé soit explicitement accordé, refusé ou qu’il n’y ait plus d’entrées de contrôle d’accès, auquel cas l’accès est refusé implicitement.

Le système évalue les éléments suivants :

-   ACE qui s’appliquent à l’objet lui-même
-   ACE spécifiques à l’objet qui s’appliquent au jeu de propriétés qui contient la propriété en cours d’accès
-   ACE spécifiques aux objets qui s’appliquent à la propriété faisant l’objet d’un accès

Le système ignore les ACE spécifiques aux objets qui s’appliquent à d’autres jeux de propriétés ou propriétés.

 

 
