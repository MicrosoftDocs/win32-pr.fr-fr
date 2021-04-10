---
title: Méthode ibackgroundcopyjob EnumFiles, méthode (Deliveryoptimization. h)
description: Récupère un pointeur d’interface IEnumBackgroundCopyFiles que vous utilisez pour énumérer les fichiers dans un travail.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles, méthode
- EnumFiles, méthode, interface méthode ibackgroundcopyjob
- Interface méthode ibackgroundcopyjob, méthode EnumFiles
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104074"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a>Méthode ibackgroundcopyjob :: EnumFiles, méthode

Récupère un pointeur d’interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que vous utilisez pour énumérer les fichiers dans un travail.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppEnumFiles* \[ à\]
</dt> <dd>

Pointeur d’interface [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) que vous utilisez pour énumérer les fichiers du travail. Libérez *ppEnumFiles* quand vous avez terminé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne **S_OK** en cas de réussite ou une des valeurs com **HRESULT** standard en cas d’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob est défini en tant que 37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





