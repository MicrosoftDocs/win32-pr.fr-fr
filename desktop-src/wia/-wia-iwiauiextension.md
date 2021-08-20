---
description: L’interface IWiaUIExtension fournit des méthodes qui remplacent l’interface utilisateur système par défaut, fournissent un logo de bitmap d’appareil personnalisé et fournissent une icône d’appareil personnalisé.
ms.assetid: e3c69019-0e07-44ad-b48b-ea7e3daed2b7
title: Interface IWiaUIExtension (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: f2b83a1cd2638489ef0cf1a635ab32619597c395f0ca9b41d2ffaed80f59c228
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118034930"
---
# <a name="iwiauiextension-interface"></a>Interface IWiaUIExtension

L’interface **IWiaUIExtension** fournit des méthodes qui remplacent l’interface utilisateur système par défaut, fournissent un logo de bitmap d’appareil personnalisé et fournissent une icône d’appareil personnalisé.

## <a name="members"></a>Membres

L’interface **IWiaUIExtension** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaUIExtension** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaUIExtension** possède ces méthodes.



| Méthode                                                                  | Description                                                                                  |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**DeviceDialog**](-wia-iwiauiextension-devicedialog.md)               | Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.<br/> |
| [**GetDeviceBitmapLogo**](-wia-iwiauiextension-getdevicebitmaplogo.md) | Obtient un logo de bitmap personnalisé pour l’appareil.<br/>                                         |
| [**GetDeviceIcon**](-wia-iwiauiextension-getdeviceicon.md)             | Obtient une icône d’appareil personnalisé.<br/>                                                        |



 

## <a name="remarks"></a>Remarques



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wiadevd. h</dt> </dl> |



 

 
