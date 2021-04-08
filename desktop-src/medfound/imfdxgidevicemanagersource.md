---
description: Fournit les fonctionnalités permettant d’obtenir le IMFDXGIDeviceManager à partir du récepteur de rendu vidéo Microsoft Media Foundation.
ms.assetid: 80078ed6-61cc-4fb9-8fd5-eda78cd5be30
title: Interface IMFDXGIDeviceManagerSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMFDXGIDeviceManagerSource
api_type:
- COM
api_location:
- mfidl.h
ms.openlocfilehash: 669ec840a3122172147840052bd1dbf5c940569d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753189"
---
# <a name="imfdxgidevicemanagersource-interface"></a>Interface IMFDXGIDeviceManagerSource

Fournit les fonctionnalités permettant d’obtenir le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Microsoft Media Foundation.

## <a name="members"></a>Membres

L’interface **IMFDXGIDeviceManagerSource** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IMFDXGIDeviceManagerSource** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IMFDXGIDeviceManagerSource** possède ces méthodes.



| Méthode                                                      | Description                                                                                                              |
|:------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------|
| [**GetManager**](imfdxgidevicemanagersource-getmanager.md) | Obtient le [**IMFDXGIDeviceManager**](/windows/desktop/api/mfobjects/nn-mfobjects-imfdxgidevicemanager) à partir du récepteur de rendu vidéo Media Foundation.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                       |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
