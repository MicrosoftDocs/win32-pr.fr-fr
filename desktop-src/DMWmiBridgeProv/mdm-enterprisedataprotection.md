---
title: Classe MDM_EnterpriseDataProtection
description: la \_ classe EnterpriseDataProtection MDM est utilisée pour déterminer l’état actuel des paramètres spécifiques de Windows Information Protection (WIP) (anciennement appelé Protection des données Enterprise).
ms.assetid: 2b97de12-76d1-4b74-a979-f0484807b840
keywords:
- Classe MDM_EnterpriseDataProtection
- Classe MDM_EnterpriseDataProtection, Description
topic_type:
- apiref
api_name:
- MDM_EnterpriseDataProtection
- MDM_EnterpriseDataProtection.InstanceID
- MDM_EnterpriseDataProtection.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c9ab641873f95f3b7d7b60772dd10ed0a38c12f57497304478a4c469ee1c645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694879"
---
# <a name="mdm_enterprisedataprotection-class"></a>\_Classe ENTERPRISEDATAPROTECTION MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la **classe \_ EnterpriseDataProtection MDM** est utilisée pour déterminer l’état actuel des paramètres spécifiques de Windows Information Protection (WIP) (anciennement appelé Protection des données Enterprise).

Pour plus d’informations sur les travaux en cours, consultez [protéger vos données d’entreprise à l’aide de la protection des données d’entreprise (EDP)](/windows/security/information-protection/windows-information-protection/protect-enterprise-data-using-wip).

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_EnterpriseDataProtection
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Membres

La **classe \_ EnterpriseDataProtection MDM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ EnterpriseDataProtection MDM** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « EnterpriseDataProtection ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/ »

</dd> <dt>

[État](/windows/client-management/mdm/enterprisedataprotection-csp#status)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 

