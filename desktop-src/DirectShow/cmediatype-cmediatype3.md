---
description: En savoir plus sur la méthode du constructeur CMediaType. CMediaType (mtype. h). Cette méthode utilise les paramètres’mtype’et’PHR'.
ms.assetid: b7d5264a-2a5f-4111-96bb-1ea2b13405be
title: CMediaType. CMediaType, constructeur (mtype. h)-mtype et PHR, paramètres
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaType.CMediaType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0c399073794f025122e1cfade3f15b3a96784f28e171482e4dcfb7bcec6a8271
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084479"
---
# <a name="cmediatypecmediatype-constructor-mtypeh---mtype-and-phr-parameters"></a>CMediaType. CMediaType, constructeur (mtype. h)-mtype et PHR, paramètres

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaType(
  [ref] const AM_MEDIA_TYPE &mtype,
              HRESULT       *phr = NULL
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*mtype* \[ Réf\]
</dt> <dd>

Référence à une structure de [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) . Le constructeur copie le type de média vers le nouvel objet, y compris le bloc de format, le cas échéant.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur HRESULT. Ce paramètre peut être un pointeur **null** . Dans le cas contraire, l’appelant doit définir la valeur sur S \_ OK avant d’appeler le constructeur. Si le constructeur échoue, il définit la valeur sur un code d’échec.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le constructeur appelle la méthode [**CMediaType :: InitMediaType**](cmediatype-initmediatype.md) pour initialiser le type de média.

## <a name="requirements"></a>Configuration requise

| Condition requise                   | Valeur                                                                                                                                                                                           |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête  | Mtype. h (include Flux. h)                                                                                     |
| Bibliothèque | Strmbase. lib (versions commerciales); Strmbasd. lib (versions Debug) |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaType, classe**](cmediatype.md)
</dt> </dl>

 

 




