---
description: Méthode constructeur CSeekingPassThru. CSeekingPassThru.
ms.assetid: e31253fc-b365-4414-9dee-906d4c41d16e
title: Constructeur CSeekingPassThru. CSeekingPassThru (Seekpt. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru.CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cab9d6329f5175c96a3bfc5962ca5a555fe62b5d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085377"
---
# <a name="cseekingpassthrucseekingpassthru-constructor"></a>Constructeur CSeekingPassThru. CSeekingPassThru

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CSeekingPassThru(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Chaîne contenant le nom de l’objet. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md) .

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Ignoré.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Seekpt. h (include streams. h)</dt> </dl>                                                                                    |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CSeekingPassThru, classe**](cseekingpassthru.md)
</dt> </dl>

 

 




