---
description: Nom du code confidentiel.
ms.assetid: 324cb8cc-7e57-43d0-9358-2683efc4fb1e
title: 'Membre CBasePin :: m_pName (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pName
api_type:
- HeaderDef
api_location:
- Amfilter.h
ms.openlocfilehash: d118ed76650b9ea580c0143ff4334a480d110c4a9d9531a23dda60c05c614630
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052679"
---
# <a name="cbasepinm_pname-member"></a>Membre CBasePin :: m \_ pname

Nom du code confidentiel.

## <a name="syntax"></a>Syntaxe


```C++
WCHAR *m_pName;
```



## <a name="remarks"></a>Notes

La méthode [**CBasePin :: QueryPinInfo**](cbasepin-querypininfo.md) retourne cette chaîne comme nom de code confidentiel, et la méthode [**CBasePin :: QueryId**](cbasepin-queryid.md) la retourne comme identificateur de code confidentiel. En général, toutefois, le nom du code confidentiel et l’identificateur du code confidentiel ne doivent pas nécessairement être identiques. L’identificateur de code confidentiel est utilisé pour la persistance des graphiques. Pour plus d’informations, consultez [**IBaseFilter :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|-----------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Amfilter. h (inclure Flux. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




