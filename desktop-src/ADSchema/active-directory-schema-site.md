---
title: Terminologie relative au schéma Active Directory
description: Les termes suivants sont couramment utilisés pour faire référence au schéma Active Directory.
ms.assetid: 22c5756f-d663-4cb7-aab0-956b22a01e9d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2b48256d1df8f9c344fe0acceb2fb6a70ed3033260baea4db7df44dd71e1c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117836435"
---
# <a name="active-directory-schema-terminology"></a>Terminologie relative au schéma Active Directory

Les termes suivants sont couramment utilisés pour faire référence au schéma Active Directory.


<dl> <dt>

<span id="Attribute"></span><span id="attribute"></span><span id="ATTRIBUTE"></span>Attribut
</dt> <dd>

Éléments de données utilisés pour décrire les objets qui sont représentés par les classes définies dans le schéma. Les attributs sont définis dans le schéma séparément des classes ; Cela permet d’appliquer une définition d’attribut unique à de nombreuses classes. Par exemple, [**Description**](a-description.md) est un attribut qui peut être appliqué à n’importe quelle classe dans le schéma. L’attribut **Description** est défini une fois dans le schéma, garantissant la cohérence, au lieu d’avoir une définition différente pour la **Description** d’un utilisateur et la **Description** d’une imprimante.

> [!Note]  
> Le terme *propriété* est fréquemment utilisé de façon interchangeable avec le terme *attribut*.

 

</dd> <dt>

<span id="Attribute_Instance"></span><span id="attribute_instance"></span><span id="ATTRIBUTE_INSTANCE"></span>Instance d’attribut
</dt> <dd>

Occurrence d’un attribut défini dans le schéma. Ce terme est utilisé pour faire la distinction entre la définition d’un attribut et une occurrence discrète de l’attribut. Par exemple, le stockage d’un objet utilisateur pour « Jeff Smith » avec l’attribut [**Common-Name**](a-cn.md) défini sur « Jeff Smith » crée une instance de [**nom commun**](a-cn.md).

</dd> <dt>

<span id="Class"></span><span id="class"></span><span id="CLASS"></span>Type
</dt> <dd>

Description formelle d’un type d’objet discret et identifiable stocké dans le service d’annuaire. Par exemple, l' [**utilisateur**](c-user.md), la [**file d’attente d’impression et le**](c-printqueue.md) [**groupe**](c-group.md) sont toutes des classes. En outre, il existe trois catégories de classes distinctes : les [classes structurelles](classes-structural.md), les [classes abstraites](classes-abstract.md)et les [classes auxiliaires](classes-auxiliary.md).

</dd> <dt>

<span id="Class_Instance"></span><span id="class_instance"></span><span id="CLASS_INSTANCE"></span>Instance de classe
</dt> <dd>

Occurrence d’une classe définie dans le schéma. Ce terme est utilisé pour faire la distinction entre la définition d’une classe et une occurrence discrète de la classe. Par exemple, le stockage d’un objet [**utilisateur**](c-user.md) pour « Jeff Smith » dans le service d’annuaire crée une instance de l' [**utilisateur**](c-user.md).

</dd> <dt>

<span id="Content_Rules"></span><span id="content_rules"></span><span id="CONTENT_RULES"></span>Règles de contenu
</dt> <dd>

Définition du contenu possible des instances de classe stockées dans le service d’annuaire. Dans les services d’annuaire NT (NTDS), sur lesquels Active Directory est basé, les règles de contenu sont entièrement exprimées par les attributs [**« doit contenir »**](a-mustcontain.md) et [**« peut contenir »**](a-maycontain.md) des définitions de schéma pour chaque classe.

</dd> <dt>

<span id="Derivation"></span><span id="derivation"></span><span id="DERIVATION"></span>Dérivation
</dt> <dd>

Consultez *héritage*.

</dd> <dt>

<span id="Directory_Information_Tree"></span><span id="directory_information_tree"></span><span id="DIRECTORY_INFORMATION_TREE"></span>Arborescence d’informations de répertoire
</dt> <dd>

Le répertoire lui-même, représenté sous la forme d’une arborescence dans laquelle les vertex sont les entrées de répertoire (instances de classe) et les lignes de connexion sont les relations parent-enfant entre les entrées.

</dd> <dt>

<span id="DIT"></span><span id="dit"></span>DIT
</dt> <dd>

Consultez *arborescence des informations de répertoire*.

</dd> <dt>

<span id="Control_Access_Rights"></span><span id="control_access_rights"></span><span id="CONTROL_ACCESS_RIGHTS"></span>Contrôler les droits d’accès
</dt> <dd>

Classe qui décrit un droit d’accès non lié à une ressource, mais une action. Par exemple, un utilisateur peut se voir accorder le droit de créer des valeurs d’ID relatives.

</dd> <dt>

<span id="Inheritance"></span><span id="inheritance"></span><span id="INHERITANCE"></span>Inheritance
</dt> <dd>

Possibilité de créer de nouvelles classes d’objets à partir de classes d’objets existantes. Le nouvel objet est défini en tant que sous- *classe* de l’objet parent. L’objet parent devient une *superclasse* du nouvel objet. Une sous-classe hérite des attributs du parent, y compris les règles de structure et les règles de contenu.

</dd> <dt>

<span id="LDAP"></span><span id="ldap"></span>LDAP
</dt> <dd>

Voir *protocole LDAP (Lightweight Directory Access*).

</dd> <dt>

<span id="Lightweight_Directory_Access_Protocol"></span><span id="lightweight_directory_access_protocol"></span><span id="LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL"></span>Protocole d’accès à Lightweight Directory
</dt> <dd>

Protocole de communication Internet standard utilisé pour communiquer avec le NTDS. LDAP version 2 et version 3 sont pris en charge.

</dd> <dt>

<span id="NT_Security_Descriptor"></span><span id="nt_security_descriptor"></span><span id="NT_SECURITY_DESCRIPTOR"></span>Descripteur de sécurité NT
</dt> <dd>

Consultez *descripteur de sécurité*.

</dd> <dt>

<span id="Object"></span><span id="object"></span><span id="OBJECT"></span>Dessin
</dt> <dd>

Unité de stockage des données dans le service d’annuaire. Les objets de service d’annuaire ne doivent pas être confondus avec les objets COM ou d’autres objets système orientés objet, qui ont un comportement de composant exécutable et au moment de l’exécution. Les objets de service d’annuaire contiennent uniquement des données. Un objet de service d’annuaire est défini par un objet de [**schéma de classe**](c-classschema.md) et un groupe d’objets de [**schéma d’attribut**](c-attributeschema.md) référencés par l’objet de schéma de [**classe**](c-classschema.md) .

Les objets de schéma de [**classe**](c-classschema.md) et d’attribut sont eux [**-**](c-attributeschema.md) mêmes des objets de service d’annuaire et ont des définitions dans le schéma comme tout autre objet. Consultez la *classe*.

</dd> <dt>

<span id="Object_Identifier"></span><span id="object_identifier"></span><span id="OBJECT_IDENTIFIER"></span>Identificateur d’objet
</dt> <dd>

Valeurs numériques uniques, émises par différentes autorités émettrices, pour identifier de manière unique les éléments de données, les syntaxes et diverses autres parties des applications distribuées. Les identificateurs d’objet (OID) sont disponibles dans les applications OSI, les répertoires X. 500, SNMP et d’autres applications pour lesquelles l’unicité est importante. Les OID sont basés sur une arborescence, dans laquelle une autorité de délivrance supérieure, telle que l’ISO, alloue une branche de l’arbre à une sous-autorité qui, à son tour, peut allouer des sous-branches.

Dans le fichier NTDS, les OID incluent certains émis par le fichier ISO pour les classes et les attributs X. 500, et certains émis par Microsoft. La notation OID est une chaîne de nombres en pointillés, par exemple « 1.2.840.113556.1.5.4 », qui se traduit comme indiqué dans la liste suivante. 

| Valeur  | Description                                                                                  |
|--------|----------------------------------------------------------------------------------------------|
| 1      | ISO : « autorité racine », a émis « 1,2 » à ANSI, qui à son tour...                           |
| 2      | ANSI... a émis « 1.2.840 » aux États-Unis, qui à son tour...                                            |
| 840    | ÉTATS-UNIS... a émis « 1.2.840.113556 » à Microsoft...                                               |
| 113556 | Microsoft... où Microsoft gère en interne plusieurs branches OID sous « 1.2.840.113556 ». |
| 1      | Microsoft DS                                                                                 |
| 5      | Classes NTDS                                                                                 |
| 4      | Builtin-Domain                                                                               |



 

</dd> <dt>

<span id="OID"></span><span id="oid"></span>OID
</dt> <dd>

Consultez *identificateur d’objet*.

</dd> <dt>

<span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>Schéma
</dt> <dd>

Définition formelle du contenu et de la structure du service d’annuaire. Le schéma définit tous les attributs et les classes. Pour chaque classe, les attributs [**Poss-Superior**](a-posssuperiors.md), [**doit contenir**](a-mustcontain.md)et [**peut contenir**](a-maycontain.md) sont définis. [**Poss-Superior**](a-posssuperiors.md) définit les structures d’arborescence possibles pour le service d’annuaire en spécifiant les classes qui peuvent être le parent d’une classe donnée. [**Contains**](a-mustcontain.md) et [**Contains Contains**](a-maycontain.md) répertorient les attributs d’une classe qui doivent être présents pour stocker la classe et les attributs supplémentaires éventuellement présents.

</dd> <dt>

<span id="Security_Descriptor"></span><span id="security_descriptor"></span><span id="SECURITY_DESCRIPTOR"></span>Descripteur de sécurité
</dt> <dd>

Informations sur la propriété d’un objet et les autorisations dont disposent les autres utilisateurs sur cet objet. La propriété [**NT-Security-Descriptor**](a-ntsecuritydescriptor.md) d’une entrée de schéma contient une chaîne qui représente le descripteur de sécurité de l’objet. Pour plus d’informations sur le format des informations contenues dans ce champ, consultez [format de chaîne du descripteur de sécurité](/windows/desktop/SecAuthZ/security-descriptor-string-format).

</dd> <dt>

<span id="Structure_Rules"></span><span id="structure_rules"></span><span id="STRUCTURE_RULES"></span>Règles de structure
</dt> <dd>

Définition de la ou des structures d’arborescence possibles. Dans le NTDS, les règles de structure sont entièrement exprimées par l’attribut Poss-Superior présent sur chaque objet de [**schéma de classe**](c-classschema.md) . Consultez *schéma*.

</dd> <dt>

<span id="Subclass"></span><span id="subclass"></span><span id="SUBCLASS"></span>Sous-classe
</dt> <dd>

Objet de [**schéma de classe**](c-classschema.md) qui hérite d’un autre objet de schéma de [**classe**](c-classschema.md) . Consultez *héritage*.

</dd> <dt>

<span id="Superclass"></span><span id="superclass"></span><span id="SUPERCLASS"></span>Superclasse
</dt> <dd>

Objet de [**schéma de classe**](c-classschema.md) à partir duquel un ou plusieurs autres objets de schéma de [**classe**](c-classschema.md) héritent. Consultez *héritage*.

</dd> <dt>

<span id="Tree"></span><span id="tree"></span><span id="TREE"></span>Arbres
</dt> <dd>

Consultez *arborescence des informations de répertoire*.

</dd> <dt>

<span id="X.500"></span><span id="x.500"></span>X. 500
</dt> <dd>

Famille de normes développées conjointement par l’ISO et l’ITU, anciennement appelée CCITT, qui spécifient l’affectation de noms, la représentation des données et les protocoles de communication pour un service d’annuaire.

</dd> </dl>

 

 