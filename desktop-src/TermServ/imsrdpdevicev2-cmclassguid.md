---
title: IMsRdpDeviceV2 propriété CmClassGuid
description: Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété CmClassGuid
- Services Bureau à distance de la propriété CmClassGuid, interface IMsRdpDeviceV2
- Services Bureau à distance de l’interface IMsRdpDeviceV2, propriété CmClassGuid
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510729"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>IMsRdpDeviceV2 :: CmClassGuid, propriété

Contient le GUID de la classe d’installation de Configuration Manager pour l’appareil.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>Valeur de la propriété

GUID de la classe d’installation de Configuration Manager pour l’appareil.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7 avec SP1<br/>                                                          |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2 avec SP1<br/>                                             |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 est défini en tant que 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





