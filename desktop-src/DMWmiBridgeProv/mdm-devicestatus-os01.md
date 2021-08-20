---
title: Classe MDM_DeviceStatus_OS01
description: La \_ classe DeviceStatus \_ OS01 MDM est utilisée par l’entreprise pour interroger le système d’exploitation sur les appareils avec leurs stratégies d’entreprise.
ms.assetid: 887dc453-f6b5-4f09-8ce1-b87f71dd8396
keywords:
- Classe MDM_DeviceStatus_OS01
- Classe MDM_DeviceStatus_OS01, Description
topic_type:
- apiref
api_name:
- MDM_DeviceStatus_OS01
- MDM_DeviceStatus_OS01.InstanceID
- MDM_DeviceStatus_OS01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ae98ed55f2fb4b5177b2596b99bb03ba8bdd6e74e3ba4e1c0e028928fdc0acb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118165842"
---
# <a name="mdm_devicestatus_os01-class"></a>\_ \_ Classe OS01 DeviceStatus MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ DeviceStatus \_ OS01 MDM** est utilisée par l’entreprise pour interroger le système d’exploitation sur les appareils avec leurs stratégies d’entreprise.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_DeviceStatus_OS01
{
  string InstanceID;
  string ParentID;
  string Edition;
};
```

## <a name="members"></a>Membres

La **classe \_ DeviceStatus \_ OS01 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ DeviceStatus \_ OS01 MDM** a ces propriétés.

<dl> <dt>

[Édition](/windows/client-management/mdm/devicestatus-csp#devicestatus-os-edition)
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

Nœud de la requête du système d’exploitation.

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

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                      |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



 

