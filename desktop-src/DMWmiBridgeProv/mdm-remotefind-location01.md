---
title: Classe MDM_RemoteFind_Location01
description: La \_ \_ classe LOCATION01 RemoteFind MDM récupère les informations d’emplacement pour un appareil particulier.
ms.assetid: 0c26bb3c-99b4-43ed-99ce-d976d48c4445
keywords:
- Classe MDM_RemoteFind_Location01
- Classe MDM_RemoteFind_Location01, Description
topic_type:
- apiref
api_name:
- MDM_RemoteFind_Location01
- MDM_RemoteFind_Location01.InstanceID
- MDM_RemoteFind_Location01.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36942badfe975a28d5212e502ab28984fa745f4a7563c39ed1cebb7d1b5dbcef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119077022"
---
# <a name="mdm_remotefind_location01-class"></a>\_ \_ Classe LOCATION01 RemoteFind MDM

\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation. Microsoft exclut toute garantie, expresse ou implicite, concernant les informations fournies ici.\]

La **classe \_ \_ Location01 RemoteFind MDM** récupère les informations d’emplacement pour un appareil particulier.

La syntaxe suivante issue du code MOF est simplifiée et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_RemoteFind_Location01
{
  string   InstanceID;
  string   ParentID;
  real32   Latitude;
  real32   Longitude;
  real32   Altitude;
  sint32   Accuracy;
  sint32   AltitudeAccuracy;
  datetime Age;
};
```

## <a name="members"></a>Membres

La **classe \_ RemoteFind \_ Location01 MDM** contient les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La **classe \_ RemoteFind \_ Location01 MDM** a ces propriétés.

<dl> <dt>

[Précision](/windows/client-management/mdm/remotefind-csp#accuracy)
</dt> <dd> <dl> <dt>

Type de données : **sint32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Age](/windows/client-management/mdm/remotefind-csp#age)
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Altitude](/windows/client-management/mdm/remotefind-csp#altitude)
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[AltitudeAccuracy](/windows/client-management/mdm/remotefind-csp#altitudeaccuracy)
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

Identifie le nom du nœud parent. Pour cette classe, la chaîne est « location ».

</dd> <dt>

[Latitude](/windows/client-management/mdm/remotefind-csp#latitude)
</dt> <dd> <dl> <dt>

Type de données : **real32**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

</dd> <dt>

[Longitude](/windows/client-management/mdm/remotefind-csp#longitude)
</dt> <dd> <dl> <dt>

Type de données : **real32**
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

Décrit le chemin d’accès complet au nœud parent. Pour cette classe, la chaîne est « ./Vendor/MSFT/RemoteFind »

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10 \[ applications de bureau uniquement\]<br/>                                                     |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                       |
| Espace de noms<br/>                | Racine dmmap de gestion des appareils mobiles \\ \\ \\<br/>                                                              |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv1. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl>  |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation de scripts PowerShell avec le fournisseur de pont WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

