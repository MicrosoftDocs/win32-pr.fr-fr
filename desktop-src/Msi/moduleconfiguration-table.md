---
description: La table ModuleConfiguration identifie les attributs configurables du module. Cette table n’est pas fusionnée dans la base de données.
ms.assetid: 3b77cc23-c104-4adc-868c-3aa2b5794bc7
title: Table ModuleConfiguration
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c499e313633d1668db81c91654800d1d5824192839329316f55040fd3bc7bad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963059"
---
# <a name="moduleconfiguration-table"></a>Table ModuleConfiguration

La table ModuleConfiguration identifie les attributs configurables du module. Cette table n’est pas fusionnée dans la base de données.

La table ModuleConfiguration contient les colonnes suivantes.



| Colonne       | Type                         | Clé | Nullable |
|--------------|------------------------------|-----|----------|
| Nom         | [Identificateur](identifier.md) | O   | N        |
| Format       | [Integer](integer.md)       | N   | N        |
| Type         | [Text](text.md)             | N   | O        |
| ContextData  | [Text](text.md)             | N   | O        |
| DefaultValue | [Text](text.md)             | N   | O        |
| Attributs   | [Integer](integer.md)       | N   | O        |
| DisplayName  | [Text](text.md)             | N   | O        |
| Description  | [Text](text.md)             | N   | O        |
| HelpLocation | [Text](text.md)             | N   | O        |
| HelpKeyword  | [Text](text.md)             | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nomme
</dt> <dd>

Ce champ définit le nom de l’élément configurable. Ce nom est référencé dans le modèle de mise en forme dans la colonne valeur de la [table ModuleSubstitution](modulesubstitution-table.md).

</dd> <dt>

<span id="Format"></span><span id="format"></span><span id="FORMAT"></span>Format
</dt> <dd>

Cette colonne spécifie le format des données en cours de modification.



| Format                                       | Valeur |
|----------------------------------------------|-------|
| [Text](text-format-types.md)                | 0     |
| [Clé](key-format-types.md)                  | 1     |
| [Integer](integer-format-types.md)          | 2     |
| [Format de champ de champ](bitfield-format-types.md) | 3     |



 

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Cette colonne spécifie le type des données en cours de modification. Ce type est utilisé pour fournir un contexte pour toute interface utilisateur et n’est pas utilisé dans le processus de fusion. Les valeurs valides pour cette colonne dépendent de la valeur dans la colonne format.

</dd> <dt>

<span id="ContextData"></span><span id="contextdata"></span><span id="CONTEXTDATA"></span>ContextData
</dt> <dd>

Cette colonne spécifie un contexte sémantique pour les données demandées. Le type est utilisé pour fournir un contexte pour toute interface utilisateur et n’est pas utilisé dans le processus de fusion. Les valeurs valides pour cette colonne dépendent des valeurs dans les colonnes format et type.

</dd> <dt>

<span id="DefaultValue"></span><span id="defaultvalue"></span><span id="DEFAULTVALUE"></span>DefaultValue
</dt> <dd>

Cette colonne spécifie une valeur par défaut pour l’élément de cet enregistrement si l’outil de fusion refuse de fournir une valeur. Cette valeur doit avoir le format, le type et le contexte de l’élément. S’il s’agit d’un élément de format « clé », la clé étrangère doit être une clé valide dans les tables du module. La valeur NULL peut être une valeur valide pour cette colonne en fonction de l’élément. Pour les éléments de format « clé », cette valeur est au [format spécial CMSM](cmsm-special-format.md). Pour tous les autres types, la valeur est traitée littéralement.

Les auteurs de modules doivent s’assurer que le module est valide dans son état par défaut. Cela permet de s’assurer que les versions de Mergemod.dll antérieures à la version 2,0 peuvent toujours utiliser le module dans son état par défaut.

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributs
</dt> <dd>

Cette colonne est un champ de bits contenant des attributs pour cet élément configurable. NULL équivaut à 0. Tous les autres éléments de cette colonne sont réservés pour une utilisation ultérieure et doivent avoir la valeur 0.



| Nom                             | Decimal | Valeur hexadécimale | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------------------|---------|-------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| msmConfigurableOptionKeyNoOrphan | 1       | 0x00000001  | Cet attribut s’applique uniquement aux enregistrements qui répertorient une clé étrangère dans une table de module dans leur champ DefaultValue. L’outil de fusion ignore l’attribut pour tous les formats autres que les [types de format de clé](key-format-types.md). Les éléments qui ne sont pas répertoriés dans la [table ModuleSubstitution](modulesubstitution-table.md) sont exclus de la vérification suivante. L’outil de fusion ne fusionne pas la ligne référencée par la colonne DefaultValue dans la base de données cible si les conditions suivantes sont respectées après avoir effectué toutes les options de configuration.<br/> Chaque ligne de la table ModuleConfiguration avec la même valeur DefaultValue a le msmConfigurationItemsKeyNoOrphan défini.<br/> Aucune ligne n’utilise DefaultValue, car l’outil de création a refusé de fournir une valeur.<br/> L’outil de fusion fusionne la ligne si l’une des conditions suivantes est satisfaite.<br/> L’outil de fusion recherche toutes les lignes qui n’ont pas de msmConfigItemsKeyNoOrphan définie.<br/> Si l’outil de fusion détecte une ligne à l’aide de DefaultValue, car l’outil de création a refusé de fournir une valeur.<br/> |
| msmConfigurableOptionNonNullable | 2       | 0x00000002  | Lorsque cet attribut est défini, la valeur NULL n’est pas une réponse valide pour cet élément. Cet attribut n’a aucun effet pour les types de [format entier](integer-format-types.md) ou les [types de format de champ](bitfield-format-types.md)de type de champ.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

<span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>NomComplet
</dt> <dd>

Cette colonne fournit une brève description de cet élément que l’outil de création peut utiliser dans l’interface utilisateur. Cette colonne ne peut pas être localisée. Affectez la valeur null à cette colonne pour que le module demande que l’outil de création n’expose pas cette propriété dans l’interface utilisateur. L’outil peut ignorer la valeur de ce champ.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Cette colonne fournit une description de cet élément que l’outil de création peut utiliser dans les éléments d’interface utilisateur. Cette chaîne peut être localisée par la transformation de langage du module. Cette colonne peut être null.

</dd> <dt>

<span id="HelpLocation"></span><span id="helplocation"></span><span id="HELPLOCATION"></span>HelpLocation
</dt> <dd>

Cette colonne fournit le nom d’un fichier d’aide (sans l’extension. chm) ou une liste délimitée par des points-virgules des espaces de noms d’aide. Cette colonne peut être null si aucune aide n’est disponible. Cette colonne peut être NULL uniquement si la colonne HelpKeyword a la valeur null.

</dd> <dt>

<span id="HelpKeyword"></span><span id="helpkeyword"></span><span id="HELPKEYWORD"></span>HelpKeyword
</dt> <dd>

Cette colonne fournit un mot clé dans le fichier d’aide ou l’espace de noms de la colonne HelpLocation. L’interprétation de ce mot clé dépend de la colonne HelpLocation. Cette colonne peut être null.

</dd> </dl>

## <a name="remarks"></a>Remarques

La table ModuleConfiguration est utilisée par les [modules de fusion configurables](configurable-merge-modules.md). Mergemod.dll 2,0 ou version ultérieure est requis pour créer un module de fusion configurable.

Pour garantir la compatibilité avec les versions antérieures de Mergemod.dll, la table ModuleConfiguration et la [table ModuleSubstitution](modulesubstitution-table.md) doivent être ajoutées à la [table ModuleIgnoreTable](moduleignoretable-table.md) de chaque module.

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE25](ice25.md)  
[ICE45](ice45.md)  
</dl>

 

 




