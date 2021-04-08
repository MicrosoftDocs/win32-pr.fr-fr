---
title: Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
description: La \_ \_ \_ classe SecurityAuditing01 RETRIEVEBYTIMERANGE02 de rapports MDM est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime.
ms.assetid: e360bc76-f006-45e1-b78a-29125fbcd5ae
keywords:
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- Classe MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbbe47dfb3ff23c1d1bd891053375e19d6e503e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740061"
---
# <a name="mdm_reporting_securityauditing01_retrievebytimerange02-class"></a>\_ \_ Classe RetrieveByTimeRange02 SecurityAuditing01 de création de rapports MDM \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02 de rapports MDM** est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime. les StartTime et StopTime sont exprimés au format ISO 8601. Si les valeurs StartTime et StopTime ne sont pas spécifiées, les valeurs sont interprétées comme étant la première ou la dernière heure existante.

Voici les autres scénarios possibles :

-   Si les StartTime et StopTime ne sont pas spécifiés, il retourne tous les journaux existants.
-   Si le StopTime est spécifié, mais que l’heure de début n’est pas spécifiée, tous les journaux qui existent avant le StopTime sont retournés.
-   Si l’heure de début est spécifiée, mais que le StopTime n’est pas spécifié, tous les journaux qui existent à partir de StartTime sont retournés.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_SecurityAuditing01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ SecurityAuditing01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « RetrieveByTimeRange ».

</dd> <dt>

[Journaux](/windows/client-management/mdm/reporting-csp#logs)
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/SecurityAuditing »

</dd> <dt>

[StartTime](/windows/client-management/mdm/reporting-csp#starttime)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 

