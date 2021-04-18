---
title: External. SelectedTaskPane
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La propriété SelectedTaskPane spécifie ou récupère le volet des tâches actuellement sélectionné.
ms.assetid: af7b4627-1336-444c-9b4e-5f2e07d9eea7
keywords:
- External. SelectedTaskPane Windows Media Player
topic_type:
- apiref
api_name:
- External.SelectedTaskPane
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28535e0497362a2153bcaad439425174e9c1bdc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532725"
---
# <a name="externalselectedtaskpane"></a>External. SelectedTaskPane

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La propriété **SelectedTaskPane** spécifie ou récupère le volet des tâches actuellement sélectionné.

## <a name="syntax"></a>Syntaxe

Window. external. SelectedTaskPane = *servicetask*

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture. Les valeurs possibles sont « ServiceTask1 », « ServiceTask2 » et « ServiceTask3 ».

## <a name="remarks"></a>Notes

Si vous spécifiez une valeur pour cette propriété, le bouton correspondant à ce volet est mis en surbrillance. Elle ne rend pas le volet de tâches spécifié actif. Vous devez spécifier une valeur pour cette propriété afin de définir le bouton du volet de tâches actuel pour votre page Web lors du chargement de la page pour vous assurer que le bouton de volet de tâches correct est actif.

Pour rendre un volet de tâches particulier actif, utilisez la méthode **NavigateTaskPaneURL** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 10 ou version ultérieure<br/>                                        |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> <dt>

[**External. NavigateTaskPaneURL**](external-navigatetaskpaneurl.md)
</dt> </dl>

 

 





