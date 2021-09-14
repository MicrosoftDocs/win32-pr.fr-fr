---
description: Spécifie si la complexité de l’algorithme d’encodage audio est restreinte.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127227586"
---
# <a name="mfpkey_constrainencomplexity-property"></a>MFPKEY \_ propriété CONSTRAINENCOMPLEXITY

Spécifie si la complexité de l’algorithme d’encodage audio est restreinte.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

Disponible uniquement à l’aide de [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).

## <a name="data-type"></a>Type de données

**VT \_ bool**

## <a name="default-value"></a>Valeur par défaut

**VARIANTE \_ false**

## <a name="remarks"></a>Notes

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur audio utilise son algorithme par défaut. l’algorithme par défaut dépend du type de sortie et de la version de Windows est en cours d’exécution. Le tableau suivant décrit le comportement par défaut pour les différentes combinaisons.



| Système d'exploitation | Comportement par défaut                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Pour tous les types de sortie, l’encodeur audio utilise par défaut l’algorithme le plus complexe.                                                                                                                 |
| Windows 7        | pour les types de sortie Standard et Professional, l’encodeur audio utilise l’algorithme le plus complexe par défaut. Pour les types de sortie sans perte, l’encodeur audio utilise l’algorithme le moins complexe par défaut. |



 

Si vous affectez à cette propriété la valeur **Variant \_ true**, vous devez également spécifier une valeur de complexité en définissant la propriété [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
