---
title: méthode doWipeProtectedMethod de la classe MDM_RemoteWipe
description: Déclenche l’appareil pour démarrer la réinitialisation à distance sur l’appareil et nettoyer entièrement le lecteur interne. Dans certaines configurations d’appareil, cette commande risque de ne pas pouvoir démarrer l’appareil.
keywords:
- méthode doWipeProtectedMethod
- méthode doWipeProtectedMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, méthode doWipeProtectedMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipeProtectedMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 09/17/2021
ms.openlocfilehash: 792d4e412b8a16869bbfa33229abe541be1c952e
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523796"
---
# <a name="dowipeprotectedmethod-method-of-the-mdm_remotewipe-class"></a>méthode doWipeProtectedMethod de la classe MDM_RemoteWipe

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

Déclenche l’appareil pour démarrer la réinitialisation à distance sur l’appareil et nettoyer entièrement le lecteur interne. Dans certaines configurations d’appareil, cette commande risque de ne pas pouvoir démarrer l’appareil. Voir aussi [doWipePersistProvisionedDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntaxe

```mof
uint32 doWipeProtectedMethod(
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
| Espace de noms<br/>                | Racine DMMap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_REMOTEWIPE MDM**](mdm-remotewipe.md)
</dt> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>
