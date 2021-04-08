---
title: Méthode EnrollMethod de la classe MDM_ClientCertificateInstall_Install03
description: Déclenche le démarrage de l’inscription de certificat par l’appareil.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Méthode EnrollMethod
- Méthode EnrollMethod, classe MDM_ClientCertificateInstall_Install03
- Classe MDM_ClientCertificateInstall_Install03, méthode EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742637"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Méthode EnrollMethod de la \_ \_ classe Install03 MDM ClientCertificateInstall

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Déclenche le démarrage de l’inscription de certificat par l’appareil. L’appareil n’enverra pas de notification au serveur MDM une fois l’inscription du certificat terminée. Le serveur MDM peut interroger ultérieurement l’appareil pour savoir si un nouveau certificat est ajouté. Voir aussi [**inscrire**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Syntaxe


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Obligatoire. Déclenche le démarrage de l’inscription de certificat par l’appareil. L’appareil n’enverra pas de notification au serveur MDM une fois l’inscription du certificat terminée. Le serveur MDM peut interroger ultérieurement l’appareil pour savoir si un nouveau certificat est ajouté.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MDM \_ ClientCertificateInstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

