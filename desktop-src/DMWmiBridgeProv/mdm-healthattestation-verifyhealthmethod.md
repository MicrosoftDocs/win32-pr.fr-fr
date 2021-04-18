---
title: Méthode VerifyHealthMethod de la classe MDM_HealthAttestation
description: Méthode pour informer l’appareil de la préparation d’une demande de vérification du certificat d’intégrité. Voir aussi VerifyHealth.
ms.assetid: f5b11081-c664-4525-8f36-5f17c21e7f22
keywords:
- Méthode VerifyHealthMethod
- Méthode VerifyHealthMethod, classe MDM_HealthAttestation
- Classe MDM_HealthAttestation, méthode VerifyHealthMethod
topic_type:
- apiref
api_name:
- MDM_HealthAttestation.VerifyHealthMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d90d71d3758059706d4ea598e7012433220feb27
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511754"
---
# <a name="verifyhealthmethod-method-of-the-mdm_healthattestation-class"></a>Méthode VerifyHealthMethod de la \_ classe MDM HealthAttestation

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Méthode pour informer l’appareil de la préparation d’une demande de vérification du certificat d’intégrité. Voir aussi [VerifyHealth](/windows/client-management/mdm/healthattestation-csp).

## <a name="syntax"></a>Syntaxe


```mof
uint32 VerifyHealthMethod();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

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

[**\_HEALTHATTESTATION MDM**](mdm-healthattestation.md)
</dt> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

