---
description: En savoir plus sur la méthode IAMFilterData ::P arseFilterData, décompresse les données de Registre binaires pour un filtre. Cette interface a été déconseillée.
ms.assetid: 86095fcf-3364-42a0-95db-08223fa3cc20
title: IAMFilterData ::P méthode arseFilterData (fil \_ Data. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.ParseFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 9560280fa6f16699af907cdb5cf682b9c4bb1277
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127234132"
---
# <a name="iamfilterdataparsefilterdata-method"></a>IAMFilterData ::P méthode arseFilterData

> [!Note]  
> Cette interface a été déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

La `ParseFilterData` méthode décompresse les données de Registre binaires pour un filtre.

Il n’y a généralement aucune raison pour qu’une application appelle cette méthode. La méthode [**IFilterMapper2 :: EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters) offre un moyen plus pratique d’accéder aux données de registre de filtre.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT ParseFilterData(
  [in]  BYTE  *rgbFilterData,
  [in]  ULONG cb,
  [out] BYTE  **prgbRegFilter2
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*rgbFilterData* \[ dans\]
</dt> <dd>

Pointeur vers les données de Registre binaires. Vous pouvez récupérer ces données en extrayant la propriété « FilterData » du moniker de filtre. Les données sont stockées sous la forme d’un **SAFEARRAY** d’octets ( \_ tableau VT UI1 \| VT \_ ).

</dd> <dt>

*CB* \[ dans\]
</dt> <dd>

Spécifie la taille des données binaires, en octets.

</dd> <dt>

*prgbRegFilter2* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers les données décompressées. Lorsque la méthode retourne, effectuez un cast de ce pointeur vers un type [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) pour accéder aux données de filtre. L’appelant doit libérer la mémoire en appelant la méthode **CoTaskMemFree** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d'échec, retourne un code d'erreur.

## <a name="remarks"></a>Notes

> [!Note]  
> l’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Données de fil \_ . h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




