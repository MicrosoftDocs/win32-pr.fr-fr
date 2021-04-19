---
description: Obtient le IMFDXGIDeviceManager à partir du récepteur de rendu vidéo Microsoft Media Foundation.
ms.assetid: 809e89e4-3ed5-4dba-82dc-4ec217b8ef38
title: 'IMFDXGIDeviceManagerSource :: GetManager, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource.GetManager
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 098810e9e06f339b1035748d71f46c7af26e96a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524612"
---
# <a name="imfdxgidevicemanagersourcegetmanager-method"></a>IMFDXGIDeviceManagerSource :: GetManager, méthode

Obtient le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Microsoft Media Foundation.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT GetManager(
  [out] IMFDXGIDeviceManager **ppManager
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ppManager* \[ à\]
</dt> <dd>

Objet [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si cette méthode est réussie, elle retourne la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                       |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMFDXGIDeviceManagerSource**](imfdxgidevicemanagersource.md)
</dt> </dl>

 

 




