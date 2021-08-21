---
title: Classe MDM_Policy_Result01_BitLocker02
description: La \_ classe Result01 Bitlocker02 de la stratégie MDM \_ \_ représente les stratégies BitLocker disponibles.
ms.assetid: 5b20a129-65a8-4ec1-b938-57ddaca46ac3
keywords:
- Classe MDM_Policy_Result01_BitLocker02
- Classe MDM_Policy_Result01_BitLocker02, Description
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_BitLocker02
- MDM_Policy_Result01_BitLocker02.InstanceID
- MDM_Policy_Result01_BitLocker02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ef9e5d2e32b97bb6df6d1f49fca3a0099d7fbebfdad3fbfd376fe7d9f886a4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118164602"
---
# <a name="mdm_policy_result01_bitlocker02-class"></a>\_Classe BitLocker02 de la stratégie MDM \_ Result01 \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Result01 \_ Bitlocker02 de la stratégie MDM** représente les stratégies BitLocker disponibles.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_BitLocker02
{
  string InstanceID;
  string ParentID;
  sint32 EncryptionMethod;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Result01 \_ BitLocker02 de la stratégie MDM** a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Result01 \_ BitLocker02 de la stratégie MDM** a ces propriétés.

<dl> <dt>

[EncryptionMethod](/windows/client-management/mdm/policy-csp-bitlocker#bitlocker-encryptionmethod)
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « BitLocker »

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
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

