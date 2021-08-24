---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
description: La \_ \_ classe EnterpriseDataProtection01 RetrieveByCount02 de rapports MDM \_ est utilisée pour récupérer un nombre spécifié de journaux à partir de StartTime.
ms.assetid: 0a581d5a-129b-48c3-a7a1-3947cc1e2ee9
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 509ab80a8f7b33d3ac7f9d40157152ce5aa693376e4e61edc4581f8d375f1c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119825479"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebycount02-class"></a>\_ \_ Classe RetrieveByCount02 EnterpriseDataProtection01 de création de rapports MDM \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02 de rapports MDM** est utilisée pour récupérer un nombre spécifié de journaux à partir de StartTime. L’heure de début est exprimée au format ISO 8601. Vous pouvez définir le nombre de journaux requis en définissant LogCount et StartTime. Elle retourne le nombre spécifié de journaux ou moins, si le nombre total de journaux est inférieur à LogCount.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByCount02
{
  string InstanceID;
  string ParentID;
  string Logs;
  sint32 LogCount;
  string StartTime;
  sint32 Type;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02** de la gestion des rapports MDM a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByCount02** de la gestion des rapports MDM a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « RetrieveByCount ».

</dd> <dt>

[LogCount](/windows/client-management/mdm/reporting-csp#logcount)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Journaux d’activité](/windows/client-management/mdm/reporting-csp#logs)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/EnterpriseDataProtection »

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Type](/windows/client-management/mdm/reporting-csp#type)
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



 

