---
description: Représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique (CIM CIM \_ ).
ms.assetid: e34c9b00-2723-4858-805e-5e3e51a5dfd2
title: Classe CIM_BIOSElement (gestion Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BIOSElement
- CIM_BIOSElement.Version
- CIM_BIOSElement.Manufacturer
- CIM_BIOSElement.PrimaryBIOS
- CIM_BIOSElement.ListOfLanguages
- CIM_BIOSElement.CurrentLanguage
- CIM_BIOSElement.LoadedStartingAddress
- CIM_BIOSElement.LoadedEndingAddress
- CIM_BIOSElement.LoadUtilityInformation
- CIM_BIOSElement.ReleaseDate
- CIM_BIOSElement.RegistryURIs
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 78f2433d2b75e2c348fdf6e7a8ff35db56c9a0c8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122879878"
---
# <a name="cim_bioselement-class-hyper-v-management"></a>Classe CIM_BIOSElement (gestion Hyper-V)

Représente le logiciel de bas niveau qui est chargé dans un stockage non volatile et utilisé pour démarrer et configurer un système informatique ([**CIM CIM \_**](cim-computersystem.md)).

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.17.0"), UMLPackagePath("CIM::Application::BIOS"), AMENDMENT]
class CIM_BIOSElement : CIM_SoftwareElement
{
  string   Version;
  string   Manufacturer;
  boolean  PrimaryBIOS;
  string   ListOfLanguages[];
  string   CurrentLanguage;
  uint64   LoadedStartingAddress;
  uint64   LoadedEndingAddress;
  string   LoadUtilityInformation;
  datetime ReleaseDate;
  string   RegistryURIs[];
};
```

## <a name="members"></a>Membres

La classe **CIM \_ BIOSElement** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ BIOSElement** possède les propriétés suivantes.

<dl> <dt>

**CurrentLanguage**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BIOSElement**.**ListOfLanguages**")
</dt> </dl>

Langue actuellement sélectionnée pour le BIOS. Ces informations peuvent être obtenues à partir de System Management BIOS (SMBIOS) à l’aide de l’attribut de langage actuel de la structure de type 13 à indexer dans la liste de chaînes qui suit la structure. Cette propriété est mise en forme à l’aide du nom de langue ISO 639 et peut être suivie par le nom du secteur ISO 3166 et la méthode d’encodage.

</dd> <dt>

**ListOfLanguages**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Liste des langues installables pour le BIOS. Ces informations peuvent être obtenues à partir de SMBIOS, à partir de la liste de chaînes qui suit la structure type 13. Un nom de langue ISO 639 doit être utilisé pour spécifier les langues installables du BIOS. Le nom du secteur ISO 3166 et la méthode d’encodage peuvent également être spécifiés, en suivant le nom de la langue.

</dd> <dt>

**LoadedEndingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,6»)
</dt> </dl>

Adresse de fin de la mémoire occupée par le BIOS.

</dd> <dt>

**LoadedStartingAddress**
</dt> <dd> <dl> <dt>

Type de données : **UInt64**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,5»)
</dt> </dl>

Adresse de début de la mémoire occupée par le BIOS.

</dd> <dt>

**LoadUtilityInformation**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,7»)
</dt> </dl>

Chaîne de forme libre qui décrit l’utilitaire Flash/chargement BIOS requis pour mettre à jour l’objet **CIM \_ BIOSElement** . La version et d’autres informations peuvent être indiquées dans cette propriété.

</dd> <dt>

**Fabricant**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Manufacturer"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,2»)
</dt> </dl>

Fabricant de l’élément logiciel.

</dd> <dt>

**PrimaryBIOS**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,9»)
</dt> </dl>

True s’il s’agit du BIOS principal du système informatique ; Sinon, false.

</dd> <dt>

**RegistryURIs**
</dt> <dd> <dl> <dt>

Type de données : tableau de **chaînes**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Emplacement de publication des registres des attributs BIOS auxquels l’implémentation du BIOS est conforme.

</dd> <dt>

**ReleaseDate**
</dt> <dd> <dl> <dt>

Type de données : **DateTime**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,8»)
</dt> </dl>

Date à laquelle ce BIOS a été publié.

</dd> <dt>

**Version**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("version"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|BIOS système DMTF \| 001,3»)
</dt> </dl>

Version de l’opération. La version de l’opération doit se présenter sous l’une des formes suivantes :

-   *&lt; majeure &gt;**. &lt; mineure &gt;*. *&lt; révision &gt;*
-   *&lt; majeure &gt;**. &lt; &gt; &lt; &gt; &lt; révision &gt; de la lettre secondaire*

</dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SOFTWAREELEMENT CIM**](cim-softwareelement.md)
</dt> </dl>

 

