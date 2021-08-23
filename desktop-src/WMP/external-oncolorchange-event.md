---
title: External. OnColorChange, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnColorChange, événement
ms.assetid: f2cd44b1-c813-479b-b847-96ddb9572697
keywords:
- Lecteur Windows Media d’événements External. OnColorChange
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
ms.openlocfilehash: eae4ca15d4d7035fc342fa20263220560570d902e28b9245a6458ac59c40a4f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119648749"
---
# <a name="externaloncolorchange-event"></a>External. OnColorChange, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

l’événement **OnColorChange** se produit lorsque la couleur de l’interface utilisateur Lecteur Windows Media change.

``` syntax
window.external.OnColorChange = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que Lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement n’accepte aucun paramètre.

## <a name="remarks"></a>Remarques

les utilisateurs peuvent modifier la couleur de l’interface utilisateur Lecteur Windows Media. Vous pouvez utiliser cet événement pour personnaliser l’apparence de votre page Web hébergée en fonction du lecteur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 2 en ligne**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





