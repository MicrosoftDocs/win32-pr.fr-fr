---
description: Représente les fournisseurs disponibles pour la réplication.
ms.assetid: CAAD1CFC-6473-4642-8366-0A5625AE1F70
title: Classe Msvm_ReplicationProvider
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationProvider
- Msvm_ReplicationProvider.InstanceID
- Msvm_ReplicationProvider.Caption
- Msvm_ReplicationProvider.Description
- Msvm_ReplicationProvider.ElementName
- Msvm_ReplicationProvider.Name
- Msvm_ReplicationProvider.OperationalStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 84b64ec1462d9d3cb487cac807891d57c219de7f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885696"
---
# <a name="msvm_replicationprovider-class"></a>MSVM \_ ReplicationProvider, classe

Représente les fournisseurs disponibles pour la réplication.

La syntaxe suivante est simplifiée à partir du code MOF et comprend les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ReplicationProvider : CIM_ManagedSystemElement
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  string Name;
  uint16 OperationalStatus[];
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ ReplicationProvider** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ ReplicationProvider** possède les propriétés suivantes.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **MaxLen** (64)
</dt> </dl>

Brève description de l’objet. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Pour cet objet, la valeur est :

« Fournisseur de réplication »

</dd> <dt>

**Description**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Description de l'objet . Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Pour les fournisseurs externes, la valeur est fournie par ces derniers. Pour que l’hôte héberge le fournisseur intégré, la valeur est :

« Fournisseur de réplication d’ordinateur virtuel sur l’hôte Hyper-V »

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nom complet du fournisseur de points de terminaison. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

Pour Host pour héberger le fournisseur incorporé, cette propriété a toujours la valeur :

« Fournisseur de réplication d’ordinateur virtuel sur l’hôte Hyper-V »

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**, **MaxLen** (256)
</dt> </dl>

L’ID d’instance WMI, qui identifie le fournisseur. Cette propriété est héritée de la [**\_ propriété ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement). Le format de cette propriété est « Microsoft : &lt; Host-machine-name &gt; \\ ReplicationProvider \\ &lt; Provider-Name &gt; ».

</dd> <dt>

**Nom**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**clé**](/windows/desktop/WmiSdk/key-qualifier), [**remplacement**](/windows/desktop/WmiSdk/standard-qualifiers) ("nom"), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Identificateur global unique (GUID) du fournisseur qui identifie le fournisseur de points de terminaison. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

Dans le cas d’un fournisseur externe, cette propriété est le CLSID de l’objet classe COM du fournisseur. Pour que l’hôte héberge le fournisseur incorporé, cette propriété est définie comme suit :

"22391CDC-272C-4DDF-BA88-9BEFB1A0975C"

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Type de données : tableau **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

États actuels de l’objet. Cette propriété est héritée de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement), et chaque élément de tableau est toujours défini sur :

<dl> <dt>

<span id="S_OK"></span><span id="s_ok"></span>**S \_ OK** (2)
</dt> </dl>

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez utiliser n’importe quel fournisseur disponible et la classe [**MSVM \_ ReplicationRelationship**](msvm-replicationrelationship.md) pour activer une relation de réplication. Par défaut, Hyper-V choisit l’hôte intégré au fournisseur hôte, qui peut être modifié lors de la création de la réplication. Le service de gestion Hyper-V communique avec un fournisseur externe à l’aide de COM.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                                 |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](cim-managedsystemelement.md)
</dt> <dt>

[**\_MANAGEDSYSTEMELEMENT CIM**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)
</dt> </dl>

 

