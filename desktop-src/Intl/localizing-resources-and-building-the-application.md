---
description: Cette rubrique explique comment créer une application MUI standard.
ms.assetid: 386e9601-ce21-4ef0-b225-0c4249d1942d
title: Localisation des ressources et génération de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74262499b20836ee4860f1c0fc1a1bf80e19d58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524929"
---
# <a name="localizing-resources-and-building-the-application"></a>Localisation des ressources et génération de l’application

Cette rubrique explique comment créer une application MUI standard. Il est supposé que vous utilisez Microsoft Visual Studio pour le codage et Microsoft Visual Studio ou la ligne de commande Visual Studio pour la génération. Vous êtes supposé utiliser un fichier solution. sln pour votre application et prendre en charge un fichier Resource. h pour refléter le fichier de ressources de la langue de base.

> [!Note]  
> Si vous utilisez la ligne de commande Visual Studio pour la génération, vous allez utiliser la commande **VCBUILD** pour générer le fichier solution.

 

Les fichiers d’application sont générés séparément pour chaque langue. Chaque Build crée des fichiers. exe. exe et des fichiers. exe. mui de langue identique neutres. En outre, plusieurs autres fichiers sont copiés dans les dossiers de version appropriés.

La génération de l’application dépend du type de ressources et du type de localisation que vous utilisez. Pour la localisation pré-build, vous disposez d’une copie du fichier de langue de base localisée pour chaque langue prise en charge. Pour la localisation après génération, vous pouvez copier le fichier. mui résultant de la génération du module exécutable et du module de ressources, et fournir les copies aux localiseurs.

> [!Note]  
> La procédure suivante suppose des ressources Win32 PE avec un projet Visual Studio généré pour chaque langage. Les ressources linguistiques de base sont fournies dans un fichier. RC et chargées à l’aide d’un module DLL. Vous pouvez répéter la procédure en fonction des besoins pour générer toutes les langues prises en charge.

 

**Pour générer l’application**

1.  Configurez un projet Visual Studio pour la langue de base.
2.  Si vous souhaitez utiliser un fichier de configuration de ressources avec les outils de ressources, définissez-en un comme décrit dans [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).
3.  Définissez les paramètres requis par l’utilitaire du compilateur RC dans les pages de propriétés du projet sous **Propriétés de configuration → ressources → ligne de commande → Options supplémentaires**.
4.  Exécutez le compilateur RC. L’utilitaire compile et fractionne les ressources non localisables et localisables en deux fichiers objets différents, à l’aide des données de configuration de ressource. Dans cette étape, les ressources indépendantes du langage sont liées à un fichier LN. Pour plus d’informations, consultez la description de l’utilitaire dans les [utilitaires de ressource](resource-utilities.md).
5.  Pour lier les ressources spécifiques à une langue dans un fichier. mui spécifique à une langue, définissez un événement après génération pour le projet dans les pages de propriétés sous **Propriétés de configuration → événements de build → événement après génération → ligne de commande**.
6.  Définissez un événement après génération pour appliquer la valeur de somme de contrôle du fichier LN au fichier. mui pour la langue. Vous pouvez utiliser l’utilitaire MUIRCT pour cette étape. Pour plus d’informations, consultez la description de l’utilitaire dans les [utilitaires de ressource](resource-utilities.md).
7.  Utilisez la ligne de commande de l’événement après génération pour ajouter des commandes permettant de copier les fichiers dans la structure de dossiers de la version appropriée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de l’interface utilisateur multilingue](using-multilingual-user-interface.md)
</dt> <dt>

[Préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md)
</dt> <dt>

[Utilitaires de ressource](resource-utilities.md)
</dt> </dl>

 

 



