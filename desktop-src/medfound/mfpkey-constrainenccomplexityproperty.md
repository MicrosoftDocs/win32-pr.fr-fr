---
description: Spécifie si la complexité de l’algorithme d’encodage audio est restreinte.
ms.assetid: a50b840f-9fe8-4291-b93f-f09c241fe802
title: MFPKEY_CONSTRAINENCOMPLEXITY, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdc6e3d5a7077c72e5933ecbc235092174e263fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534205"
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

Si vous laissez cette propriété à sa valeur par défaut **Variant \_ false**, l’encodeur audio utilise son algorithme par défaut. L’algorithme par défaut dépend du type de sortie et de la version de Windows en cours d’exécution. Le tableau suivant décrit le comportement par défaut pour les différentes combinaisons.



| Système d’exploitation | Comportement par défaut                                                                                                                                                                                    |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Windows Vista    | Pour tous les types de sortie, l’encodeur audio utilise par défaut l’algorithme le plus complexe.                                                                                                                 |
| Windows 7        | Pour les types de sortie standard et Professional, l’encodeur audio utilise l’algorithme le plus complexe par défaut. Pour les types de sortie sans perte, l’encodeur audio utilise l’algorithme le moins complexe par défaut. |



 

Si vous affectez à cette propriété la valeur **Variant \_ true**, vous devez également spécifier une valeur de complexité en définissant la propriété [**MFPKEY \_ ENCCOMPLEXITY**](mfpkey-enccomplexityproperty.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 
