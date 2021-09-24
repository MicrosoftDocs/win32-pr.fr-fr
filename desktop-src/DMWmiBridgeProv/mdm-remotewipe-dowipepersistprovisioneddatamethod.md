---
title: méthode doWipePersistProvisionedDataMethod de la classe MDM_RemoteWipe
description: Déclenche l’appareil pour sauvegarder les données de configuration dans un emplacement persistant et effectuer une réinitialisation à distance sur l’appareil. Les informations qui ont été sauvegardées seront restaurées et appliquées à l’appareil lors de la reprise.
keywords:
- méthode doWipePersistProvisionedDataMethod
- méthode doWipePersistProvisionedDataMethod, classe MDM_RemoteWipe
- Classe MDM_RemoteWipe, méthode doWipePersistProvisionedDataMethod
topic_type:
- apiref
api_name:
- MDM_RemoteWipe.doWipePersistProvisionedDataMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f346b520499c6a6d0eb5c181f8fd9b5dcd0208b
ms.sourcegitcommit: 2c13d0f1620f7c089687ef1d97e8c1d22e5d537a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "128523799"
---
# <a name="dowipepersistprovisioneddatamethod-method-of-the-mdm_remotewipe-class"></a>méthode doWipePersistProvisionedDataMethod de la classe MDM_RemoteWipe

> [!NOTE]
> **Certaines informations relatives à un produit en version préliminaire, qui peuvent être substantiellement modifiées avant sa commercialisation. Microsoft exclut toute garantie, expresse ou implicite, en ce qui concerne les informations fournies ici.** 
 ![ image](https://user-images.githubusercontent.com/31261191/133865694-1fae8e8b-c3ba-41a9-bcba-dbb67a6e2130.png)

Déclenche l’appareil pour sauvegarder les données de configuration dans un emplacement persistant et effectuer une réinitialisation à distance sur l’appareil. Les informations qui ont été sauvegardées seront restaurées et appliquées à l’appareil lors de la reprise. Voir aussi [doWipePersistProvisionedDataMethod](/windows/client-management/mdm/remotewipe-csp).

## <a name="syntax"></a>Syntaxe

```mof
uint32 doWipePersistProvisionedDataMethod(
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
