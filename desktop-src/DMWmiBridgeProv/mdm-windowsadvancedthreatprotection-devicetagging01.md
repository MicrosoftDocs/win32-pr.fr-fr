---
title: Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
description: la \_ classe WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM est utilisée pour intégrer, déterminer l’état de configuration et d’intégrité, et les points de terminaison annuler pour Windows Defender Protection avancée contre les menaces.
ms.assetid: b56d5d46-e994-404a-865a-c59bb948f2b3
keywords:
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- Classe MDM_WindowsAdvancedThreatProtection_DeviceTagging01, Description
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.InstanceID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.ParentID
- MDM_WindowsAdvancedThreatProtection_DeviceTagging01.IdMethod
api_type:
- DllExport
api_location:
- DMWmiBridgeProv.dll
ms.openlocfilehash: f095c39c78400f5d040ff00ab668f51c7d7abfaac2b0d872ed860f768ea55404
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119913409"
---
# <a name="mdm_windowsadvancedthreatprotection_devicetagging01-class"></a>\_ \_ Classe DEVICETAGGING01 WindowsAdvancedThreatProtection MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

la \_ classe WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM est utilisée pour intégrer, déterminer l’état de configuration et d’intégrité, et les points de terminaison annuler pour Windows Defender Protection avancée contre les menaces.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_WindowsAdvancedThreatProtection_DeviceTagging01
{
  string InstanceID;
  string ParentID;
  string Group;
  sint32 Criticality;
  sint32 IdMethod;
};
```

## <a name="members"></a>Membres

La **classe \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ WindowsAdvancedThreatProtection \_ DeviceTagging01 MDM** a ces propriétés.

<dl> <dt>

[Caractère critique](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#criticality)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Groupe](/windows/client-management/mdm/windowsadvancedthreatprotection-csp#group)
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

**IdMethod**
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

TBD

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
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

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                       |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



 

