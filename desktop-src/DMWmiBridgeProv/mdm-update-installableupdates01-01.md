---
title: Classe MDM_Update_InstallableUpdates01_01
description: La \_ classe mise à jour MDM \_ InstallableUpdates01 \_ 01 est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.
ms.assetid: 53ca2291-a92a-46ed-948d-6d2a2dddd296
keywords:
- Classe MDM_Update_InstallableUpdates01_01
- Classe MDM_Update_InstallableUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_InstallableUpdates01_01
- MDM_Update_InstallableUpdates01_01.InstanceID
- MDM_Update_InstallableUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2bcb9dd3ec026e6894d4ba7155cc41f12bc01e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843125"
---
# <a name="mdm_update_installableupdates01_01-class"></a>\_Classe de mise à jour MDM \_ InstallableUpdates01 \_ 01

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ mise à jour MDM \_ InstallableUpdates01 \_ 01** est utilisée pour gérer et contrôler le lancement des mises à jour approuvées.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_InstallableUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 Type;
  sint32 RevisionNumber;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ InstallableUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ mise à jour MDM \_ InstallableUpdates01 \_ 01** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identifie le nom du nœud parent. Pour cette classe, la chaîne est le GUID de la mise à jour approuvée.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/InstallableUpdates »

</dd> <dt>

[RevisionNumber](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-revisionnumber)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Type](/windows/client-management/mdm/update-csp#installableupdates-installable-update-guid-type)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
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



 

