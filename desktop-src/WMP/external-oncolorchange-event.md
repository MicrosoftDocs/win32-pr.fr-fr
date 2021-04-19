---
title: External. OnColorChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnColorChange, événement
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Événement External. OnColorChange lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnColorChange Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 029c8bb860443ed026737c7413be2bed8862c6d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542398"
---
# <a name="externaloncolorchange-event"></a>External. OnColorChange, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnColorChange** se produit lorsque la couleur de l’interface utilisateur du lecteur Windows Media change.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement n’accepte aucun paramètre.

## <a name="remarks"></a>Notes

Les utilisateurs peuvent modifier la couleur de l’interface utilisateur du lecteur Windows Media. Vous pouvez utiliser cet événement pour personnaliser l’apparence de votre page Web hébergée en fonction du lecteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





