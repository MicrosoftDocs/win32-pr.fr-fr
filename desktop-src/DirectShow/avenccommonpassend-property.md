---
description: Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.
ms.assetid: 847f638f-9ab9-42ca-8e39-82c113cee92f
title: Propriété AVEncCommonPassEnd (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02faeb9d78f10b962b7134fd316bda348b0f03e1a82ace210956c2243231df19
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873369"
---
# <a name="avenccommonpassend-property"></a>Propriété AVEncCommonPassEnd

Arrête le passage de l’encodage en cours ou interroge si le passage de l’encodage actuel est le dernier.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonPassEnd**

## <a name="remarks"></a>Remarques

L’affectation de la **\_ valeur variant** à cette propriété met fin à la passe d’encodage en cours. L’affectation de la **\_ valeur false** à cette propriété met fin à l’encodage multipasse.

La lecture de cette propriété demande si le passage de l’encodage actuel est le dernier.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




