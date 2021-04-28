---
description: Méthode constructeur CMediaControl. CMediaControl.
ms.assetid: 00549dfe-5dd4-445e-bad3-eb6bcfea8f5f
title: Constructeur CMediaControl. CMediaControl (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaControl.CMediaControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96775678a8d182a3dc88f25fc19b194367c57d92
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099207"
---
# <a name="cmediacontrolcmediacontrol-constructor"></a>Constructeur CMediaControl. CMediaControl

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CMediaControl(
   const TCHAR     *pName,
         LPUNKNOWN pUnk
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pName* 
</dt> <dd>

Pointeur vers le nom de l’objet à des fins de débogage.

</dd> <dt>

*pUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet.

</dd> </dl>

## <a name="remarks"></a>Notes 

Allouez le paramètre *pname* dans la mémoire statique. Ce nom apparaît sur le terminal de débogage lors de la création et de la suppression de l’objet.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CMediaControl, classe**](cmediacontrol.md)
</dt> </dl>

 

 




