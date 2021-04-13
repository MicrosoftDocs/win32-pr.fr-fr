---
description: Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriété AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 026b20cf0c13536403e7ccf32b160e8c6fc08141
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482513"
---
# <a name="avenccommonpassend-property"></a>Propriété AVEncCommonPassEnd

Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Notes

L’affectation de la **\_ valeur variant** à cette propriété met fin à la passe d’encodage en cours. L’affectation de la **\_ valeur false** à cette propriété met fin à l’encodage multipasse.

La lecture de cette propriété demande si le passage de l’encodage actuel est le dernier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




