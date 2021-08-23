---
title: IBackgroundCopyFile5 SetProperty, méthode (Deliveryoptimization. h)
description: Définit une propriété générique d’un transfert de fichiers d’optimisation de la remise.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty (méthode)
- SetProperty, méthode, interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, méthode SetProperty
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 10da7fff9066ccefe7c356e3577ffffe7b0fc2e89d5fdb3f74611f5621d5b757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755599"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a>IBackgroundCopyFile5 :: SetProperty, méthode

Définit une propriété générique d’un transfert de fichiers d’optimisation de la remise.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*PropertyId* \[ dans\]
</dt> <dd>

Spécifie la propriété à définir.

</dd> <dt>

*ProertyValue* \[ à\]
</dt> <dd>

Pointeur vers une Union qui spécifie la valeur à définir. Le membre d’Union approprié pour l’ID de propriété est utilisé.

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

[**IBackgroundCopyFile5. GetProperty**](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





