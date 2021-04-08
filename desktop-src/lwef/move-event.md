---
title: Déplacer l’événement
description: Déplacer l’événement
ms.assetid: 973e9e68-edbb-4741-b50e-57db96712df8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31facb1d57b807fb0322783a291b77ef5a7c1487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840093"
---
# <a name="move-event"></a>Déplacer l’événement

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un caractère est déplacé.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent* \_ **Move (ByVal** *CharacterID*, **ByVal** *X*, **ByVal** *Y*, **ByVal** *cause * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                   |
|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère qui a été déplacé.                                                                                                                                                                                                                                                                                                   |
| *X*           | Retourne la coordonnée x (en pixels) du bord supérieur du nouvel emplacement du cadre de caractère sous la forme d’un entier.                                                                                                                                                                                                                                         |
| *O*           | Retourne la coordonnée y (en pixels) du bord gauche du nouvel emplacement du cadre de caractère sous la forme d’un entier.                                                                                                                                                                                                                                        |
| *Cause*       | Retourne une valeur qui indique ce qui a provoqué le déplacement du caractère. 1 l’utilisateur a fait glisser le caractère.<br/> 2 votre application cliente a déplacé le caractère.<br/> 3 une autre application cliente a déplacé le caractère.<br/> 4 le serveur de l’agent a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Cet événement se produit lorsque l’utilisateur ou une application modifie la position du caractère. Les coordonnées sont pertinentes dans l’angle supérieur gauche de l’écran. Cet événement est envoyé uniquement aux clients du caractère (applications qui ont chargé le caractère).

**Voir aussi**

[**Propriété MoveCause**](movecause-property.md), [ **événement Size**](size-event.md)

 

 





