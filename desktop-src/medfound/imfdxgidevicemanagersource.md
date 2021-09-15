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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413042"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[applications Windows 8.1 desktop apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 Applications de \[ Bureau R2 \| applications UWP\]<br/>                       |
| MIDL<br/>                      | <dl> <dt>Mfidl. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces Media Foundation](media-foundation-interfaces.md)
</dt> </dl>

 

 
