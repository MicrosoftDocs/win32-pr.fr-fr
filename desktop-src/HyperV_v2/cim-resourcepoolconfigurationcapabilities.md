---
description: Gère les fonctionnalités de l' \_ instance CIM ResourcePoolConfigurationService pour un \_ objet ResourcePool CIM.
ms.assetid: bd2eb4da-8ecd-4adb-b657-837c8da4dcdc
title: Classe CIM_ResourcePoolConfigurationCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationCapabilities
- CIM_ResourcePoolConfigurationCapabilities.AsynchronousMethodsSupported
- CIM_ResourcePoolConfigurationCapabilities.SynchronousMethodsSupported
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 967b307049fa9c5f81b8deb6da96bcaa3be9acc8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513002"
---
# <a name="cim_resourcepoolconfigurationcapabilities-class"></a>\_Classe CIM ResourcePoolConfigurationCapabilities

Gère les fonctionnalités de l’instance [**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md) pour un [**objet \_ ResourcePool CIM**](cim-resourcepool.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_ResourcePoolConfigurationCapabilities : CIM_Capabilities
{
  uint32 AsynchronousMethodsSupported[];
  uint32 SynchronousMethodsSupported[];
};
```

## <a name="members"></a>Membres

La classe **CIM \_ ResourcePoolConfigurationCapabilities** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ ResourcePoolConfigurationCapabilities** possède les propriétés suivantes.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Méthodes du service de configuration prises en charge pour les opérations asynchrones.

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

**CreateResourcePool est pris en charge** (2)


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

**CreateChild ResourcePool est pris en charge** (3)


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

**DeleteResourcePool est pris en charge** (4)


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

**AddResourcesToResourcePool est pris en charge** (5)


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

**RemoveResourcesFromResourcePool est pris en charge** (6)


</dt> <dd></dd> <dt>

<span id="ChangeParentResourcePool_is_supported"></span><span id="changeparentresourcepool_is_supported"></span><span id="CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

**ChangeParentResourcePool est pris en charge** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Méthodes du service de configuration prises en charge pour les opérations synchrones.

<dt>

<span id="CreateResourcePool_is_supported"></span><span id="createresourcepool_is_supported"></span><span id="CREATERESOURCEPOOL_IS_SUPPORTED"></span>

**CreateResourcePool est pris en charge** (2)


</dt> <dd></dd> <dt>

<span id="CreateChild_ResourcePool_is_supported"></span><span id="createchild_resourcepool_is_supported"></span><span id="CREATECHILD_RESOURCEPOOL_IS_SUPPORTED"></span>

**CreateChild ResourcePool est pris en charge** (3)


</dt> <dd></dd> <dt>

<span id="DeleteResourcePool_is_supported"></span><span id="deleteresourcepool_is_supported"></span><span id="DELETERESOURCEPOOL_IS_SUPPORTED"></span>

**DeleteResourcePool est pris en charge** (4)


</dt> <dd></dd> <dt>

<span id="AddResourcesToResourcePool_is_supported"></span><span id="addresourcestoresourcepool_is_supported"></span><span id="ADDRESOURCESTORESOURCEPOOL_IS_SUPPORTED"></span>

**AddResourcesToResourcePool est pris en charge** (5)


</dt> <dd></dd> <dt>

<span id="RemoveResourcesFromResourcePool_is_supported"></span><span id="removeresourcesfromresourcepool_is_supported"></span><span id="REMOVERESOURCESFROMRESOURCEPOOL_IS_SUPPORTED"></span>

**RemoveResourcesFromResourcePool est pris en charge** (6)


</dt> <dd></dd> <dt>

<span id="CIM_ChangeParentResourcePool_is_supported"></span><span id="cim_changeparentresourcepool_is_supported"></span><span id="CIM_CHANGEPARENTRESOURCEPOOL_IS_SUPPORTED"></span>

**CIM \_ ChangeParentResourcePool est pris en charge** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF réservé** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fournisseur réservé** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_Fonctionnalités CIM**](cim-capabilities.md)
</dt> </dl>

 

 




