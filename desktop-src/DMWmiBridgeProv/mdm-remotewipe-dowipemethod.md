---
title: méthode doWipeMethod de la classe MDM_RemoteWipe
description: Déclenche le démarrage de la réinitialisation à distance par l’appareil.
ms.assetid: dc25dc09-6a74-4c08-b452-b1d83085bb41
keywords:
- méthode doWipeMethod
- méthode doWipeMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, méthode doWipeMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f31dcc9dde2fe51ca0d8677df8b27637edd06c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464354"
---
# <a name="dowipemethod-method-of-the-mdm_remotewipe-class"></a>méthode doWipeMethod de la \_ classe MDM RemoteWipe

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

Déclenche le démarrage de la réinitialisation à distance par l’appareil. Voir aussi : la [réinitialisation](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntaxe


```mof
uint32 doWipeMethod(
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
| Espace de noms<br/>                | Racine DMMap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_REMOTEWIPE MDM**](mdm-remotewipe.md)
</dt> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

