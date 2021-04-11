---
title: Fonctions d’inscription MDM
description: Les fonctions suivantes sont utilisées par l’inscription MDM.
ms.assetid: 1b063a56-f59f-4b02-949f-c8b6bbf45a13
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 821e08d9c6631bbb300a86ab6b9c480a3af0c25b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104316608"
---
# <a name="mdm-registration-functions"></a>Fonctions d’inscription MDM

Les fonctions suivantes sont utilisées par l’inscription MDM.

## <a name="in-this-section"></a>Dans cette section

<dl> <dt>

[**DiscoverManagementService**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementservice)
</dt> <dd>

Découvre le service MDM.

</dd> <dt>

[**DiscoverManagementServiceEx**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-discovermanagementserviceex)
</dt> <dd>

Découvre le service MDM à l’aide d’un serveur candidat.

</dd> <dt>

[**GetDeviceRegistrationInfo**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getdeviceregistrationinfo)
</dt> <dd>

Récupère les informations d’inscription de l’appareil.

</dd> <dt>

[**GetManagementAppHyperlink**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-getmanagementapphyperlink)
</dt> <dd>

Récupère le lien hypertexte de l’application de gestion associé au service MDM.

</dd> <dt>

[**IsDeviceRegisteredWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-isdeviceregisteredwithmanagement)
</dt> <dd>

Vérifie si l’appareil est inscrit auprès d’un service MDM.

</dd> <dt>

[**IsManagementRegistrationAllowed**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-ismanagementregistrationallowed)
</dt> <dd>

Vérifie si l’inscription MDM est autorisée par la stratégie locale.

</dd> <dt>

[**RegisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagement)
</dt> <dd>

Inscrit un appareil auprès d’un service de gestion des appareils mobiles à l’aide du [ \[ protocole d’inscription MS-MDE \] : Mobile Device](/openspecs/windows_protocols/ms-mde/5c841535-042e-489e-913c-9d783d741267).

</dd> <dt>

[**RegisterDeviceWithManagementUsingAADCredentials**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-registerdevicewithmanagementusingaadcredentials)
</dt> <dd>

Inscrit un appareil auprès d’un service MDM, à l’aide des informations d’identification de Azure Active Directory (AAD).

</dd> <dt>

[**SetManagedExternally**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-setmanagedexternally)
</dt> <dd>

Indique à l’agent MDM que l’appareil est géré en externe et qu’il ne doit pas être inscrit auprès d’un service MDM.

</dd> <dt>

[**UnregisterDeviceWithManagement**](/windows/desktop/api/MDMRegistration/nf-mdmregistration-unregisterdevicewithmanagement)
</dt> <dd>

Annule l’inscription d’un appareil auprès du service MDM

</dd> </dl>

 

 