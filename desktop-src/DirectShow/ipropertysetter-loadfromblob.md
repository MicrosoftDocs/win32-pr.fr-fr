---
description: La méthode LoadFromBlob charge les données de propriété à partir d’un format de persistance.
ms.assetid: b314a844-2190-469a-a030-4494e2140ce6
title: 'IPropertySetter :: LoadFromBlob, méthode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPropertySetter.LoadFromBlob
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 7deaae82157baf0509f82258d114638b9db501647ad74aaed3ea344c063c5875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397540"
---
# <a name="ipropertysetterloadfromblob-method"></a>IPropertySetter :: LoadFromBlob, méthode

> [!Note]  
> \[Action déconseillée. Cette API peut être supprimée des futures versions de Windows.\]

 

La `LoadFromBlob` méthode charge des données de propriété à partir d’un format de persistance.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT LoadFromBlob(
  [in] LONG cSize,
  [in] BYTE *pb
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*cSize* \[ dans\]
</dt> <dd>

Taille des données, en octets.

</dd> <dt>

*PB* \[ dans\]
</dt> <dd>

Pointeur vers un tableau d’octets qui contient les données.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interface IPropertySetter**](ipropertysetter.md)
</dt> <dt>

[Codes d’erreur et de réussite](error-and-success-codes.md)
</dt> </dl>

 

 




