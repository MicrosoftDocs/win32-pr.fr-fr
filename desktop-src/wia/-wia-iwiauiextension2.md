---
description: L’interface IWiaUIExtension2 fournit des méthodes qui remplacent la valeur par défaut, l’interface utilisateur fournie par le système par une interface utilisateur personnalisée, et qui fournissent une icône d’appareil personnalisée.
ms.assetid: 1a747ea3-2476-438b-baf0-903b86cbbb16
title: Interface IWiaUIExtension2 (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 2111c25a83a9b826f4cab7dba8f689e01a9868ac416b8fb3026f1b1fb49a90ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118208142"
---
# <a name="iwiauiextension2-interface"></a>Interface IWiaUIExtension2

L’interface IWiaUIExtension2 fournit des méthodes qui remplacent la valeur par défaut, l’interface utilisateur fournie par le système par une interface utilisateur personnalisée, et qui fournissent une icône d’appareil personnalisée. Les fournisseurs d’appareils peuvent implémenter cette interface pour fournir des interfaces utilisateur personnalisées pour leurs appareils.

## <a name="members"></a>Membres

L’interface **IWiaUIExtension2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaUIExtension2** possède ces méthodes.



| Méthode                                                       | Description                                                                                  |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension2-devicedialog.md)   | Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.<br/> |
| [**GetDeviceIcon**](-wia-iwiauiextension2-getdeviceicon.md) | Obtient une icône d’appareil personnalisé.<br/>                                                        |



 

## <a name="remarks"></a>Remarques



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
