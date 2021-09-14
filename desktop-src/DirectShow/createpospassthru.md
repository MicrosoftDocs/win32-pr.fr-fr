---
description: La fonction CreatePosPassThru crée un objet CPosPassThru ou un objet CRendererPosPassThru.
ms.assetid: d6fccfb4-b256-40aa-b927-84c7a886f631
title: CreatePosPassThru, fonction (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreatePosPassThru
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08735a0bac2cc5aa8f5bb61461f10097435ad9c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006690"
---
# <a name="createpospassthru-function"></a>CreatePosPassThru fonction)

La `CreatePosPassThru` fonction crée un objet [**CPosPassThru**](cpospassthru.md) ou un objet [**CRendererPosPassThru**](crendererpospassthru.md) .

## <a name="syntax"></a>Syntaxe


```C++
STDAPI CreatePosPassThru(
   LPUNKNOWN pAgg,
   BOOL      bRenderer,
   IPin      *pPin,
   IUnknown  **ppPassThru
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAgg* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*bRenderer* 
</dt> <dd>

Valeur booléenne qui spécifie si le filtre est un convertisseur. Utilisez la valeur **true** si le filtre est un convertisseur, ou **false** dans le cas contraire. Si la valeur est **true**, cette méthode crée une instance de la classe [**CRendererPosPassThru**](crendererpospassthru.md) . Si la valeur est **false**, la méthode crée une instance de la classe **CPosPassThru** .

</dd> <dt>

*pPin* 
</dt> <dd>

Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) sur la broche d’entrée du filtre.

</dd> <dt>

*ppPassThru* 
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers l’interface **IUnknown** de l’objet.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne S \_ OK en cas de réussite. Sinon, retourne une valeur **HRESULT** indiquant la cause de l’erreur.

## <a name="remarks"></a>Notes

Cette méthode utilise l’interface [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru) pour créer l’objet. L’objet est chargé dynamiquement à partir de Quartz.dll.

Si la fonction est réussie, l’interface **IUnknown** retournée a un nombre de références en attente. L’appelant doit libérer l’interface.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Ctlutil. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CPosPassThru, classe**](cpospassthru.md)
</dt> </dl>

 

 




