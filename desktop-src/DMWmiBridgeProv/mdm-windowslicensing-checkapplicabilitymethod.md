---
title: Méthode CheckApplicabilityMethod de la classe MDM_WindowsLicensing
description: vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit de Windows 10 pour les appareils de bureau. Voir aussi CheckApplicability.
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
ms.openlocfilehash: db236e05ffe7b5b6273e7cba594266c31720932b43a7df2de751a0fa66cced5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119750149"
---
# <a name="checkapplicabilitymethod-method-of-the-mdm_windowslicensing-class"></a>Méthode CheckApplicabilityMethod de la \_ classe MDM WindowsLicensing

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

vérifie si la clé de produit entrée peut être utilisée pour une mise à niveau d’édition, l’activation ou la modification d’une clé de produit de Windows 10 pour les appareils de bureau. Voir aussi [CheckApplicability](/windows/client-management/mdm/windowslicensing-csp).

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
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

 

