---
title: Classe MDM_Reboot_Schedule01
description: Le \_ Schedule01class de redémarrage MDM \_ est utilisé pour configurer une heure spécifique pour le redémarrage d’un appareil.
ms.assetid: d865609a-9f17-4256-9c69-4fea75011c1f
keywords:
- Classe MDM_Reboot_Schedule01
- Classe MDM_Reboot_Schedule01, Description
topic_type:
- apiref
api_name:
- MDM_Reboot_Schedule01
- MDM_Reboot_Schedule01.InstanceID
- MDM_Reboot_Schedule01.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7229aca469ee83d9ac2e4b29f6d6b7c54875120
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464358"
---
# <a name="mdm_reboot_schedule01-class"></a>\_Classe Schedule01 de redémarrage MDM \_

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Schedule01 de redémarrage MDM** est utilisée pour configurer une heure spécifique pour le redémarrage d’un appareil.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_Reboot_Schedule01
{
  string InstanceID;
  string ParentID;
  string Single;
  string DailyRecurrent;
};
```

## <a name="members"></a>Membres

La **classe \_ \_ Schedule01 de redémarrage MDM** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ \_ Schedule01 de redémarrage MDM** a ces propriétés.

<dl> <dt>

[DailyRecurrent](/windows/client-management/mdm/reboot-csp#schedule-dailyrecurrent)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « Schedule ».

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/Reboot »

</dd> <dt>

[Unique](/windows/client-management/mdm/reboot-csp#schedule-single)
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



 

