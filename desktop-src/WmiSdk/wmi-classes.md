---
description: Cette section fournit des informations sur la classe WMI et la page de référence.
ms.assetid: 0110677a-bbba-42f7-8e59-55d83758f70a
ms.tgt_platform: multiple
title: Classes WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1da15af60f1d1a32d652c8776e20ef36d65c1ff158dc6ac7465886361c5862c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757509"
---
# <a name="wmi-classes"></a>Classes WMI

Cette section fournit des informations sur la classe WMI et la page de référence. Pour plus d’informations sur la façon de récupérer des données de classe ou d’instance, consultez [manipulation d’informations de classes et d’instances](manipulating-class-and-instance-information.md). La liste suivante répertorie, décrit et fournit des liens vers des informations spécifiques sur la classe WMI. Pour plus d’informations et des exemples de code de script sur l’utilisation des classes WMI pour obtenir une variété de données de système d’exploitation et de matériel, consultez [tâches WMI pour les scripts et les applications](wmi-tasks-for-scripts-and-applications.md). Pour obtenir des exemples en C++, consultez [exemples d’applications WMI c++](wmi-c---application-examples.md). La [connexion à WMI sur un ordinateur distant](connecting-to-wmi-on-a-remote-computer.md) montre comment obtenir des données distantes. Vous pouvez également utiliser PowerShell pour accéder aux objets WMI. pour obtenir la liste des classes WMI qui incluent des exemples de code PowerShell, voir [ici](https://msdn.microsoft.com/library/tags-cloud.aspx?tag=powershell+code+wmi).



| Section                                                    | Description                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Classes système WMI](wmi-system-classes.md)               | classes prédéfinies incluses dans chaque espace de noms dans le noyau Windows Management Instrumentation (WMI). Vous pouvez reconnaître une classe système WMI, car le nom commence par un trait de soulignement double ( \_ \_ ). Ces classes fournissent une grande partie des fonctionnalités de base pour WMI. les classes système WMI sont similaires aux tables système de SQL server. |
| [Classes MSFT](msft-classes.md)                           | Autres classes Microsoft qui offrent la possibilité de manipuler plusieurs fonctionnalités du système d’exploitation, telles que les événements à distance et les extensions de stratégie. Les classes de [résolution des problèmes WMI](wmi-troubleshooting.md) sont des classes msft qui fournissent des données sur les opérations WMI.                                                                                               |
| [Classes CIM](cimclas.md)                                 | Classes [*de schéma Common Information Model (CIM)*](gloss-c.md) . Si vous souhaitez écrire vos propres classes WMI, vous pouvez hériter d’une ou de plusieurs de ces classes. Les [classes WMI Win32](/windows/desktop/CIMWin32Prov/win32-provider) héritent des classes CIM.                                                                          |
| [Classes de consommateur standard](standard-consumer-classes.md) | Ensemble de consommateurs d’événements WMI qui déclenchent une action lors de la réception d’un événement arbitraire. Pour plus d’informations, consultez [surveillance des événements](monitoring-events.md).                                                                                                                                                                                               |



 

## <a name="wmi-class-scripting-center-code-examples"></a>Exemples de code du centre de script de la classe WMI

Les exemples de code du centre de script suivants affectent plusieurs classes WMI sur plusieurs espaces de noms.



| Lien                                                                                                                                      | Description                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Explorateur WMI de l’interface graphique utilisateur et générateur d’aide de méthode WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/89c759b7-20b4-49e8-98a8-3c8fbdb2dd69) | Exemple de script qui fournit un explorateur WMI GUI et un générateur d’aide de méthode WMI.                                                                                                                                                        |
| [Rechercher dans l’Explorateur WMI espaces de noms WMI](https://Gallery.TechNet.Microsoft.Com/scriptcenter/WMI-Explorer-Search-WMI-cd87e309)                 | Permet aux utilisateurs de rechercher des classes dans tous les espaces de noms disponibles sur les ordinateurs spécifiés. Cet exemple est la présente de la ligne de commande de l’exemple de l’Explorateur WMI GUI et peut être considérée comme une extension de Get-WmiObject-List. |
| [outil d’Administration de système Arposh Windows](https://Gallery.TechNet.Microsoft.Com/scriptcenter/Arposh-Windows-System-a1beb102)            | AWSA a été créé avec l’administrateur système à l’esprit. la résolution des problèmes de Windows nécessite un large éventail d’outils et de connaissances. AWSA regroupe ces outils dans un emplacement central et ajoute des fonctionnalités supplémentaires.       |



 

## <a name="naming-conventions-for-wmi-classes-and-properties"></a>Conventions d’affectation des noms pour les classes et les propriétés WMI

Les noms de propriété doivent être conformes à la syntaxe format MOF (MOF) définie par le DTMF (Distributed Management Task Force). Les caractères d’identificateur initiaux doivent provenir des lettres de a à z et du trait de soulignement ( \_ ). Tous les caractères supplémentaires doivent être compris entre les lettres de a à z, le caractère de soulignement et les chiffres de 0 à 9. Pour plus d’informations, consultez la section utilisation d’Unicode de la [spécification CIM Version 2,2](https://www.dmtf.org/standards/cim).

SQL les mots réservés ne doivent pas être utilisés dans les noms de classe et de propriété. pour obtenir la liste complète des mots réservés SQL et pour plus d’informations, consultez la section instructions de la [spécification CIM Version 2,2](https://www.dmtf.org/standards/cim).

## <a name="document-conventions-for-a-wmi-class-reference-page"></a>Conventions de document pour une page de référence de classe WMI

Cette section identifie et décrit les conventions de document pour une page de référence de classe WMI.

Une page de référence classique contient un bloc de syntaxe, un tableau de méthodes et une liste de propriétés.

-   Bloc de syntaxe

    Version simplifiée du code MOF qui comprend le nom de la classe, la classe parente (le cas échéant) et les propriétés de classe, par ordre alphabétique, avec les types de données.

-   Table des méthodes

    Si une classe a des méthodes, les méthodes sont répertoriées dans le tableau qui suit immédiatement le bloc de syntaxe. Chaque méthode implémentée est liée à une page de référence.

-   Liste Propriétés

    Chaque propriété de classe est listée avec un type de données, un type d’accès (lecture seule ou lecture/écriture), des qualificateurs et une description de la propriété.

## <a name="syntax-block"></a>Bloc de syntaxe

``` syntax
class Win32_xyz : CIM_xyz 
{
  uint16 abc  ;
  string def  ;
};
```

## <a name="methods-table"></a>Table des méthodes



| \_Méthodes Win32 XYZ | Description                                |
|--------------------|--------------------------------------------|
| *SomeMethod*       | Brève description de ce que fait la méthode. |



 

## <a name="properties-list"></a>Liste Propriétés

<dl> <dt>

<span id="abc"></span><span id="ABC"></span>ABC
</dt> <dd>

Type de données : **UInt16**

Type d’accès : indique si vous disposez d’un accès en lecture/écriture ou en lecture seule à cette propriété.

Qualificateurs : le cas échéant, affiche les qualificateurs de la propriété. Par exemple, **Key**, **override**.

Décrit la propriété et fournit des informations d’héritage pour la propriété. Par exemple, cette propriété est héritée de ** \_ CIM* XYZ * * *. Il existe un lien vers la classe parente si Microsoft fournit une implémentation de cette classe. Toutefois, les classes CIM ne sont pas disponibles.

</dd> <dt>

<span id="def"></span><span id="DEF"></span>def
</dt> <dd>

Type de données : **chaîne**

Type d'accès : Lecture seule

Description de la propriété.

</dd> </dl>

## <a name="remarks"></a>Remarques

Fournit plus d’informations sur la classe, le cas échéant. Fournit également des informations de dérivation, le cas échéant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence WMI](wmi-reference.md)
</dt> </dl>

 

 
