---
description: Une transformation est une collection de modifications appliquées à une installation. En appliquant une transformation à un package d’installation de base, le programme d’installation peut ajouter ou remplacer des données dans la base de données d’installation. Le programme d’installation ne peut appliquer que des transformations au cours d’une installation.
ms.assetid: 1edc5227-70ac-4769-ab7f-67d01031dc33
title: À propos des transformations
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcbae9f21ec71209116f3c8eadffca20381cfe71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202569"
---
# <a name="about-transforms"></a>À propos des transformations

Une transformation est une collection de modifications appliquées à une installation. En appliquant une transformation à un package d’installation de base, le programme d’installation peut ajouter ou remplacer des données dans la base de données d’installation. Le programme d’installation ne peut appliquer que des transformations au cours d’une installation.

Le programme d’installation enregistre une liste des transformations requises par le produit pendant l’installation. Le programme d’installation doit appliquer ces transformations au package d’installation du produit lors de la configuration ou de l’installation du produit. Si une transformation indiquée n’est pas disponible et que la résilience de la source de transformation ne peut pas la restaurer, l’installation échoue.

Une transformation peut modifier les informations qui se trouvent dans n’importe quelle table persistante dans la [base de données du programme d’installation](installer-database.md). Une transformation peut également ajouter ou supprimer des tables persistantes dans la base de données du programme d’installation. Les transformations ne peuvent pas modifier les éléments d’un package d’installation qui ne se trouvent pas dans une table de base de données, tels que les informations du [flux d’informations de synthèse](summary-information-stream.md), les informations contenues dans les sous-stockages ou les fichiers des armoires incorporées.

Les transformations ont un flux d’informations de synthèse qui peut contenir des conditions de validation et des conditions d’erreur. La validation de transformation et les conditions d’erreur peuvent être ajoutées aux informations de résumé à l’aide de la fonction [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa) . Les conditions de validation contrôlent si le programme d’installation peut appliquer la transformation à une base de données d’installation donnée. La validation de la transformation peut être conditionnée sur les valeurs des propriétés [**UpgradeCode**](upgradecode.md), [**ProductCode**](productcode.md), [**ProductVersion**](productversion.md) et [**ProductLanguage**](productlanguage.md) spécifiées dans la transformation et celles de la base de données d’installation. Les conditions d’erreur de transformation contrôlent les erreurs qui sont supprimées lorsque la transformation est appliquée. Les conditions d’erreur incluses dans la transformation sont remplacées par les conditions d’erreur spécifiées à l’aide des méthodes [**MsiDatabaseApplyTransform**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabaseapplytransforma) et [**ApplyTransform**](database-applytransform.md) .

> [!Note]  
> Les transformations de personnalisation typiques n’ont aucune condition de validation ni ne sont validées par rapport à [**ProductCode**](productcode.md). Les transformations stockées dans les [packages de correctifs](patch-packages.md) ont généralement des conditions de validation strictes pour s’assurer que la transformation appropriée est appliquée à la cible du correctif.

 

Il existe trois types de transformations Windows Installer :

-   [Transformations incorporées](embedded-transforms.md)
-   [Transformations sécurisées](secured-transforms.md)
-   [Transformations non sécurisées](unsecured-transforms.md)

 

 



