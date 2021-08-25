---
description: La table ActionText contient le texte à afficher dans une boîte de dialogue de progression et écrit dans le journal pour les actions dont l’exécution prend beaucoup de temps. Le texte affiché comprend la description de l’action et, éventuellement, les données mises en forme à partir de l’action.
ms.assetid: 88d18422-77d0-4929-9341-d078843cb2a9
title: Table ActionText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f21923588676db4ad38482768a493428ce76caf32b32334e429fbe41335c2bf7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927259"
---
# <a name="actiontext-table"></a>Table ActionText

La table ActionText contient le texte à afficher dans une boîte de dialogue de progression et écrit dans le journal pour les actions dont l’exécution prend beaucoup de temps. Le texte affiché comprend la description de l’action et, éventuellement, les données mises en forme à partir de l’action.

La table ActionText contient les colonnes suivantes.



| Colonne      | Type                         | Clé | Nullable |
|-------------|------------------------------|-----|----------|
| Action      | [Identificateur](identifier.md) | O   | N        |
| Description | [Text](text.md)             | N   | O        |
| Modèle    | [Modèle](template.md)     | N   | O        |



 

## <a name="columns"></a>Colonnes

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Transactionnel
</dt> <dd>

Nom de l'action.

Clé de table primaire.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descriptive
</dt> <dd>

Description localisée affichée dans la boîte de dialogue de progression, ou écrite dans le journal lorsque l’action est en cours d’exécution.

</dd> <dt>

<span id="Template"></span><span id="template"></span><span id="TEMPLATE"></span>Modèle
</dt> <dd>

Modèle de format localisé utilisé pour mettre en forme les enregistrements de données d’action à afficher pendant l’exécution de l’action. Si aucun modèle n’est fourni, les données d’action ne sont pas affichées.

</dd> </dl>

## <a name="remarks"></a>Remarques

En règle générale, les entrées de la table ActionText font référence aux actions des tables de séquence. Le programme d’installation effectue d’autres actions qui ne sont pas répertoriées dans la table de séquence, mais qui doivent toujours être spécifiées dans la table. Le tableau suivant identifie les entrées de table requises pour lesquelles le nom d’action et le modèle doivent être créés exactement comme indiqué, mais la description peut être personnalisée.



| Action          | Description                             | Modèle |
|-----------------|-----------------------------------------|----------|
| Restauration        | Annule des actions.                         | \[1\]    |
| RollbackCleanup | Supprime les anciens fichiers.                      | \[1\]    |
| GenerateScript  | Génère des opérations système pour l’action. | \[1\]    |



 

> [!Note]  
> Le texte d’action s’affiche uniquement pour les actions qui s’exécutent dans le script d’installation. Par conséquent, le texte d’action s’affiche uniquement pour les actions qui sont séquencées entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md) .

 

Vous pouvez importer une table ActionText localisée dans votre base de données à l’aide de Msidb.exe ou [**MsiDatabaseImport**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseimporta). Le kit de développement logiciel (SDK) contient une table ActionText localisée pour chacune des langues listées dans la section [localisation des tables Error et ActionText](localizing-the-error-and-actiontext-tables.md) . Si la table ActionText n’est pas remplie, le programme d’installation charge les chaînes localisées pour la langue spécifiée par la propriété [**ProductLanguage**](productlanguage.md) .

## <a name="validation"></a>Validation

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE46](ice46.md)  
</dl>

 

 



