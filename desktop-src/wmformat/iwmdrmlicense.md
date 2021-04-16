---
title: Interface IWMDRMLicense
description: L’interface IWMDRMLicense représente une liste d’une ou de plusieurs licences.
ms.assetid: afef7f9a-6621-4de7-bd40-3211c5c7ba09
keywords:
- Format Windows Media de l’interface IWMDRMLicense
- Interface IWMDRMLicense format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicense
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 918154b180ed95dce51224e6340a3ab18f432d18
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463375"
---
# <a name="iwmdrmlicense-interface"></a>Interface IWMDRMLicense

L’interface **IWMDRMLicense** représente une liste d’une ou de plusieurs licences.

## <a name="members"></a>Membres

L’interface **IWMDRMLicense** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicense** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMLicense** possède ces méthodes.



| Méthode                                                                                   | Description                                                                                                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanPersist**](iwmdrmlicense-canpersist.md)                                           | Interroge si la licence peut être rendue persistante dans un magasin de licences local.<br/>                                                                                                                                               |
| [**CreateDecryptor**](iwmdrmlicense-createdecryptor.md)                                 | Crée un objet déchiffreur à l’aide des paramètres de la licence actuelle.<br/>                                                                                                                                                   |
| [**CreateEncryptor**](iwmdrmlicense-createencryptor.md)                                 | Crée un objet chiffreur à l’aide des paramètres de la licence actuelle.<br/>                                                                                                                                                  |
| [**CreateSecureDecryptor**](iwmdrmlicense-createsecuredecryptor.md)                     | Crée un objet déchiffreur sécurisé. Le déchiffreur sécurisé diffère du déchiffreur normal en ce sens qu’il déchiffre le contenu, puis le chiffre à nouveau en fonction des paramètres spécifiés dans les paramètres de cette méthode.<br/> |
| [**GetAnalogVideoRestrictionLevels**](iwmdrmlicense-getanalogvideorestrictionlevels.md) | Récupère toutes les restrictions vidéo analogiques définies sur la licence actuelle.<br/>                                                                                                                                                     |
| [**GetInclusionList**](iwmdrmlicense-getinclusionlist.md)                               | Récupère la liste d’inclusion entière pour la licence ou la chaîne de licences actuelle.<br/>                                                                                                                                           |
| [**GetLicense**](iwmdrmlicense-getlicense.md)                                           | Récupère les données de licence en tant que Extensible Markup Language (XML) ou XMR (extensible Media Rights).<br/>                                                                                                                        |
| [**GetLicenseProperty**](iwmdrmlicense-getlicenseproperty.md)                           | Récupère une propriété de la licence actuelle.<br/>                                                                                                                                                                          |
| [**GetNext**](iwmdrmlicense-getnext.md)                                                 | Charge les informations relatives à la licence suivante dans la liste.<br/>                                                                                                                                                               |
| [**GetOutputProtectionLevels**](iwmdrmlicense-getoutputprotectionlevels.md)             | Récupère des informations sur tous les niveaux de protection de sortie (OPLs) attribués à la licence.<br/>                                                                                                                                |
| [**PersistLicense**](iwmdrmlicense-persistlicense.md)                                   | Enregistre la licence actuelle à partir du magasin temporaire dans le magasin de licences local permanent.<br/>                                                                                                                              |
| [**ResetEnumeration**](iwmdrmlicense-resetenumeration.md)                               | Réinitialise la liste de licences à son état d’origine.<br/>                                                                                                                                                                          |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

