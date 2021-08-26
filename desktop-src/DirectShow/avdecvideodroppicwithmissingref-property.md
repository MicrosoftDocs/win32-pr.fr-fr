---
description: Spécifie si le décodeur supprime les trames intra avec des frames de référence manquants.
ms.assetid: 9007d5a8-f498-4394-a4e6-02a7616f3e2a
title: Propriété AVDecVideoDropPicWithMissingRef (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2ac5e8c02c63c977d8d5a8e47bb5d6f878c538364ac2fe5b65c1e691c84ca23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000319"
---
# <a name="avdecvideodroppicwithmissingref-property"></a>Propriété AVDecVideoDropPicWithMissingRef

Spécifie si le décodeur supprime les trames intra avec des frames de référence manquants.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**Variante \_ BOOL** (**VT \_ bool**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoDropPicWithMissingRef**

## <a name="remarks"></a>Remarques

Si le flux binaire est endommagé, il est possible qu’il manque des frames de référence dans une trame. Si la valeur de cette propriété est **\_ true**, le décodeur supprime le frame. Si la valeur est **\_ false**, le décodeur tente de décoder le frame, en utilisant un ou plusieurs frames proches comme frames de référence. L’image décodée résultante aura des artefacts de blocage.

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

 

 




