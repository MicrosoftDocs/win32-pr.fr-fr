---
title: Fonctions d’inscription MDM
description: Les fonctions suivantes sont déclarées dans `mdmregistration.h` , et sont utilisées par l’inscription MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.localizationpriority: low
ms.topic: reference
ms.date: 11/19/2020
ms.openlocfilehash: f9149c4bd2f9f931a506dc35d05b5e1c641dc87445fbf88fd73ff9ad20ac514b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040369"
---
# <a name="mdm-registration-functions"></a>Fonctions d’inscription MDM

Les fonctions suivantes sont déclarées dans `mdmregistration.h` , et sont utilisées par l’inscription MDM.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**DiscoverManagementService**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementservice) | Découvre le service MDM. |
| [**DiscoverManagementServiceEx**](/windows/win32/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex) | Découvre le service MDM à l’aide d’un serveur candidat. |
| [**GetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-getdevicemanagementconfiginfo) | Obtient les informations de configuration associées à l’ID du fournisseur. |
| [**GetDeviceRegistrationInfo**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo) | Récupère les informations d’inscription de l’appareil. |
| [**GetManagementAppHyperlink**](/windows/win32/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink) | Récupère le lien hypertexte de l’application de gestion associé au service MDM. |
| [**IsDeviceRegisteredWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement) | Vérifie si l’appareil est inscrit auprès d’un service MDM. |
| [**IsManagementRegistrationAllowed**](/windows/win32/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed) | Vérifie si l’inscription MDM est autorisée par la stratégie locale. |
| [**RegisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement) | Inscrit un appareil auprès d’un service de gestion des appareils mobiles à l’aide du [ \[ protocole d’inscription MS-MDE \] : Mobile Device](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267). |
| [**RegisterDeviceWithManagementUsingAADCredentials**](/windows/win32/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials) | inscrit un appareil auprès d’un service MDM, à l’aide des informations d’identification de Azure Active Directory (AAD). |
| [**SetDeviceManagementConfigInfo**](/windows/win32/api/mdmregistration/nf-mdmregistration-setdevicemanagementconfiginfo) | Définit les informations de configuration associées à l’ID du fournisseur. |
| [**SetManagedExternally**](/windows/win32/api/MDMRegistration/nf-mdmregistration-setmanagedexternally) | Indique à l’agent MDM que l’appareil est géré en externe et qu’il ne doit pas être inscrit auprès d’un service MDM. |
| [**UnregisterDeviceWithManagement**](/windows/win32/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement) | Annule l’inscription d’un appareil auprès du service MDM. |

## <a name="related-topics"></a>Rubriques connexes

* [Informations de référence sur l’inscription MDM](./mdm-registration-reference.md)
