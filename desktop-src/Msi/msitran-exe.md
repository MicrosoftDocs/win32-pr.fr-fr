---
description: Msitran.exe utilise MsiDatabaseGenerateTransform, MsiCreateTransformSummaryInfo et MsiDatabaseApplyTransform pour générer ou appliquer un fichier de transformation. Cet outil est disponible uniquement dans les composants SDK Windows pour les développeurs Windows Installer.
ms.assetid: cfc7b907-78d7-4a78-bab4-ede9012d5a36
title: Msitran.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a69936155fb3880f43e0f7563bc6aabd59f53703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529365"
---
# <a name="msitranexe"></a>Msitran.exe

Msitran.exe utilise [**MsiDatabaseGenerateTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasegeneratetransforma), [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)et [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) pour générer ou appliquer un fichier de transformation.

Cet outil est disponible uniquement dans les [composants SDK Windows pour les développeurs Windows Installer](platform-sdk-components-for-windows-installer-developers.md).

## <a name="syntax"></a>Syntaxe

Pour générer une transformation, utilisez la syntaxe ci-après.

**msitran-g** *{base dB} {ref DB} {nom du fichier de transformation} \[ {conditions d’erreur/ \] conditions de validation}*

Pour appliquer une transformation, utilisez la syntaxe ci-après.

**msitran-a** *{transformer} {base de données} \[ {conditions \] d’erreur}*

## <a name="command-line-options"></a>Options de la ligne de commande

Msitran.exe utilise les options de ligne de commande suivantes qui ne respectent pas la casse. Un séparateur de barre oblique peut également être utilisé à la place d’un tiret.



| Option | Description            |
|--------|------------------------|
| -g     | Génération de transformation.  |
| -a     | Transformation de l’application. |



 

Les erreurs suivantes peuvent être supprimées lors de l’application d’une transformation. Pour supprimer une erreur, incluez le caractère approprié dans l’argument {condition d’erreur}. Les conditions spécifiées avec-g sont placées dans les informations récapitulatives de la transformation, mais ne sont pas utilisées lors de l’application d’une transformation avec-a. Pour plus d’informations, consultez [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma).



| Option | Erreur supprimée           |
|--------|----------------------------|
| a      | Ajoutez une ligne existante.          |
| b      | Supprimer une ligne non existante.   |
| c      | Ajoutez une table existante.        |
| d      | Supprime une table non existante. |
| e      | Modifiez la ligne existante.       |
| f      | Modifiez la page de codes.           |



 

Les conditions de validation suivantes peuvent être utilisées pour indiquer qu’une transformation peut être appliquée à un package. Ces conditions peuvent être spécifiées avec-g, mais pas-a.



| Option | Condition de validation                                  |
|--------|-------------------------------------------------------|
| g      | Vérifiez le code de mise à niveau.                                   |
| l      | Vérifiez la langue.                                       |
| p      | Vérifiez la plateforme.                                       |
| r      | Vérifiez le produit.                                        |
| s      | Vérifiez uniquement la version principale.                             |
| t      | Vérifiez uniquement les versions majeures et mineures.                  |
| u      | Vérifiez les versions majeure, mineure et de mise à niveau.             |
| v      | Version de base de données appliquée < version de base de données de base.  |
| w      | Version de base de données appliquée <= version de base de données de base. |
| x      | Version de base de données appliquée = version de base de la base de données.     |
| y      | Version de base de données appliquée >= version de base de données de base. |
| z      | Version de base de données appliquée > version de base de données de base.  |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Outils de développement Windows Installer](windows-installer-development-tools.md)
</dt> <dt>

[Transformations de base de données](database-transforms.md)
</dt> <dt>

[Exemple de transformation de personnalisation](a-customization-transform-example.md)
</dt> <dt>

[Versions, outils et redistribuables publiés](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



