---
description: La méthode DecideBufferSize définit les exigences de mémoire tampon de la broche de sortie.
ms.assetid: f1ddc39e-dcd5-4a44-8a8e-e384692408e1
title: Méthode CTransInPlaceFilter. DecideBufferSize (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 55227510eee3c1afdcd14ed390edf21eccfcf1de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535923"
---
# <a name="ctransinplacefilterdecidebuffersize-method"></a>Méthode CTransInPlaceFilter. DecideBufferSize

La `DecideBufferSize` méthode définit les exigences de mémoire tampon de la broche de sortie.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *pProperties
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pAlloc* 
</dt> <dd>

Pointeur vers l’objet [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) utilisé par la broche de sortie.

</dd> <dt>

*pProperties* 
</dt> <dd>

Pointeur vers les propriétés d’allocateur demandées pour le nombre, la taille et l’alignement, comme spécifié par la structure des [**\_ Propriétés de l’allocateur**](/windows/win32/api/strmif/ns-strmif-allocator_properties) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur **HRESULT** . Les valeurs possibles sont les suivantes :



| Code de retour                                                                            | Description        |
|----------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**\_OK**</dt> </dl>   | Succès<br/> |
| <dl> <dt>**E \_ échec**</dt> </dl> | Échec<br/> |



 

## <a name="remarks"></a>Notes

Cette méthode est appelée lorsque la classe **CTransInPlaceFilter** doit fournir une taille de mémoire tampon au filtre en aval. Si le filtre **CTransInPlaceFilter** est déjà connecté en amont, il utilise les propriétés Allocator sur la connexion de code confidentiel amont. Dans le cas contraire, elle définit la taille de la mémoire tampon sur 1 octet comme valeur de détenteur temporaire. Lorsque le filtre amont se connecte, la classe **CTransInPlaceFilter** renégocie l’allocateur en aval. Pour plus d’informations sur le processus de connexion de code confidentiel dans cette classe, consultez [**CTransInPlaceFilter, classe**](ctransinplacefilter.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




