---
description: ICE40 effectue une validation diverse.
ms.assetid: 1f2ba2a1-0170-4434-88fd-a5d1ca8b67c4
title: ICE40
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17617fe5748fcba5ae0edab414ad1bc83c2e5c22
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021561"
---
# <a name="ice40"></a>ICE40

ICE40 effectue une validation diverse.

## <a name="result"></a>Résultats

ICE40 publie des avertissements sur les éléments suivants :

-   La propriété [**REINSTALLMODE**](reinstallmode.md) a été substituée.
-   La [table RemoveIniFile](removeinifile-table.md) possède une entrée de balise DELETE sans valeur.
-   La [table d’erreurs](error-table.md) est manquante dans le fichier .msi et la propriété de [**Résumé du nombre de pages**](page-count-summary.md) est inférieure ou égale à 100. cet avertissement ICE est obsolète, car Windows Installer ne requiert pas que le package ait une table d’erreurs. Les messages d’erreur peuvent être récupérés à l’aide de Msimsg.dll.

## <a name="example"></a>Exemple

[Table de propriétés](property-table.md)



| Propriété                               | Valeur |
|----------------------------------------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | Un     |



 

[Table RemoveIniFile](removeinifile-table.md)



| RemoveIniFile                          | Action | Valeur |
|----------------------------------------|--------|-------|
| [**REINSTALLMODE**](reinstallmode.md) | 4      |       |



 

## <a name="results"></a>Résultats

ICE40 signale les erreurs suivantes.



| Erreur ICE40                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**REINSTALLMODE**](reinstallmode.md) est défini dans la table de propriétés. Cela peut entraîner des difficultés. | La définition de la propriété [**REINSTALLMODE**](reinstallmode.md) dans .msi fichier peut entraîner un comportement inattendu. Pour corriger cette erreur, ne définissez pas cette propriété.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| L’entrée RemoveIniFile Remove1 doit avoir une valeur, car l’action est « supprimer la balise » (4).                | Il existe une action supprimer la balise dans la colonne RemoveIniFile de la [table RemoveIniFile](removeinifile-table.md) sans spécifier de balise à supprimer dans la colonne valeur.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| La table d’erreurs est manquante. Seuls les messages d’erreur numériques seront générés.                              | cet avertissement ICE est obsolète, car Windows Installer ne requiert pas que le package ait une [table d’erreurs](error-table.md). Les messages d’erreur peuvent être récupérés à l’aide de Msimsg.dll.<br/> Cet avertissement signifie que la [table d’erreurs](error-table.md) est manquante dans le fichier .msi et que la propriété de [**Résumé du nombre de pages**](page-count-summary.md) est inférieure ou égale à 100. <br/> pour corriger cette erreur, utilisez une version actuelle du Windows Installer ou ajoutez une table d’erreurs au package d’installation et créez des modèles de mise en forme dans la colonne Message pour les messages d’erreur.<br/> |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 




