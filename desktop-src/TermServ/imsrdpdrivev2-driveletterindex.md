---
title: IMsRdpDriveV2 propriété DriveLetterIndex
description: Contient l’index de la lettre du lecteur.
ms.assetid: 9091d1c4-b97e-4e4c-9563-5a0b881ec250
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété DriveLetterIndex
- Services Bureau à distance de la propriété DriveLetterIndex, interface IMsRdpDriveV2
- Services Bureau à distance de l’interface IMsRdpDriveV2, propriété DriveLetterIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveV2.DriveLetterIndex
- IMsRdpDriveV2.get_DriveLetterIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10dc107eba84b0b0559ce711add4596040cf23423e0723855e2c0c9ef0de652a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119399659"
---
# <a name="imsrdpdrivev2driveletterindex-property"></a>IMsRdpDriveV2 ::D propriété riveLetterIndex

Contient l’index de la lettre du lecteur.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_DriveLetterIndex(
  [out, retval] ULONG *pDriveLetterIndex
);
```



## <a name="property-value"></a>Valeur de la propriété

Index de la lettre du lecteur. 0 = « A », 1 = « B », et ainsi de suite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 avec SP1<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDriveV2**](imsrdpdrivev2.md)
</dt> </dl>

 

 





