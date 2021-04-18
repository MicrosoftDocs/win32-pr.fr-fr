---
description: Votre application globalisée doit définir un grand nombre d’éléments d’interface utilisateur, tels que des menus, des boîtes de dialogue, des chaînes d’aide et d’autres éléments, représentés sous forme de ressources localisées.
ms.assetid: 4d8b769d-0830-4e4e-b284-ce0b21dfe5d4
title: Gestion des ressources MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aeed59c4b835e2c93e5f4cfc9988509349d8b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519569"
---
# <a name="mui-resource-management"></a>Gestion des ressources MUI

Votre application globalisée doit définir un grand nombre d’éléments d’interface utilisateur, tels que des menus, des boîtes de dialogue, des chaînes d’aide et d’autres éléments, représentés sous forme de ressources localisées. La langue de l’interface utilisateur devient l’un des paramètres de l’application. Cette section décrit la technologie de ressources MUI, que nous vous recommandons d’utiliser pour la création de vos ressources d’application.

## <a name="features-of-the-mui-resource-technology"></a>Fonctionnalités de la technologie de ressources MUI

La technologie de ressources MUI, exposée dans Windows Vista et versions ultérieures, présente les caractéristiques suivantes :

-   Les fichiers de ressources spécifiques à une langue sont stockés séparément du fichier binaire de code d’application, de sorte qu’une modification du code n’affecte pas les ressources.
-   Les ressources de plusieurs langues peuvent être déployées dans une installation unique ou séparément pour chaque langue.
-   Une ressource est chargée et affichée en fonction de la langue de l’application telle qu’elle est définie par l’utilisateur.

Cette technologie associe les ressources définies dans les fichiers spécifiques à une langue à une version particulière d’un fichier indépendant de la langue (LN). Le fichier LN est un fichier PE Win32 qui représente le code d’application binaire et les ressources indépendantes du langage. L’Association de fichiers utilise une somme de contrôle reflétée dans les données de configuration de ressource contenues dans tous les fichiers associés. Le chargeur de ressources utilise la somme de contrôle pour vérifier que les fichiers contiennent la même version des ressources requises. Il valide également la langue dans le fichier spécifique à la langue avec son nom de dossier. Le chargeur ne charge pas de fichier de ressources si l’Association appropriée n’est pas établie.

Plus précisément, la somme de contrôle principale est calculée à partir des numéros de version majeure et mineure d’un fichier et du nom de fichier (sensible à la casse), qui sont obtenus à partir de la ressource de version. Cette somme de contrôle ne doit pas changer entre les versions RTM et Service Pack du même composant. En outre, une somme de contrôle de service est utilisée pour déterminer la version appropriée du fichier de ressources spécifique à la langue à charger. Cette somme de contrôle est calculée en fonction des ressources localisables dans le fichier.

MUI fournit deux utilitaires de ressource que vous pouvez utiliser pour préparer les fichiers de ressources de votre application. Un utilitaire spécifique à MUI, appelé MUIRCT, vous permet de générer un fichier LN et les fichiers de ressources spécifiques à une langue associés. Sur Windows Vista et versions ultérieures, le compilateur Windows RC a également été modifié pour créer ces fichiers en fonction de la technologie de ressources MUI. Pour plus d’informations sur la syntaxe et les détails de ces outils, consultez [utilitaires de ressource](resource-utilities.md).

## <a name="ln-file"></a>Fichier LN

Le fichier LN pour une application MUI contient du code exécutable et des ressources indépendantes du langage qui sont partagées et installées par toutes les versions linguistiques de l’application.

## <a name="language-specific-resource-file"></a>Fichier de ressources Language-Specific

Un fichier de ressources spécifique à un langage contient normalement des chaînes d’interface utilisateur et d’autres éléments qui nécessitent une localisation pour une langue particulière. Votre application MUI utilise un fichier de ressources spécifique à une langue par langue prise en charge. Le fichier LN de l’application est le même pour chaque fichier de ressources spécifique à une langue.

En cas de création à l’aide de la technologie de ressources MUI, les fichiers spécifiques à une langue ont une extension « . mui » et sont gérés comme suit :

-   Les fichiers spécifiques à une langue associés à un fichier LN donné partagent tous le même nom de fichier, qui est formé en ajoutant l’extension « . mui » au nom de fichier complet (avec l’extension) du fichier LN correspondant. Par exemple, un fichier LN nommé « Myfile.dll » contient des fichiers spécifiques à la langue nommés « Myfile.dll. mui ».
-   Les fichiers spécifiques à une langue résident dans des sous-dossiers du dossier contenant le fichier LN. Chaque nom de dossier reflète la langue.

## <a name="resource-configuration-data"></a>Données de configuration des ressources

Pour associer un fichier LN à ses fichiers spécifiques à une langue, la technologie de ressources MUI utilise les données de configuration de ressource, y compris la somme de contrôle. La procédure de génération de ressources place ces informations dans une section de configuration RC de chaque LN et fichier spécifique à la langue. Une forme lisible par l’utilisateur de ces informations est disponible via l’utilitaire MUIRCT. Pour plus d’informations, consultez [utilitaires de ressource](resource-utilities.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’interface utilisateur multilingue](about-multilingual-user-interface.md)
</dt> <dt>

[Utilitaires de ressource](resource-utilities.md)
</dt> </dl>

 

 



