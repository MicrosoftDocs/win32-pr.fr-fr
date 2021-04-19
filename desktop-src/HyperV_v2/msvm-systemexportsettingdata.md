---
description: Associe un ordinateur virtuel et ses données de paramètre d’exportation.
ms.assetid: FAAE7F74-07C0-4638-ABF9-5DEDBF2B9DD6
title: Classe Msvm_SystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemExportSettingData
- Msvm_SystemExportSettingData.ManagedElement
- Msvm_SystemExportSettingData.SettingData
- Msvm_SystemExportSettingData.IsDefault
- Msvm_SystemExportSettingData.IsCurrent
- Msvm_SystemExportSettingData.IsNext
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8203a45bb911743bb064c1a686da0b3d8abe99bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106513362"
---
# <a name="msvm_systemexportsettingdata-class"></a>MSVM \_ SystemExportSettingData, classe

Associe un ordinateur virtuel et ses données de paramètre d’exportation. Avant d’appeler la méthode [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) de la classe [**\_ VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md) , vous pouvez récupérer une instance de [**MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md) à l’aide de cette association.

La syntaxe suivante est simplifiée format MOF (MOF) et comprend toutes les propriétés héritées.

## <a name="syntax"></a>Syntaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemExportSettingData : CIM_ElementSettingData
{
  CIM_ComputerSystem                  REF ManagedElement;
  Msvm_VirtualSystemExportSettingData REF SettingData;
  uint16                                  IsDefault = 1;
  uint16                                  IsCurrent = 1;
  uint16                                  IsNext = 0;
};
```

## <a name="members"></a>Membres

La classe **MSVM \_ SystemExportSettingData** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **MSVM \_ SystemExportSettingData** possède les propriétés suivantes.

<dl> <dt>

**IsCurrent**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le paramètre référencé est actuellement utilisé dans l’opération de l’élément, ou si ces informations sont inconnues. Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valeur                                                                        | Signification                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Actuel<br/>     |
| <dl> <dt>2</dt> </dl> | Non actuel<br/> |



 

</dd> <dt>

**IsDefault**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le paramètre référencé est un paramètre par défaut pour l’élément, ou si ces informations sont inconnues. Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valeur                                                                        | Signification                |
|------------------------------------------------------------------------------|------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>     |
| <dl> <dt>1</dt> </dl> | Default<br/>     |
| <dl> <dt>2</dt> </dl> | Pas par défaut<br/> |



 

</dd> <dt>

**IsNext**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le paramètre référencé est ou non le paramètre suivant à appliquer. Par exemple, l’application peut être exécutée sur une demande de réinitialisation, de réinitialisation et de reconfiguration. Il peut s’agir d’un paramètre permanent, ou d’un paramètre utilisé une seule fois, comme indiqué par l’indicateur. S’il s’agit d’un paramètre permanent, le paramètre est appliqué à chaque réinitialisation de l’élément managé, jusqu’à ce que cet indicateur soit réinitialisé manuellement. Toutefois, s’il s’agit d’une utilisation unique, l’indicateur est automatiquement effacé après l’application des paramètres. En outre, si cet indicateur est spécifié (c’est-à-dire défini sur une valeur autre que 0 (inconnu)), il est prioritaire sur les données de paramètre qui ont pu être spécifiées comme valeurs par défaut. Par exemple : si l’élément géré est un système informatique et que la valeur de cet indicateur est 1 (suivant), le paramètre sera effectif à la prochaine réinitialisation du système. Et, sauf si cet indicateur est modifié, il est conservé pour les réinitialisations ultérieures du système. Toutefois, si cet indicateur a la valeur 3 (est ensuite utilisé pour une utilisation unique), ce paramètre n’est utilisé qu’une seule fois et l’indicateur est réinitialisé après cela sur 2 (n’est pas suivant). Ainsi, dans l’exemple ci-dessus, si le système redémarre rapidement en succession, le paramètre ne sera pas utilisé au deuxième redémarrage.

Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).



| Valeur                                                                        | Signification                           |
|------------------------------------------------------------------------------|-----------------------------------|
| <dl> <dt>0</dt> </dl> | Unknown<br/>                |
| <dl> <dt>1</dt> </dl> | Est ensuite<br/>                |
| <dl> <dt>2</dt> </dl> | N’est pas suivant<br/>            |
| <dl> <dt>3</dt> </dl> | Est ensuite utilisé pour une utilisation unique<br/> |



 

</dd> <dt>

**Propriété ManagedElement**
</dt> <dd> <dl> <dt>

Type de données : **[ **CIM CIM \_**](msvm-computersystem.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. propriété ManagedElement")
</dt> </dl>

Référence à la machine virtuelle. Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> <dt>

**SettingData**
</dt> <dd> <dl> <dt>

Type de données : **[ **MSVM \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ ElementSettingData. SettingData")
</dt> </dl>

Référence aux données de paramètre d’exportation pour la machine virtuelle. Cette propriété est héritée de la [**\_ ElementSettingData CIM**](/previous-versions/windows/desktop/iscsitarg/cim-elementsettingdata).

</dd> </dl>

## <a name="remarks"></a>Notes

L’accès à la classe **MSVM \_ SystemExportSettingData** peut être limité par le filtrage UAC. Pour plus d’informations, consultez [contrôle de compte d’utilisateur et WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

