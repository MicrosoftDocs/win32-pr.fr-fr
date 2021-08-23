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
ms.openlocfilehash: fc8854bb0b406048d999324a034ebc62b100496c7cf4b5838733e9addd50d42f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000699"
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

 

 





