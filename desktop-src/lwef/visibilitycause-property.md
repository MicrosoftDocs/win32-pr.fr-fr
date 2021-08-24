---
title: Propriété VisibilityCause
description: Propriété VisibilityCause
ms.assetid: 106574ef-af5f-44cf-9efb-9e6da19ebc1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f1e90b77dfdfae364761254676d0867a43aebacf516d4f2adad2973700d7e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119398789"
---
# <a name="visibilitycause-property"></a>Propriété VisibilityCause

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur entière qui spécifie ce qui a provoqué l’état visible du caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent*. **Caractères («**_CharacterID_*_»). VisibilityCause_*



| Valeur | Description                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------|
| 0     | Le caractère n’a pas été affiché.                                                                            |
| 1     | Utilisateur a masqué le caractère à l’aide de la commande dans le menu contextuel de l’icône de la barre des tâches du caractère ou à l’aide de l’entrée vocale.. |
| 2     | L’utilisateur a affiché le caractère.                                                                               |
| 3     | Votre application a masqué le caractère.                                                                          |
| 4     | Votre application a affiché le caractère.                                                                       |
| 5     | Une autre application cliente a masqué le caractère.                                                                |
| 6     | Une autre application cliente a affiché le caractère.                                                             |
| 7     | L’utilisateur a masqué le caractère à l’aide de la commande dans le menu contextuel du caractère.                                 |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez utiliser cette propriété pour déterminer ce qui a provoqué le déplacement du caractère lorsque plusieurs applications partagent le même caractère. Ces valeurs sont les mêmes que celles retournées par les événements d' [**affichage**](show-event.md) et de [**masquage**](hide-event.md) .

## <a name="see-also"></a>Voir aussi

[**Masquer les événements**](hide-event.md), [**afficher les événements**](show-event.md), masquer la [**méthode**](hide-method.md), afficher la [**méthode**](show-method.md)


 

 




