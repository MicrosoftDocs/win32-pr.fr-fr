---
title: Interfaces clientes DRM Microsoft Windows Media
description: Interfaces clientes DRM Microsoft Windows Media
ms.assetid: 27bbc33f-8102-4db2-bbc6-1a1da92bac80
keywords:
- Windows Media Format SDK, interfaces
- gestion des droits numériques (DRM), interfaces
- DRM (gestion des droits numériques), interfaces
- API étendues du client DRM, interfaces
- API étendues clientes, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b4e259ef5b8ef410db072a7f942d139f682bc90
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196007"
---
# <a name="microsoft-windows-media-drm-client-interfaces"></a>Interfaces clientes DRM Microsoft Windows Media

le tableau suivant décrit les interfaces prises en charge par les api clientes DRM Windows Media.



| Interface                                                                    | Description                                                                                                     |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IDRMStatusCallback**](idrmstatuscallback.md)                             | Fournit la définition d’un rappel d’État que vous pouvez implémenter pour gérer les opérations DRM asynchrones.     |
| [**IWMDRMDecrypt**](iwmdrmdecrypt.md)                                       | Fournit une méthode pour déchiffrer le contenu.                                                                       |
| [**IWMDRMEncrypt**](iwmdrmencrypt.md)                                       | Fournit une méthode pour chiffrer les données sur place.                                                                 |
| [**IWMDRMEncryptScatter**](iwmdrmencryptscatter.md)                         | Chiffre les données à partir de blocs non contigus.                                                                       |
| [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)                         | Extension de l’interface **IMFMediaEventGenerator** qui fournit une méthode pour annuler des opérations asynchrones. |
| [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md)       | Permet la récupération d’informations d’État avancées sur la progression de l’individualisation.                       |
| [**IWMDRMLicense**](iwmdrmlicense.md)                                       | Représente une ou plusieurs licences dans le magasin de licences local.                                                     |
| [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md) | Permet la récupération d’informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.                   |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Active les opérations de gestion pour le magasin de licences local.                                                      |
| [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)                   | Fournit des options de gestion supplémentaires pour le magasin de licences local.                                             |
| [**IWMDRMLicenseQuery**](iwmdrmlicensequery.md)                             | Permet aux applications d’interroger les droits et l’état de licence d’un fichier protégé.                                |
| [**IWMDRMNetReceiver**](iwmdrmnetreceiver.md)                               | fournit les méthodes nécessaires pour créer une application Microsoft Windows Media DRM pour les périphériques réseau.          |
| [**IWMDRMNetTransmitter**](iwmdrmnettransmitter.md)                         | fournit les méthodes nécessaires pour créer une application Microsoft Windows Media DRM pour les périphériques réseau.       |
| [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) | Fournit des méthodes qui permettent l’acquisition de licences avec intervention de l’utilisateur.                                        |
| [**IWMDRMProvider**](iwmdrmprovider.md)                                     | crée les autres objets des api étendues du Client Windows Microsoft Media DRM.                              |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gère différents processus liés à la sécurité pour l’ordinateur client et le sous-système DRM.                           |
| [**IWMDRMSecurity**](iwmdrmsecurity.md)                                     | Gère la révocation et le renouvellement des composants.                                                                       |
| [**IWMSecureBuffer**](iwmsecurebuffer.md)                                   | Active le chiffrement et le déchiffrement des mémoires tampons.                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Guide de référence de programmation**](drm-programming-reference.md)
</dt> </dl>

 

 




