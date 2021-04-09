---
title: Méthode CheckApplicabilityMethod de la classe MDM_WindowsLicensing
description: Vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit Windows 10 pour les appareils de bureau. Voir aussi CheckApplicability.
ms.assetid: b28ea397-72dd-4c10-a9fb-53087c3b654c
keywords:
- Méthode CheckApplicabilityMethod
- Méthode CheckApplicabilityMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode CheckApplicabilityMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.CheckApplicabilityMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae08c4a13d036a7d1185a3d53dee846ea460e53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104941"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Méthode CheckApplicabilityMethod de la \_ classe MDM WindowsLicensing

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit Windows 10 pour les appareils de bureau. Voir aussi [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Syntaxe


```mof
uint32 CheckApplicabilityMethod(
  [in] string param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*param* \[ dans\]
</dt> <dd>

Clé de produit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

TRUE ou FALSE

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

[**\_WINDOWSLICENSING MDM**](mdm-windowslicensing.md)
</dt> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

