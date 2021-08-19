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
ms.openlocfilehash: fbed5497bcebb3518c7f6a56646976cc01fbfebc501af4a08e861139311f4bc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096709"
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
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
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

 

 





