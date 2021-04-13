---
title: Méthode ChangeProductKeyMethod de la classe MDM_WindowsLicensing
description: Cette méthode installe une clé de produit pour les appareils Windows 10 Desktop. Point ne pas redémarrer. Voir aussi ChangeProductKey.
ms.assetid: 1d9e3243-2ca4-427b-bda2-d33e1e70c80d
keywords:
- Méthode ChangeProductKeyMethod
- Méthode ChangeProductKeyMethod, classe MDM_WindowsLicensing
- Classe MDM_WindowsLicensing, méthode ChangeProductKeyMethod
topic_type:
- apiref
api_name:
- MDM_WindowsLicensing.ChangeProductKeyMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e00345fb0e23655b457e0540c70289a169c54ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466194"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Méthode ChangeProductKeyMethod de la \_ classe MDM WindowsLicensing

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Cette méthode installe une clé de produit pour les appareils Windows 10 Desktop. Point ne pas redémarrer. Voir aussi [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)

## <a name="syntax"></a>Syntaxe


```mof
uint32 ChangeProductKeyMethod(
  [in] string param
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*param* \[ dans\]
</dt> <dd></dd> </dl>

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
</dt> </dl>

 

