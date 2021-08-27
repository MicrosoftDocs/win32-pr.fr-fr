---
title: Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
description: La \_ \_ \_ classe EnterpriseDataProtection01 RETRIEVEBYTIMERANGE02 de rapports MDM est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime.
ms.assetid: 6abec00e-901f-4f79-840d-a4ef3a4d392d
keywords:
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- Classe MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02, Description
topic_type:
- apiref
api_name:
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.InstanceID
- MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60952e10f437b75edb4edf5a9465d4926b7e0615cc736f19f31520e02997d5f9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045609"
---
# <a name="mdm_reporting_enterprisedataprotection01_retrievebytimerange02-class"></a>\_ \_ Classe RetrieveByTimeRange02 EnterpriseDataProtection01 de création de rapports MDM \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02 de rapports MDM** est utilisée pour récupérer les journaux qui existent dans les classes StartTime et StopTime. Les StartTime et StopTime sont exprimés au format ISO 8601. Si les valeurs StartTime et StopTime ne sont pas spécifiées, les valeurs sont interprétées comme étant la première ou la dernière heure existante.

Voici les autres scénarios possibles :

-   Si les StartTime et StopTime ne sont pas spécifiés, il retourne tous les journaux existants.
-   Si le StopTime est spécifié, mais que l’heure de début n’est pas spécifiée, tous les journaux qui existent avant le StopTime sont retournés.
-   Si l’heure de début est spécifiée, mais que le StopTime n’est pas spécifié, tous les journaux qui existent à partir de StartTime sont retournés.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reporting_EnterpriseDataProtection01_RetrieveByTimeRange02
{
  string InstanceID;
  string ParentID;
  string Logs;
  string StartTime;
  string StopTime;
  sint32 Type;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ EnterpriseDataProtection01 \_ RetrieveByTimeRange02** de la gestion des rapports MDM a ces propriétés.

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

[StopTime](/windows/client-management/mdm/reporting-csp#stoptime)
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



 

