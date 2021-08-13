---
description: La table de signatures contient les informations qui identifient de façon unique une signature de fichier. pour plus d’informations sur les signatures, consultez signatures numériques et Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Table de signature
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ddda5c501b24e12498f356c10a1aa2a3549426daca5e4cc3c19c1f62ed04cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624646"
---
# <a name="signature-table"></a>Table de signature

La table de signatures contient les informations qui identifient de façon unique une signature de fichier. pour plus d’informations sur les signatures [, consultez signatures numériques et Windows Installer](digital-signatures-and-windows-installer.md).

La table de signatures contient les colonnes suivantes.



| Colonne     | Type                               | Clé | Nullable |
|------------|------------------------------------|-----|----------|
| Signature  | [Identificateur](identifier.md)       | O   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | O        |
| MaxVersion | [Text](text.md)                   | N   | O        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | O        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | O        |
| À l’esprit    | [DoubleInteger](doubleinteger.md) | N   | O        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | O        |
| Langages  | [Text](text.md)                   | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature
</dt> <dd>

La colonne signature est une signature de fichier unique.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Extension
</dt> <dd>

Nom du fichier.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

Version minimale du fichier, avec une comparaison de langage. Si ce champ est spécifié, le fichier doit avoir une version qui est au moins égale à MinVersion. Si le fichier a une version égale à la valeur du champ MinVersion, mais que la langue spécifiée dans la colonne languages diffère, le fichier ne répond pas aux critères de filtre de signature.

> [!Note]  
> La langue spécifiée dans la colonne langues est utilisée dans la comparaison et il n’existe aucun moyen d’ignorer la langue. Si vous souhaitez qu’un fichier respecte la spécification de champ MinVersion, quelle que soit la langue, vous devez entrer une valeur dans le champ MinVersion qui est inférieure d’une unité à la valeur réelle. Par exemple, si la version minimale du filtre est 2.0.2600.1183, utilisez 2.0.2600.1182 pour rechercher le fichier sans faire correspondre les informations de langue.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Version maximale du fichier. Si ce champ est spécifié, le fichier doit avoir une version qui est au plus égale à MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Taille minimale du fichier. Si ce champ est spécifié, le fichier sous inspection doit avoir une taille au moins égale à MinSize. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize
</dt> <dd>

Taille maximale du fichier. Si ce champ est spécifié, le fichier sous inspection doit avoir une taille qui est au plus égale à MaxSize. Il doit s’agir d’un nombre non négatif.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>À l’esprit
</dt> <dd>

Date et heure de la modification minimale du fichier. Si ce champ est spécifié, le fichier en cours d’inspection doit avoir une date et une heure de modification au moins égales à l’MinDate. Il doit s’agir d’un nombre non négatif. Le format de ce champ est deux valeurs 16 bits compressées de type **Word**. La valeur de **mot** de poids fort spécifie la date au format de date ms-dos. La valeur de **mot** de poids faible spécifie l’heure au format de temps ms-dos. La valeur 0 pour la valeur d’heure représente minuit. Consultez la section Notes.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

Date de création maximale du fichier. Si ce champ est spécifié, le fichier sous inspection doit avoir une date de création qui est au plus égale à MaxDate. Il doit s’agir d’un nombre non négatif. Le format de ce champ est deux valeurs 16 bits compressées de type **Word**. La valeur de **mot** de poids fort spécifie la date au format de date ms-dos. La valeur de **mot** de poids faible spécifie l’heure au format de temps ms-dos. La valeur 0 pour la valeur d’heure représente minuit. Consultez la section Notes.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Traduction
</dt> <dd>

Langues prises en charge par le fichier.

</dd> </dl>

## <a name="remarks"></a>Remarques

Cette table est utilisée avec la [table AppSearch](appsearch-table.md).

La signature est recherchée à l’aide de la [table RegLocator](reglocator-table.md), de la table [IniLocator](inilocator-table.md), de la table [CompLocator](complocator-table.md)et de la [table DrLocator](drlocator-table.md). Les colonnes de cette table ne sont généralement pas localisées. Si un auteur décide de rechercher des produits dans plusieurs langues, il peut y avoir une entrée distincte incluse dans le tableau pour chaque langue.

la table de signatures suit généralement les [règles](file-versioning-rules.md)de contrôle de version de fichier Windows Installer. Les langues spécifiées dans la colonne languages de la table de signature ne sont pas évaluées à moins que les versions de fichiers soient équivalentes. La colonne languages permet de garantir qu’un fichier est d’une langue particulière s’il s’agit de la version demandée. Aucune méthode n’est disponible pour ignorer la colonne languages. Une valeur NULL entrée dans la colonne Languages est traitée comme un fichier sans langage et ne correspond pas à la signature de fichier d’un fichier dont la langue apparaît dans la table de signature. L’exemple suivant recherche une version particulière de MSI.DLL.

[Table DrLocator](drlocator-table.md)

| Signature\_ | Parent | Chemin                  | Profondeur |
|-------------|--------|-----------------------|-------|
| MsiDll      | nul | c : \\ Windows \\ system32 | 0     |



 

[Table AppSearch](appsearch-table.md)



| Propriété | Signature\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Table de signature



| Signature | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | À l’esprit | MaxDate | Langages |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | nul     | nul  | nul  | nul  | nul  | 0         |



 

dans ce cas, et sur Windows XP SP1, l' [action AppSearch](appsearch-action.md) définit MSIDLL sur c : \\ Windows \\ system32 \\msi.dll, car MSI.DLL est un fichier indépendant de la langue. Si la valeur de la colonne Languages est modifiée de 0 à 1033, l’action AppSearch ne parvient pas à trouver le msi.dll correspondant et la propriété MSIDLL n’est pas définie.

Vous ne pouvez pas utiliser la table de signatures pour effectuer une requête sur des langues uniquement. Pour rechercher les différentes versions linguistiques d’un fichier, vous devez disposer d’une entrée distincte dans la table de signatures pour chaque version de langue. Si plusieurs langues sont fournies dans la colonne Languages, la recherche porte sur un fichier qui prend en charge toutes ces langues.

Le format des colonnes MinDate et MaxDate est deux valeurs 16 bits compressées de type **Word**.

**Mot** de date



| Bits | Content                                             |
|------|-----------------------------------------------------|
| 0 – 4  | Jour du mois (1-31)                             |
| 5-8  | Month (1 = janvier, 2 = février, etc.)        |
| 9-15 | Décalage d’année à partir de 1980 (Ajouter 1980 pour atteindre l’année réelle) |



 

**Mot** de temps



| Bits  | Content                     |
|-------|-----------------------------|
| 0 – 4   | Secondes divisées par 2        |
| 5-10  | Minutes (0-59)              |
| 11-15 | Heure (de 0 à 23 sur 24 heures) |



 

La formule permettant de calculer les valeurs des champs MinDate et MaxDate est la suivante :

((Année-1980) \* 512 + mois \* 32 + jour) \* 65536 + heures \* 2048 + minutes \* 32 + secondes/2

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



