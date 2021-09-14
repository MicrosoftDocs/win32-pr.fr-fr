---
description: La table CustomAction fournit les moyens d’intégrer du code personnalisé et des données dans l’installation. La source du code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un fichier exécutable existant.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Table CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091758"
---
# <a name="customaction-table"></a>Table CustomAction

La table CustomAction fournit les moyens d’intégrer du code personnalisé et des données dans l’installation. La source du code exécuté peut être un flux contenu dans la base de données, un fichier récemment installé ou un fichier exécutable existant.

La table CustomAction contient les colonnes suivantes.



| Colonne       | Type                               | Clé | Nullable |
|--------------|------------------------------------|-----|----------|
| Action       | [Identificateur](identifier.md)       | O   | N        |
| Type         | [Integer](integer.md)             | N   | N        |
| Source       | [CustomSource](customsource.md)   | N   | O        |
| Cible       | [Correct](formatted.md)         | N   | O        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l'action. L’action apparaît normalement dans une table de séquence, sauf si elle est appelée par une autre action personnalisée. Si le nom correspond à une action intégrée, l’action personnalisée n’est jamais appelée.

Clé de table primaire.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Entrer
</dt> <dd>

Champ de bits d’indicateur spécifiant le type de base des actions personnalisées et des options. Consultez la [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md) pour obtenir la liste des types de base. Consultez Options de [traitement des retours d’actions](custom-action-return-processing-options.md)personnalisées, [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md), [option cible masquée des actions personnalisées](custom-action-hidden-target-option.md)et [action personnalisée In-Script les options d’exécution](custom-action-in-script-execution-options.md).

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Code
</dt> <dd>

Un nom de propriété ou une clé externe dans une autre table. Pour plus d’informations sur les sources d’action personnalisées possibles, consultez [sources d’action personnalisées](custom-action-sources.md) et [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md). Par exemple, la colonne source peut contenir une clé externe dans la première colonne de l’une des tables suivantes, contenant la source du code d’action personnalisé.

[Table de répertoire](directory-table.md) pour l’appel d’exécutables existants.

[Table de fichiers](file-table.md) pour appeler des exécutables et des dll qui viennent d’être installés.

[Table binaire](binary-table.md) pour appeler des fichiers exécutables, des dll et des données stockées dans la base de données.

[Table de propriétés](property-table.md) permettant d’appeler des exécutables dont les chemins sont détenus par une propriété.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Indicatif
</dt> <dd>

Paramètre d’exécution qui dépend du type de base de l’action personnalisée. Consultez la [liste récapitulative de tous les types d’actions personnalisés](summary-list-of-all-custom-action-types.md) pour obtenir une description de ce qui doit être entré dans ce champ pour chaque type d’action personnalisée. Par exemple, ce champ peut contenir les éléments suivants en fonction de l’action personnalisée.



| Cible                                    | Action personnalisée                         |
|-------------------------------------------|---------------------------------------|
| Point d’entrée (obligatoire)                    | Appel d’une DLL.                        |
| Nom de l’exécutable avec arguments (obligatoire) | Appel d’un fichier exécutable existant.       |
| Arguments de ligne de commande (facultatif)         | Appel d’un exécutable vient d’être installé. |
| Nom du fichier cible (obligatoire)               | Création d’un fichier à partir de données personnalisées.     |
| Null                                      | Exécution du code de script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Entrez la valeur **msidbCustomActionTypePatchUninstall** dans ce champ pour spécifier une action personnalisée avec l' [option action personnalisée désinstaller le correctif](custom-action-patch-uninstall-option.md).

**[Windows Installer 4,0 et versions antérieures](not-supported-in-windows-installer-4-0.md):** Non pris en charge. cette option est disponible à partir de Windows Installer 4,5.

</dd> </dl>

Pour plus d’informations, consultez toutes les rubriques sous [actions personnalisées](custom-actions.md).

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



