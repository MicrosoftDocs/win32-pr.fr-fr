---
title: Propriété MoveCause
description: Propriété MoveCause
ms.assetid: 8f78a6da-8498-4a39-a4b9-5ab7a43d97f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7f91d068befa2b919c04818c46dbc1a48faa0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840094"
---
# <a name="movecause-property"></a>Propriété MoveCause

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur entière qui spécifie ce qui a provoqué le dernier déplacement du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent*. **Caractères («***CharacterID***»). MoveCause**



| Valeur | Description                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| 0     | Le caractère n’a pas été déplacé.                                                          |
| 1     | L’utilisateur a déplacé le caractère.                                                              |
| 2     | Votre application a déplacé le caractère.                                                      |
| 3     | Une autre application cliente a déplacé le caractère.                                            |
| 4     | Le serveur de l’agent a déplacé le caractère pour le garder à l’écran après une modification de la résolution de l’écran. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Vous pouvez utiliser cette propriété pour déterminer ce qui a provoqué le déplacement du caractère, lorsque plusieurs applications partagent le même caractère. Ces valeurs sont les mêmes que celles retournées par l’événement [**Move**](move-event.md) .

## <a name="see-also"></a>Voir aussi

[**Move, événement**](move-event.md), [ **méthode MoveTo**](moveto-method.md)


 

 




