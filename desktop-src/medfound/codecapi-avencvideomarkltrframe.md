---
description: Marque le frame actuel comme un cadre LTR.
ms.assetid: D70A54D6-DA9B-40E5-B130-0AA9C5363DF0
title: CODECAPI_AVEncVideoMarkLTRFrame, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a377f30aec049bc5cbc850ea03ace9dcc640bd6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524628"
---
# <a name="codecapi_avencvideomarkltrframe-property"></a>CODECAPI \_ propriété AVEncVideoMarkLTRFrame

Marque le frame actuel comme un cadre LTR.

## <a name="data-type"></a>Type de données

**ULong** (VT \_ UI4)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoMarkLTRFrame**

## <a name="remarks"></a>Notes

**Encodeurs H. 264/AVC :**

La valeur de ce contrôle est la valeur de la syntaxe H. 264 *LongTermFramIdx* associée au frame actuel. Si le frame actuel n’est pas dans la couche de base, par exemple, l’élément de syntaxe *temporal \_ ID* n’est pas égal à 0, cette propriété s’applique au frame de couche de base suivant dans l’ordre de codage.

Cette propriété ne doit pas être appelée si un appel en attente pour marquer un frame LTR a été émis à l’aide de la \_ propriété CODECAPI AVEncVideoMarkLTRFrame et que l’encodeur n’a pas encore marqué un frame comme LTR. En d’autres termes, l’encodeur ne doit pas faire remonter les \_ demandes CODECAPI AVEncVideoMarkLTRFrame. Si une \_ demande CODECAPI AVEncVideoMarkLTRFrame est soumise alors qu’une autre \_ demande de AVEncVideoMarkLTRFrame CODECAPI est toujours en attente, la demande plus ancienne doit être supprimée.

La \_ propriété CODECAPI AVEncVideoMarkLTRFrame est dynamique et peut être définie au cours de la session d’encodage.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                   |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




