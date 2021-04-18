---
title: Interface IWMDRMLicenseManagement
description: L’interface IWMDRMLicenseManagement fournit des méthodes qui effectuent des opérations générales liées au magasin de licences local. Pour obtenir une instance de cette interface, appelez IWMDRMProvider CreateObject. Transmettez IID \_ IWMDRMLicenseManagement comme paramètre riid.
ms.assetid: 254bf54e-8ea6-4fd1-8abd-9d32539d529b
keywords:
- Format Windows Media de l’interface IWMDRMLicenseManagement
- Interface IWMDRMLicenseManagement format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14a7c555200e2eac99def75a1ad8c1d5dc1223fc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312481"
---
# <a name="iwmdrmlicensemanagement-interface"></a>Interface IWMDRMLicenseManagement

L’interface **IWMDRMLicenseManagement** fournit des méthodes qui effectuent des opérations générales liées au magasin de licences local.

Pour obtenir une instance de cette interface, appelez [**IWMDRMProvider :: CreateObject**](iwmdrmprovider-createobject.md). Transmettez **IID \_ IWMDRMLicenseManagement** comme paramètre *riid* .

## <a name="members"></a>Membres

L’interface **IWMDRMLicenseManagement** hérite de [**IWMDRMEventGenerator**](iwmdrmeventgenerator.md). **IWMDRMLicenseManagement** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMLicenseManagement** possède ces méthodes.



| Méthode                                                                                               | Description                                                                                                             |
|:-----------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md)                                     | Acquiert de manière asynchrone une licence à partir d’une URL spécifiée.<br/>                                                      |
| [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)                                     | Crée une sauvegarde des licences dans le magasin de licences local.<br/>                                                 |
| [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md)                               | Supprime les licences marquées du magasin de licences et défragmente le magasin pour améliorer les performances.<br/>             |
| [**CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md)                 | Crée un objet d’énumérateur de licence rempli avec les informations de licence en fonction des valeurs de paramètre.<br/>            |
| [**CreateLicenseRevocationChallenge**](iwmdrmlicensemanagement-createlicenserevocationchallenge.md) | Génère une demande de révocation de licence.<br/>                                                                    |
| [**DeleteLicense**](iwmdrmlicensemanagement-deletelicense.md)                                       | Supprime une licence du magasin de licences local temporaire.<br/>                                                    |
| [**MonitorLicenseAcquisition**](iwmdrmlicensemanagement-monitorlicenseacquisition.md)               | Lance l’analyse pour un processus d’acquisition de licence.<br/>                                                      |
| [**ProcessLicenseDeletionMessage**](iwmdrmlicensemanagement-processlicensedeletionmessage.md)       | Supprime une licence importée pour le contenu initialement protégé par un autre système de protection du contenu.<br/> |
| [**ProcessLicenseRevocationResponse**](iwmdrmlicensemanagement-processlicenserevocationresponse.md) | Révoque les licences du magasin de licences local.<br/>                                                               |
| [**RestoreLicenses**](iwmdrmlicensemanagement-restorelicenses.md)                                   | Restaure les licences précédemment sauvegardées.<br/>                                                                      |
| [**StoreLicense**](iwmdrmlicensemanagement-storelicense.md)                                         | Ajoute une licence au magasin de licences local.<br/>                                                                   |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> <dt>

[**IWMDRMEventGenerator**](iwmdrmeventgenerator.md)
</dt> </dl>

 

 





