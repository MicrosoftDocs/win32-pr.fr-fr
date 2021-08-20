---
title: Interface IWMDRMNetTransmitter
description: l’interface IWMDRMNetTransmitter fournit les méthodes nécessaires pour utiliser Windows DRM de média pour les périphériques réseau comme émetteur. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMNetTransmitter comme paramètre riid.
ms.assetid: e93db52a-8829-4d16-b839-824e34b3e582
keywords:
- Format Windows Media de l’interface IWMDRMNetTransmitter
- Interface IWMDRMNetTransmitter format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7526ad349403abdb74f1e5684356af1b51b91f99b40e8e26a3b04932d4e5cf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027557"
---
# <a name="iwmdrmnettransmitter-interface"></a>Interface IWMDRMNetTransmitter

l’interface **IWMDRMNetTransmitter** fournit les méthodes nécessaires pour utiliser Windows DRM de média pour les périphériques réseau comme émetteur.

Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md). Transmettez **IID \_ IWMDRMNetTransmitter** comme paramètre *riid* .

## <a name="members"></a>Membres

L’interface **IWMDRMNetTransmitter** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNetTransmitter** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMNetTransmitter** possède ces méthodes.



| Méthode                                                                        | Description                                                                                                 |
|:------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) | Génère un message de réponse de licence feuille.<br/>                                                       |
| [**GetRootLicenseResponse**](iwmdrmnettransmitter-getrootlicenseresponse.md) | Génère un message de réponse de la licence racine<br/>                                                        |
| [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)       | traite un challenge de licence envoyé par un récepteur Microsoft Windows Media DRM pour les périphériques réseau.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Interface IWMDRMNetReceiver**](iwmdrmnetreceiver.md)
</dt> </dl>

 

