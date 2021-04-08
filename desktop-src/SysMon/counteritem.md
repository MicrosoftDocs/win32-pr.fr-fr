---
title: Objet CounterItem (Isysmon. h)
description: Utilisez cette classe pour récupérer le chemin d’accès et la valeur d’un compteur et pour spécifier la couleur utilisée pour représenter le compteur. Pour récupérer cet objet, appelez compteurs. Item.
ms.assetid: 76b69395-efd8-4321-b7ed-63daa46e2636
keywords:
- CounterItem, objet SysMon
- Description de l’objet CounterItem SysMon
topic_type:
- apiref
api_name:
- CounterItem
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df999e327591309f015d8720f61643625eced4d3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741916"
---
# <a name="counteritem-object"></a>Objet CounterItem

Utilisez cette classe pour récupérer le chemin d’accès et la valeur d’un compteur et pour spécifier la couleur utilisée pour représenter le compteur.

Pour récupérer cet objet, appelez [**compteurs. Item**](counters-item.md).

## <a name="members"></a>Membres

L’objet **CounterItem** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **CounterItem** a ces méthodes.



| Méthode                                             | Description                                                                    |
|:---------------------------------------------------|:-------------------------------------------------------------------------------|
| [**GetDataAt**](counteritem-getdataat.md)         | Récupère les données de compteur à partir d’un point spécifique dans le graphique linéaire.<br/> |
| [**GetStatistics**](counteritem-getstatistics.md) | Récupère les valeurs moyennes, maximales et minimales du compteur.<br/> |
| [**GetValue**](counteritem-getvalue.md)           | Récupère la dernière valeur du compteur.<br/>                            |



 

### <a name="properties"></a>Propriétés

L’objet **CounterItem** a ces propriétés.



| Propriété                                                  | Description                                                                     |
|:----------------------------------------------------------|:--------------------------------------------------------------------------------|
| [**Couleur**](counteritem-color.md)<br/>             | Récupère ou définit la couleur utilisée pour représenter sous forme de graphique la valeur de compteur.<br/>         |
| [**LineStyle**](counteritem-linestyle.md)<br/>     | Récupère ou définit le style de ligne utilisé pour représenter sous forme de graphique la valeur de compteur.<br/>    |
| [**D**](counteritem-path.md)<br/>               | Récupère le chemin d’accès du compteur.<br/>                                   |
| [**ScaleFactor**](counteritem-scalefactor.md)<br/> | Récupère ou définit le facteur d’échelle utilisé pour représenter sous forme de graphique la valeur de compteur.<br/>  |
| [**Sélectionné**](counteritem-selected.md)<br/>       | Récupère ou définit une valeur qui indique si le compteur est sélectionné.<br/> |
| [**Valeur**](counteritem-value.md)<br/>             | Récupère la valeur actuelle du compteur.<br/>                          |
| [**Parent**](counteritem-visible.md)<br/>         | Récupère ou définit une valeur qui indique si le compteur est graphique.<br/>  |
| [**Width**](counteritem-width.md)<br/>             | Récupère ou définit la largeur de ligne utilisée pour représenter sous forme de graphique la valeur de compteur.<br/>    |



 

## <a name="remarks"></a>Notes

La [**valeur**](counteritem-value.md) est la propriété par défaut de **CounterItem**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                            |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Isysmon. h</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>Sysmon. ocx</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Classes SYSMON](sysmon-classes.md)
</dt> </dl>

 

 





