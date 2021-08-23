---
description: Méthode constructeur CTransInPlaceFilter. CTransInPlaceFilter.
ms.assetid: f0d30125-5d16-470c-a5fb-a7df96814dad
title: Constructeur CTransInPlaceFilter. CTransInPlaceFilter (Transip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.CTransInPlaceFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98fb678a2df7c79e40c5ecf39b0a059ebc9e44f4f3f603e1d1a6551446204aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767579"
---
# <a name="ctransinplacefilterctransinplacefilter-constructor"></a>Constructeur CTransInPlaceFilter. CTransInPlaceFilter

Méthode de constructeur.

## <a name="syntax"></a>Syntaxe


```C++
CTransInPlaceFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   REFCLSID  clsid,
   HRESULT   *phr,
   bool      bModifiesData = TRUE
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pObjectName* 
</dt> <dd>

Chaîne contenant le nom de débogage du filtre. Pour plus d’informations, consultez [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Pointeur vers le propriétaire de cet objet. Si l’objet est agrégé, passer un pointeur vers l’interface **IUnknown** de l’objet d’agrégation. Sinon, affectez la valeur **null** à ce paramètre.

</dd> <dt>

*identificateur* 
</dt> <dd>

Identificateur de classe du filtre.

</dd> <dt>

*phr* 
</dt> <dd>

Ignoré.

</dd> <dt>

*bModifiesData* 
</dt> <dd>

Valeur booléenne qui spécifie si le filtre modifie les données d’entrée. Si la **valeur est true**, le filtre modifie les données. Dans le cas contraire, le filtre passe les données en aval inchangées.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Transip. h (inclure Flux. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CTransInPlaceFilter, classe**](ctransinplacefilter.md)
</dt> </dl>

 

 




