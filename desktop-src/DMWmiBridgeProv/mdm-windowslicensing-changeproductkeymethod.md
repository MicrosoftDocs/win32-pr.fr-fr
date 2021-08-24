---
title: Méthode ChangeProductKeyMethod de la classe MDM_WindowsLicensing
description: cette méthode installe une clé de produit pour Windows 10 les appareils de bureau. Point ne pas redémarrer. Voir aussi ChangeProductKey.
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
ms.openlocfilehash: 0c164a97061b5e558a199a7d7e19a6bf26d7efc5d2a82c0a00e3831985c1a1cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693349"
---
# <a name="changeproductkeymethod-method-of-the-mdm_windowslicensing-class"></a>Méthode ChangeProductKeyMethod de la \_ classe MDM WindowsLicensing

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

cette méthode installe une clé de produit pour Windows 10 les appareils de bureau. Point ne pas redémarrer. Voir aussi [ChangeProductKey](/windows/client-management/mdm/windowslicensing-csp)

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
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_WINDOWSLICENSING MDM**](mdm-windowslicensing.md)
</dt> </dl>

 

