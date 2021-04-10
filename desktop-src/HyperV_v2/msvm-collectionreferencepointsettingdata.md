---
description: Fournit des informations supplémentaires à utiliser avec la méthode CreateReferencePoint de la \_ classe CollectionReferencePointService MSVM.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Classe Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ac05518a3ea9512745e9d2391c2d8cf1d387c96a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114582"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>MSVM \_ CollectionReferencePointSettingData, classe

Fournit des informations supplémentaires à utiliser avec la méthode [**CreateReferencePoint**](msvm-collectionreferencepointservice-createreferencepoint.md) de la [**classe \_ CollectionReferencePointService MSVM**](msvm-collectionreferencepointservice.md) .

La syntaxe suivante est simplifiée par rapport au code MOF (Managed Object Format) et inclut toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ CollectionReferencePointSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ CollectionReferencePointSettingData** possède les propriétés suivantes.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d’accès : lecture/écriture
</dt> </dl>

Niveau de cohérence du point de référence.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Inconnu** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>**Cohérence des applications** (1)


</dt> <dd>

Le point de référence indique un point dans le temps où le système virtuel se trouvait dans un état de cohérence en cas d’incident.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Cohérence des incidents** (2)


</dt> <dd>

Le point de référence indique un point dans le temps où le système virtuel était dans un état de cohérence des applications.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 10 uniquement\]<br/>                                                             |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




