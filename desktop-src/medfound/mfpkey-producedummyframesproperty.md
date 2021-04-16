---
description: Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.
ms.assetid: dc09cecb-98c0-40bb-9e5d-f4661bf98522
title: MFPKEY_PRODUCEDUMMYFRAMES, propriété (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b40bdaa54b3dc14a2b4ef44235d7f87cab5b905
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202339"
---
# <a name="mfpkey_producedummyframes-property"></a>MFPKEY \_ propriété PRODUCEDUMMYFRAMES

Spécifie si l’encodeur génère des entrées de frame factice dans le flux binaire pour les frames en double.

## <a name="constant-for-ipropertybag"></a>Constante pour IPropertyBag

\_wszWMVCProduceDummyFrames g

## <a name="data-type"></a>Type de données

VT \_ bool

## <a name="default-value"></a>Valeur par défaut

VARIANTE \_ false

## <a name="remarks"></a>Notes

Si cette valeur est \_ false, le codec ne placera aucune donnée dans le flux binaire pour les trames dupliquées.

Les trames factices peuvent être importantes dans les applications où les numéros de trame sont conservés. C’est le cas, par exemple, lorsque les codes de temps SMPTE sont conservés pour le contenu encodé.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




