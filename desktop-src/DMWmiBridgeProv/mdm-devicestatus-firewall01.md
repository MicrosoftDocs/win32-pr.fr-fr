---
title: Classe MDM_DeviceStatus_Firewall01
description: La \_ classe DeviceStatus \_ Firewall01 MDM est utilisée par l’entreprise pour interroger l’état de conformité du pare-feu des appareils avec leurs stratégies d’entreprise.
ms.assetid: 0f62350c-8c7b-44fb-b163-dedaf4669895
keywords:
- Classe MDM_DeviceStatus_Firewall01
- Classe MDM_DeviceStatus_Firewall01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_Firewall01
- MDM_DeviceStatus_Firewall01.InstanceID
- MDM_DeviceStatus_Firewall01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67166a076b9e6db01d8642d7b1d21e72b8732c6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742628"
---
# <a name="mdm_devicestatus_firewall01-class"></a>\_ \_ Classe FIREWALL01 DeviceStatus MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ DeviceStatus \_ Firewall01 MDM** est utilisée par l’entreprise pour interroger l’état de conformité du pare-feu des appareils avec leurs stratégies d’entreprise.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_Firewall01
{
  string InstanceID;
  string ParentID;
  sint32 Status;
};
```

## <a name="members"></a>Membres

La **classe \_ DeviceStatus \_ Firewall01 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ DeviceStatus \_ Firewall01 MDM** a ces propriétés.

<dl> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Nœud pour la requête de pare-feu.

</dd> <dt>

**ID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/DeviceStatus »

</dd> <dt>

[État](/windows/client-management/mdm/devicestatus-csp#devicestatus-battery-status)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

