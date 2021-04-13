---
title: Méthode IBackgroundCopyFile GetProgress (Deliveryoptimization. h)
description: Récupère des informations sur la progression du transfert de fichiers.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- Méthode GetProgress
- Méthode GetProgress, interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, méthode GetProgress
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465079"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a>IBackgroundCopyFile :: GetProgress, méthode

Récupère des informations sur la progression du transfert de fichiers.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*pProgress* \[ à\]
</dt> <dd>

Structure dont les membres indiquent la progression du transfert de fichier. Pour plus d’informations sur le type d’informations de progression disponibles, consultez la structure [**BG_FILE_PROGRESS**](bg-file-progress.md) .

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
| IID<br/>                      | IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BG_FILE_PROGRESS**](bg-file-progress.md)
</dt> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetProgress**](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





