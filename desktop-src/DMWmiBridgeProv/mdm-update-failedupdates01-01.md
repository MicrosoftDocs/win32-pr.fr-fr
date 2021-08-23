---
title: Classe MDM_Update_FailedUpdates01_01
description: La \_ classe FailedUpdates01 01 de la mise à jour MDM \_ \_ est utilisée pour gérer les mises à jour ayant échoué.
ms.assetid: 3bb7993b-b44b-44d1-84ee-dbdda0093ca0
keywords:
- Classe MDM_Update_FailedUpdates01_01
- Classe MDM_Update_FailedUpdates01_01, Description
topic_type:
- apiref
api_name:
- MDM_Update_FailedUpdates01_01
- MDM_Update_FailedUpdates01_01.InstanceID
- MDM_Update_FailedUpdates01_01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 646f485544e9a51711e55453d79f1a16d0a37d38c8d18d6ed4d2340e3c34fa30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119795949"
---
# <a name="mdm_update_failedupdates01_01-class"></a>\_Classe de mise à jour MDM \_ FailedUpdates01 \_ 01

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ FailedUpdates01 \_ 01 de la mise à jour MDM** est utilisée pour gérer les mises à jour ayant échoué.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Update_FailedUpdates01_01
{
  string InstanceID;
  string ParentID;
  sint32 HResult;
  sint32 State;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ FailedUpdates01 \_ 01 de la mise à jour MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe de **\_ mise à jour MDM \_ FailedUpdates01 \_ 01** a ces propriétés.

<dl> <dt>

[Signé](/windows/client-management/mdm/update-csp#failedupdates-failed-update-guid-hresult)
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est le GUID de la mise à jour ayant échoué.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Update/FailedUpdates »

</dd> <dt>

[**Département**](/windows/client-management/mdm/update-csp)
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



 

