---
title: Événement External. OnColorChange (type 1)
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | Événement External. OnColorChange (type 1)
ms.assetid: 45e6ec4a-e680-4d50-8fb7-410f12383eef
keywords:
- External. OnColorChange, événement (type 1) lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnColorChange Event (Type 1)
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11805cc154c60b8a765f46041f74d40929df418d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541302"
---
# <a name="externaloncolorchange-event-type-1"></a>Événement External. OnColorChange (type 1)

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

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





