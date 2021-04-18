---
description: Notez que cette interface est dépréciée.
ms.assetid: ab6972ef-7c28-4cd1-b007-eb70f9aeb2cb
title: 'IAMFilterData :: CreateFilterData, méthode (fil \_ Data. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData.CreateFilterData
api_type:
- COM
api_location:
- Quartz.dll
ms.openlocfilehash: 4c83f19de8e709f9890b23957f730fbbac12dd7d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540242"
---
# <a name="iamfilterdatacreatefilterdata-method"></a>IAMFilterData :: CreateFilterData, méthode

> [!Note]  
> Cette interface a été déconseillée. Les nouvelles applications ne doivent pas l’utiliser.

 

La `CreateFilterData` méthode crée des données de Registre binaires pour un filtre. Ces données peuvent être écrites dans le Registre sous la forme d’une \_ sous-clé binaire reg nommée FilterData, sous la clé CLSID du filtre.

Il n’y a généralement aucune raison pour qu’une application appelle cette méthode. La méthode [**IFilterMapper2 :: RegisterFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-registerfilter) crée automatiquement les données binaires et les ajoute à l’emplacement approprié dans le registre. Pour plus d’informations, consultez [comment inscrire des filtres DirectShow](how-to-register-directshow-filters.md).

## <a name="syntax"></a>Syntaxe


```C++
HRESULT CreateFilterData(
  [in]  REGFILTER2 *prf2,
  [out] BYTE       **prgbFilterData,
  [out] ULONG      *pcb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*prf2* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**REGFILTER2**](/windows/desktop/api/strmif/ns-strmif-regfilter2) qui contient les informations de filtre.

</dd> <dt>

*prgbFilterData* \[ à\]
</dt> <dd>

Adresse d’une variable qui reçoit un pointeur vers les données binaires. La méthode alloue la mémoire pour les données. L’appelant doit libérer la mémoire en appelant la méthode **CoTaskMemFree** .

</dd> <dt>

*PCB* \[ à\]
</dt> <dd>

Pointeur vers une variable qui reçoit la taille des données binaires, en octets.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la méthode est réussie, elle retourne la valeur \_ OK. En cas d'échec, retourne un code d'erreur.

## <a name="remarks"></a>Notes

> [!Note]  
> L’en-tête de \_ données. h se trouve dans le répertoire de l' [exemple du mappeur](mapper-sample.md) dans le SDK Windows.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Données de fil \_ . h</dt> </dl> |
| DLL<br/>    | <dl> <dt>Quartz.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IAMFilterData**](iamfilterdata.md)
</dt> </dl>

 

 




