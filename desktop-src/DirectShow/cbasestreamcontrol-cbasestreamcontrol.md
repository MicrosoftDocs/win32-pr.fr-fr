---
description: Méthode constructeur CBaseStreamControl. CBaseStreamControl.
ms.assetid: c0eff80f-04d3-4919-bb27-1b76c1bd1cce
title: Constructeur CBaseStreamControl. CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl.CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4c6521bec65e0182b8eb48eb5d3efe9ea609c6a7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923780"
---
# <a name="cbasestreamcontrolcbasestreamcontrol-constructor"></a>Constructeur CBaseStreamControl. CBaseStreamControl

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CBaseStreamControl(
   HRESULT *phr
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*phr* 
</dt> <dd>

Pointeur vers une valeur **HRESULT** . Si le constructeur échoue, ce paramètre reçoit un code d’erreur. Si cela se produit, l’état de l’objet n’est pas valide.

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Strmctl. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CBaseStreamControl, classe**](cbasestreamcontrol.md)
</dt> </dl>

 

 




