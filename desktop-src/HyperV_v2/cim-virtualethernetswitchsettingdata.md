---
description: Décrit les données de paramètres d’un commutateur Ethernet virtuel.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519846"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>\_Classe CIM VirtualEthernetSwitchSettingData

Décrit les données de paramètres d’un commutateur Ethernet virtuel.

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ VirtualEthernetSwitchSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ VirtualEthernetSwitchSettingData** possède les propriétés suivantes.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient les pools de ressources hôtes actuellement associés, ou à associer au commutateur Ethernet, afin d’allouer des connexions Ethernet entre le commutateur Ethernet et un ordinateur virtuel. Chaque valeur non null de cette propriété doit être conforme à **l' \_ URI WBEM \_ UntypedInstancePath** tel que défini dans la spécification « DSP0207 » DMTF.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre d’adresses MAC uniques que le commutateur peut apprendre pour l’apprentissage des adresses MAC, tel que défini dans la norme IEEE 802,1.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau qui contient les ID de réseau local virtuel auxquels le commutateur peut accéder.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




