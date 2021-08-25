---
title: Interface IWMDRMSecurity
description: L’interface IWMDRMSecurity gère diverses informations relatives à la sécurité pour l’ordinateur client et le sous-système de gestion des droits numériques (DRM). Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject.
ms.assetid: 9439aedc-359d-4b2c-a88c-7b0e8eacb5a0
keywords:
- Format Windows Media de l’interface IWMDRMSecurity
- Interface IWMDRMSecurity format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMSecurity
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31593dda35e7fa33540faa3c954f1901e1afa227372b25326c0f36154d443153
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839731"
---
# <a name="iwmdrmsecurity-interface"></a>Interface IWMDRMSecurity

L’interface **IWMDRMSecurity** gère diverses informations relatives à la sécurité pour l’ordinateur client et le sous-système de gestion des droits numériques (DRM).

Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md). Transmettez **IID \_ IWMDRMSecurity** comme paramètre *riid* .

## <a name="members"></a>Membres

L’interface **IWMDRMSecurity** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMSecurity** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMSecurity** possède ces méthodes.



| Méthode                                                                                      | Description                                                                                                      |
|:--------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**CheckCertForRevocation**](iwmdrmsecurity-checkcertforrevocation.md)                     | Détermine si un certificat a été révoqué.<br/>                                                    |
| [**GetContentEnablersForRevocations**](iwmdrmsecurity-getcontentenablersforrevocations.md) | Récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats révoqués.<br/> |
| [**GetContentEnablersFromHashes**](iwmdrmsecurity-getcontentenablersfromhashes.md)         | Récupère les interfaces d’activation du contenu qui permettent le renouvellement des composants en fonction de certificats hachés.<br/>  |
| [**GetMachineCertificate**](iwmdrmsecurity-getmachinecertificate.md)                       | Récupère le certificat de l’ordinateur du sous-système DRM sur l’ordinateur client.<br/>                        |
| [**GetRevocationData**](iwmdrmsecurity-getrevocationdata.md)                               | Récupère une liste de révocation de certificats à partir du magasin local.<br/>                                         |
| [**GetRevocationDataVersion**](iwmdrmsecurity-getrevocationdataversion.md)                 | Récupère le numéro de version d’une liste de révocation de certificats dans le magasin local.<br/>                     |
| [**GetSecurityVersion**](iwmdrmsecurity-getsecurityversion.md)                             | Récupère la version du sous-système DRM sur l’ordinateur client.<br/>                                    |
| [**PerformSecurityUpdate**](iwmdrmsecurity-performsecurityupdate.md)                       | Lance une mise à jour de sécurité pour le sous-système DRM sur l’ordinateur client.<br/>                              |
| [**SetRevocationData**](iwmdrmsecurity-setrevocationdata.md)                               | Définit une liste de révocation de certificats dans le magasin local.<br/>                                                |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Exemple d’individualisation DRM**](drm-individualization-example.md)
</dt> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





