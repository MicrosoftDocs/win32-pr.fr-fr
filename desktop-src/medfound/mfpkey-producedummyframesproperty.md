---
description: Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: MFPKEY_PRODUCEDUMMYFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cb8f186c885e9cc150ab194bdadd01403a37b423b30bf6009b173819d27dfa9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939889"
---
# <a name="mfpkey_producedummyframes-property"></a>MFPKEY \_ propriété PRODUCEDUMMYFRAMES

Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCProduceDummyFrames g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ false

## <a name="remarks"></a>Remarques

Si cette valeur est \_ false, le codec ne placera aucune donnée dans le flux binaire pour les trames dupliquées.

Les trames factices peuvent être importantes dans les applications où les numéros de trame sont conservés. C’est le cas, par exemple, lorsque les codes de temps SMPTE sont conservés pour le contenu encodé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




