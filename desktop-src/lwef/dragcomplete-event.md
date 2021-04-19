---
title: Événement DragComplete
description: Événement DragComplete
ms.assetid: b48e7097-9d9d-4eab-9dfc-68dbc9793382
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7a02fe98e4cf3cdefc1b7734305067550e4923
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512448"
---
# <a name="dragcomplete-event"></a>Événement DragComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque l’utilisateur termine le glissement d’un caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent * * * \_ DragComplete* *  **(ByVal** *CharacterID*, **ByVal** *Button*, **ByVal** *MAJ*, **ByVal** *X*, **ByVal** *Y * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère déplacé sous la forme d’une chaîne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| *Button*      | Retourne un entier qui identifie le bouton qui a été enfoncé et relâché pour déclencher l’événement. L’argument Button est un champ de bits avec les bits correspondant au bouton gauche (bit 0), le bouton droit (bit 1) et le bouton central (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. Seul l’un des bits est défini, ce qui indique le bouton à l’origine de l’événement.                                                                                                                                                                                                                                                                                |
| *Majuscule*       | Retourne un entier qui correspond à l’état des touches Maj, CTRL et ALT lorsque le bouton spécifié dans l’argument de bouton est enfoncé ou relâché. Un bit est défini si la touche est enfoncée. L’argument Shift est un champ de bits avec les bits de poids faible correspondant à la touche Maj (bit 0), la touche CTRL (bit 1) et la touche ALT (bit 2). Ces bits correspondent respectivement aux valeurs 1, 2 et 4. L’argument Shift indique l’état de ces clés. Certains, tous ou aucun des bits peuvent être définis, ce qui indique qu’une partie, la totalité ou aucune des touches est enfoncée. Par exemple, si les touches CTRL et ALT étaient enfoncées, la valeur de Shift serait 6. |
| *X, Y*         | Retourne un entier qui spécifie l’emplacement actuel du pointeur de la souris. Les valeurs X et Y sont toujours exprimées en pixels, par rapport à l’angle supérieur gauche de l’écran.                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Cet événement est envoyé uniquement au client d’entrée-actif d’un caractère. Lorsque l’utilisateur fait glisser un caractère sans client d’entrée-actif, le serveur définit son dernier client d’entrée/de sortie en tant que client en entrée-actif, en envoyant l’événement [**ActivateInput**](activateinput-event.md) à ce client, puis en envoyant les événements [**DragStart**](dragstart-event.md) et **DragComplete** .

### <a name="see-also"></a>Voir aussi

[**Événement DragStart**](dragstart-event.md)


 

 




