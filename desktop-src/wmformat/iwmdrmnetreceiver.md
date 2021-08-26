---
title: Interface IWMDRMNetReceiver
description: l’interface IWMDRMNetReceiver fournit les méthodes nécessaires pour utiliser Microsoft Windows DRM pour les périphériques réseau comme récepteur. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMNetReceiver comme paramètre riid.
ms.assetid: 29966260-c0aa-4e7e-b827-a872c7429333
keywords:
- Format Windows Media de l’interface IWMDRMNetReceiver
- Interface IWMDRMNetReceiver format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5cb917d7d229b81a6792461c506b2a6b50aaee2af3bd5f133e44273077924f86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930109"
---
# <a name="iwmdrmnetreceiver-interface"></a>Interface IWMDRMNetReceiver

l’interface **IWMDRMNetReceiver** fournit les méthodes nécessaires pour utiliser Microsoft Windows DRM pour les périphériques réseau comme récepteur.

Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md). Transmettez **IID \_ IWMDRMNetReceiver** comme paramètre *riid* .

## <a name="members"></a>Membres

L’interface **IWMDRMNetReceiver** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMNetReceiver** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMNetReceiver** possède ces méthodes.



| Méthode                                                                               | Description                                                                                                                     |
|:-------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**GetLicenseChallenge**](iwmdrmnetreceiver-getlicensechallenge.md)                 | Génère une demande de licence qui est envoyée à l’émetteur lors de la demande de contenu protégé.<br/>                     |
| [**GetRegistrationChallenge**](iwmdrmnetreceiver-getregistrationchallenge.md)       | Génère une demande d’inscription envoyée à l’émetteur lors de l’inscription ou de la revalidation du récepteur.<br/> |
| [**ProcessLicenseResponse**](iwmdrmnetreceiver-processlicenseresponse.md)           | Traite la réponse de licence envoyée par l’émetteur en réponse à une demande de licence.<br/>                              |
| [**ProcessRegistrationResponse**](iwmdrmnetreceiver-processregistrationresponse.md) | Traite la réponse d’inscription envoyée par l’émetteur en réponse à une demande d’inscription.<br/>                    |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> <dt>

[**Interface IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





