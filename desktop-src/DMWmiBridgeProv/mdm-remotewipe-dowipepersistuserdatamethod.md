---
title: méthode doWipePersistUserDataMethod de la classe MDM_RemoteWipe
description: Déclenche l’appareil pour démarrer la réinitialisation à distance tout en conservant les comptes d’utilisateur et les données.
keywords:
- méthode doWipePersistUserDataMethod
- méthode doWipePersistUserDataMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, méthode doWipePersistUserDataMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipePersistUserDataMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 09/17/2021
ms.openlocfilehash: 00a9dd0ee93d71b2aeec3bb8b83a3b34bc044e05
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523800"
---
# <a name="dowipepersistuserdatamethod-method-of-the-mdm_remotewipe-class"></a>méthode doWipePersistUserDataMethod de la classe MDM_RemoteWipe

> [!NOTE]
> **Certaines informations portent sur la préversion du produit, qui est susceptible d’être en grande partie modifié avant sa commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.**

Déclenche l’appareil pour démarrer la réinitialisation à distance tout en conservant les comptes d’utilisateur et les données. Voir aussi [doWipePersistUserDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntaxe

```mof
uint32 doWipePersistUserDataMethod(
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
