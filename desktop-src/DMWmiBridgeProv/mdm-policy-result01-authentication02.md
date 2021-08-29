---
title: Classe MDM_Policy_Result01_Authentication02
description: La \_ classe Result01 Authentication02 de la stratégie MDM \_ \_ représente les stratégies de gestion des authentifications disponibles.
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- Classe MDM_Policy_Result01_Authentication02
- Classe MDM_Policy_Result01_Authentication02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bfb88ebe1097d2b1f8b08c2f825e4e727d13d6be433098bf87eda52cf4be85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913659"
---
# <a name="mdm_policy_result01_authentication02-class"></a>\_Classe Authentication02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** représente les stratégies de gestion des authentifications disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ Authentication02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[AllowAadPasswordReset](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowFastReconnect](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowFidoDeviceSignon](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AllowSecondaryAuthenticationDevice](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « Authentication ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Policy/Result »

</dd> </dl>

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

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

