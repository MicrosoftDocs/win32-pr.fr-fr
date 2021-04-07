---
title: Interface IWMDRMNonSilentLicenseAquisition
description: L’interface IWMDRMNonSilentLicenseAquisition fournit des méthodes qui permettent d’acquérir une licence nécessitant l’intervention de l’utilisateur. Cette interface peut être obtenue en effectuant une acquisition de licence non silencieuse.
ms.assetid: 57dc3daa-d457-49b0-b589-a72ba180e75e
keywords:
- Format Windows Media de l’interface IWMDRMNonSilentLicenseAquisition
- Interface IWMDRMNonSilentLicenseAquisition format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMNonSilentLicenseAquisition
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89fce7764b755231812c761778131c159ddd860b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728709"
---
# <a name="iwmdrmnonsilentlicenseaquisition-interface"></a>Interface IWMDRMNonSilentLicenseAquisition

L’interface **IWMDRMNonSilentLicenseAquisition** fournit des méthodes qui permettent d’acquérir une licence nécessitant l’intervention de l’utilisateur.

Cette interface peut être obtenue en effectuant une acquisition de licence non silencieuse. Une fois que vous avez appelé [**IWMDRMLicenseManagement :: AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) , un événement **MEWMDRMLicenseAcquisitionCompleted** est généré. Appelez la méthode **IMFMediaEvent :: GetValue** de l’événement pour obtenir un pointeur vers une interface **IUnknown** qui peut être interrogée pour obtenir un pointeur vers une instance de cette interface.

## <a name="members"></a>Membres

L’interface **IWMDRMNonSilentLicenseAquisition** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMNonSilentLicenseAquisition** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMNonSilentLicenseAquisition** possède ces méthodes.



| Méthode                                                                | Description                                                                             |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| [**GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) | Récupère le problème de licence qui doit être publié sur le serveur de licences.<br/> |
| [**GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md)             | Récupère l’URL vers laquelle la demande de licence doit être publiée.<br/>           |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**Acquisition de licence non silencieuse**](non-silent-license-acquisition.md)
</dt> </dl>

 

