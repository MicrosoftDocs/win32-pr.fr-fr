---
description: L’interface IWiaDevMgr2 est utilisée pour créer et gérer des appareils d’acquisition d’images et pour s’inscrire afin de recevoir des événements d’appareil.
ms.assetid: 0e9fb3a1-bbe3-4dba-ba8c-b79f202d5a38
title: Interface IWiaDevMgr2 (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1dd73733d77c80ba4f3880464000f823e0e35092
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127231072"
---
# <a name="iwiadevmgr2-interface"></a>Interface IWiaDevMgr2

L’interface **IWiaDevMgr2** est utilisée pour créer et gérer des appareils d’acquisition d’images et pour s’inscrire afin de recevoir des événements d’appareil.

## <a name="members"></a>Membres

L’interface **IWiaDevMgr2** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaDevMgr2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaDevMgr2** possède ces méthodes.



| Méthode                                                                                    | Description                                                                                                                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateDevice**](-wia-iwiadevmgr2-createdevice.md)                                     | Crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour un appareil WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                 |
| [**EnumDeviceInfo**](-wia-iwiadevmgr2-enumdeviceinfo.md)                                 | Crée un énumérateur d’informations de propriété pour chaque appareil WIA 2,0 disponible. <br/>                                                                                                                                                                                                                                                                                                                 |
| [**GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md)                                       | La méthode [**IWiaDevMgr2 :: GetImageDlg**](-wia-iwiadevmgr2-getimagedlg.md) affiche une ou plusieurs boîtes de dialogue qui permettent à un utilisateur d’acquérir une image à partir d’un appareil WIA 2,0 et d’écrire l’image dans un fichier spécifié. Cette méthode étend les fonctionnalités de [**IWiaDevMgr2 :: SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) pour encapsuler l’acquisition d’images dans un seul appel d’API. <br/> |
| [**RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)         | La méthode [**IWiaDevMgr2 :: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md) inscrit une application pour recevoir des événements même si l’application n’est pas en cours d’exécution.<br/>                                                                                                                                                                                                      |
| [**RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md) | Inscrit une application en cours d’exécution pour la notification d’événements WIA 2,0. <br/>                                                                                                                                                                                                                                                                                                                                  |
| [**RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)     | La méthode [**IWiaDevMgr2 :: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md) inscrit une application pour recevoir des événements d’appareil. Il est principalement fourni pour la compatibilité descendante avec les applications qui n’ont pas été écrites pour WIA 2,0.<br/>                                                                                                                         |
| [**SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md)                               | Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images. <br/>                                                                                                                                                                                                                                                                                                   |
| [**SelectDeviceDlgID**](-wia-iwiadevmgr2-selectdevicedlgid.md)                           | Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images. <br/>                                                                                                                                                                                                                                                                                                   |



 

## <a name="remarks"></a>Notes

L’interface **IWiaDevMgr2** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
