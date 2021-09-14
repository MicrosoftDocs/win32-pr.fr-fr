---
description: Méthode constructeur CBaseControlVideo. CBaseControlVideo.
ms.assetid: 925c6c45-0990-4044-aca1-34f343f438b5
title: Constructeur CBaseControlVideo. CBaseControlVideo (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.CBaseControlVideo
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 389c05b5254326d2966799b857107e79792610e9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127225049"
---
# <a name="cbasecontrolvideocbasecontrolvideo-constructor"></a>Constructeur CBaseControlVideo. CBaseControlVideo

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseControlVideo(
   CBaseFilter *pFilter,
   CCritSec    *pInterfaceLock,
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pFilter* 
</dt> <dd>

Pointeur vers l’objet de filtre de média propriétaire.

</dd> <dt>

*pInterfaceLock* 
</dt> <dd>

Pointeur vers la section critique à utiliser pour le verrouillage.

</dd> <dt>

*pName* 
</dt> <dd>

Pointeur vers la description de l’objet.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers l’interface de contrôle **IUnknown** , si l’objet fait partie d’un agrégat ; dans le cas contraire, doit avoir la **valeur null**.

</dd> <dt>

*phr* 
</dt> <dd>

Pointeur vers une variable qui reçoit une valeur HRESULT indiquant la réussite ou l’échec de la méthode de constructeur.

</dd> </dl>

## <a name="remarks"></a>Notes

L’objet implémente l’interface de contrôle [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) .

Toutes les méthodes d’interface de [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) implémentées par cette classe requièrent que le filtre soit correctement connecté. Pour cette raison, la classe reçoit un code confidentiel avec lequel elle doit se synchroniser. Chaque fois qu’une méthode d’interface est appelée, l’objet détermine que le pin est toujours connecté.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseControlVideo, classe**](cbasecontrolvideo.md)
</dt> </dl>

 

 




