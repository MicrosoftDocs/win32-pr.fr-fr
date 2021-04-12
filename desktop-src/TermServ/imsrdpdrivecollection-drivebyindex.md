---
title: IMsRdpDriveCollection propriété DriveByIndex
description: Récupère le lecteur à l’index spécifié.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveByIndex
- Services Bureau à distance de la propriété DriveByIndex, interface IMsRdpDriveCollection
- Services Bureau à distance de l’interface IMsRdpDriveCollection, propriété DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384983"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a>IMsRdpDriveCollection ::D propriété riveByIndex

Récupère le lecteur à l’index spécifié.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a>Valeur de la propriété

Pointeur d’interface [**IMsRdpDrive**](imsrdpdrive.md) .

## <a name="error-codes"></a>Codes d’erreur

Si la méthode est réussie, **S \_ OK** est retourné. Toute autre valeur **HRESULT** indique que l’appel a échoué.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsRdpDriveCollection est défini en tant que 7ff17599-da2c-4677-ad35-f60c04fe1585<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDriveCollection**](imsrdpdrivecollection.md)
</dt> </dl>

 

 





