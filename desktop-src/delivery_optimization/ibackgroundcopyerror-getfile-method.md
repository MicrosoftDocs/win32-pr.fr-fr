---
title: IBackgroundCopyError GetFile, méthode (Deliveryoptimization. h)
description: Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.
ms.assetid: 7E1DB3EE-0690-4D0E-BA98-70F5FBDCF12F
keywords:
- GetFile, méthode
- GetFile, méthode, interface IBackgroundCopyError
- Interface IBackgroundCopyError, méthode GetFile
topic_type:
- apiref
api_name:
- IBackgroundCopyError.GetFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b84396797378c77a6f774b4c63a3966b0d601b7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510533"
---
# <a name="ibackgroundcopyerrorgetfile-method"></a>IBackgroundCopyError :: GetFile, méthode

Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetFile(
  [out] IBackgroundCopyFile **ppFile
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppFile* \[ à\]
</dt> <dd>

Pointeur d’interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) dont les méthodes vous permettent de déterminer les noms de fichiers locaux et distants associés à l’erreur. Le paramètre *ppFile* a la valeur **null** si l’erreur n’est pas associée au fichier local ou distant. Lorsque vous avez terminé, libérez *ppFile*.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode retourne les valeurs **HRESULT** suivantes.



| Code de retour                                                                                                | Description                                                                                                    |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * * *</dt> </dl>                   | Un pointeur d’interface a été récupéré avec succès sur l’objet fichier.<br/>                                     |
| <dl> <dt>**DO_E_FILE_NOT_AVAILABLE**</dt> </dl> | L’erreur n’est pas associée à un fichier local ou distant. Le paramètre *ppFile* a la valeur **null**.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyError::GetError**](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





