---
title: Classe MDM_Update_PendingRebootUpdates01_01
description: La \_ classe PendingRebootUpdates01 01 de la mise à jour MDM \_ \_ est utilisée pour gérer les mises à jour en attente au redémarrage.
ms.assetid: 752cdaaa-7883-43d4-be7d-7da9ad15d041
keywords:
- Classe MDM_Update_PendingRebootUpdates01_01
- Classe MDM_Update_PendingRebootUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_PendingRebootUpdates01_01
- MDM_Update_PendingRebootUpdates01_01.InstanceID
- MDM_Update_PendingRebootUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86a1cc421f4bd423137ff5699ebaf2412952e5f0f741952f91be15738b19b7ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109259"
---
# <a name="mdm_update_pendingrebootupdates01_01-class"></a>\_Classe de mise à jour MDM \_ PendingRebootUpdates01 \_ 01

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ PendingRebootUpdates01 \_ 01 de la mise à jour MDM** est utilisée pour gérer les mises à jour en attente au redémarrage.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_PendingRebootUpdates01_01
{
  string   InstanceID;
  string   ParentID;
  datetime InstalledTime;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ PendingRebootUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ mise à jour MDM \_ PendingRebootUpdates01 \_ 01** a ces propriétés.

<dl> <dt>

[InstalledTime](/windows/client-management/mdm/update-csp#pendingrebootupdates-pending-reboot-update-guid-installedtime)
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est le GUID de la mise à jour qui est en attente de redémarrage.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/PendingRebootUpdates »

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                            |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>\\DMWmiBridgeProv.dllMOF</dt> </dl> |



 

