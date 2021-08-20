---
description: l’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole OpenSearch et d’un fichier de descripteur de OpenSearch (. fichier osdx) (un connecteur de recherche).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6279b66be3b259058cc1b13bae6d9185e035211c65e87c21e070db638e74573
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118051838"
---
# <a name="opensearch"></a>OpenSearch

l’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole [OpenSearch](https://github.com/dewitt/opensearch) et d’un fichier de descripteur de OpenSearch (. fichier osdx) (un connecteur de recherche).

Cette rubrique contient les sections suivantes.

-   [Requirements](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Conditions requises



| Produit     | Version minimale du produit |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Kit de développement logiciel (SDK) Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [exemple de OpenSearch](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AdventureSearch** . 
2.  Entrez `msbuild AdventureSearch.sln`.

pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  ouvrez Windows Explorer et accédez au répertoire du projet **AdventureSearch** .
2.  Double-cliquez sur l’icône du fichier AdventureSearch. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio Solution ».

     

3.  Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2.  à l’invite de commandes, entrez `AdventureSearch.exe` ou dans Windows Explorer, double-cliquez sur l’icône de AdventureSearch.exe.
3.  à l’invite de commandes, entrez `GetOSDX.exe` ou dans Windows Explorer, double-cliquez sur l’icône de GetOSDX.exe.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[Vue d’ensemble du schéma de description du connecteur de recherche](search-sconn-desc-schema-entry.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Recherche fédérée dans Windows](-search-federated-search-overview.md)
</dt> <dt>

[Rechercher des exemples de code](-search-samples-ovw.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[Schéma de description de la bibliothèque](../shell/library-schema-entry.md)
</dt> </dl>

 

 
