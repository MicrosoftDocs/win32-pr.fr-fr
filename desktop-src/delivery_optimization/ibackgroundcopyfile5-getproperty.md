---
title: IBackgroundCopyFile5 GetProperty, méthode (Deliveryoptimization. h)
description: Obtient une propriété générique d’un transfert de fichiers d’optimisation de la remise.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty, méthode
- Méthode GetProperty, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, méthode GetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a664c752bd28b176189cdd77e955684236cfa23c6b384378610336335651fad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119635949"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5 :: GetProperty, méthode

Obtient une propriété générique d’un transfert de fichiers d’optimisation de la remise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyId* \[ dans\]
</dt> <dd>

Spécifie la propriété de fichier dont la valeur doit être récupérée.

</dd> <dt>

*PropertyValue* \[ à\]
</dt> <dd>

Valeur de la propriété, retournée en tant que pointeur vers une BITS_FILE_PROPERTY_VALUE Union. Utilisez le champ Union correspondant à la valeur de l’ID de propriété passée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne **S_OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 est défini en tant que 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





