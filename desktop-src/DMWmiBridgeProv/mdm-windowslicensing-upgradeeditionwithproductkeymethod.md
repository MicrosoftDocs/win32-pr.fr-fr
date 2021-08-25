---
title: Méthode UpgradeEditionWithProductKeyMethod de la classe MDM_WindowsLicensing
description: entre une clé de produit pour une mise à niveau d’édition de Windows 10 les appareils de bureau. Voir aussi UpgradeEditionWithProductKey.
ms.assetid: 6576fb5c-210c-4979-8c01-ed8f78e72c2c
keywords:
- Méthode UpgradeEditionWithProductKeyMethod
- Méthode UpgradeEditionWithProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode UpgradeEditionWithProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.UpgradeEditionWithProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a44293701c5a18f20b7e286530446c662778999f3ffa5ed8edffb5819dda8a91
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913239"
---
# <a name="upgradeeditionwithproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Méthode UpgradeEditionWithProductKeyMethod de la \_ classe MDM WindowsLicensing

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

entre une clé de produit pour une mise à niveau d’édition de Windows 10 les appareils de bureau. Voir aussi [UpgradeEditionWithProductKey](/windows/client-management/mdm/windowslicensing-csp).

## <a name="syntax"></a>Syntaxe


```mof
uint32 UpgradeEditionWithProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*param* \[ dans\]
</dt> <dd>

Clé de produit.

</dd> </dl>

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

 

