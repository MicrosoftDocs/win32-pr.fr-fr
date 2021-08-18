---
description: représente un service d’appareil virtuel de la plateforme Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340169"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>MSVM \_ VirtualSystemResourceComponent, classe

représente un service d’appareil virtuel de la plateforme Microsoft Windows Hyper-V.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ VirtualSystemResourceComponent** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ VirtualSystemResourceComponent** possède les propriétés suivantes.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Tableau de chaînes contenant des classes non associées supplémentaires qui sont exposées par cette instance **MSVM \_ VirtualSystemResourceComponent** . Ces classes doivent dériver d' [**un \_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ou d’un [**\_ ResourceAllocationSettingData CIM**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**IDENTIFICATEUR**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

GUID qui représente l’identificateur de classe de l’objet COM du service. Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contexte**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Contexte dans lequel l’objet nouvellement créé s’exécutera. Cette valeur est passée dans le paramètre *dwClsContext* à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur 1.

</dd> <dt>

**Activé**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance est activée et peut être utilisée pour effectuer les demandes des clients ; Sinon, **false**. Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)et est toujours définie sur **true**.

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance peut être ajoutée à chaud à un ordinateur virtuel ; Sinon, **false**. La valeur par défaut est **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

**True** si cette instance peut être supprimée à chaud d’une machine virtuelle ; Sinon, **false**. La valeur par défaut est **False**.

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Chaîne indépendante du langage qui identifie de façon unique le service. Le format suivant est suggéré pour empêcher les conflits de noms : « version du composant du fournisseur \| \| ». Par exemple, ce nom représente la version 1,0 du composant de port réseau émulé Microsoft : « Microsoft \| EmulatedNetworkPortComponent \| v 1.0 ». Cette propriété est héritée de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Type**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Relation de l’objet WMI décrit ici avec l’appareil virtuel.



| Valeur                                                                                                                                                                                                                                                           | Signification                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**« Non modifiable »**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton est un objet WMI de niveau supérieur qui est lié 1:1 avec un appareil virtuel et qui ne peut exister qu’une seule fois par ordinateur virtuel. Il s'agit de la valeur par défaut.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**« MultiInstance »**</dt> <dt>2</dt> </dl>     | Multi-instance est un objet WMI de niveau supérieur qui peut exister plusieurs fois par machine virtuelle et est lié 1:1 avec un appareil virtuel.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**« Sous-appareil »**</dt> <dt>3</dt> </dl>                     | Le sous-appareil est un objet WMI qui n’a pas de référence parent, mais qui est contrôlé par un seul appareil virtuel qui ne peut exister qu’une seule fois par ordinateur virtuel. L’objet WMI peut cependant exister plusieurs fois.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

L’accès à la classe **MSVM \_ VirtualSystemResourceComponent** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                                    |
| Fin de la prise en charge des clients<br/>    | Windows 8.1<br/>                                                                                  |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSVM \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

