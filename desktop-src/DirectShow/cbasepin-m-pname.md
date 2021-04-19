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
ms.openlocfilehash: f2580b9aba379362c39e3d792504434fa18fe076
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106533181"
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
| En-tête<br/> | <dl> <dt>Amfilter. h (include streams. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBasePin, classe**](cbasepin.md)
</dt> </dl>

 

 




