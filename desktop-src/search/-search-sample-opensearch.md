---
description: L’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole OpenSearch et un fichier de descripteur OpenSearch (. fichier osdx) (un connecteur de recherche).
ms.assetid: 792884e4-826b-4474-82e1-1680d4d8b602
title: OpenSearch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8656efec434744d14714529d1e7b0d01a5349ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393459"
---
# <a name="opensearch"></a>OpenSearch

L’exemple de code OpenSearch montre comment créer un service de recherche fédéré à l’aide du protocole [OpenSearch](https://github.com/dewitt/opensearch) et un fichier de descripteur OpenSearch (. fichier osdx) (un connecteur de recherche).

Cette rubrique contient les sections suivantes.

-   [Configuration requise](#requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Exécution de l’exemple](#running-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise



| Produit     | Version minimale du produit |
|-------------|-------------------------|
| Windows     | Windows 7               |
| Kit de développement logiciel (SDK) Windows | 7.0                     |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible aux emplacements suivants.



| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub  | [OpenSearch, exemple](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/shellextensibility/OpenSearch)      |



 

 

> [!Note]  
> Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à partir de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet **AdventureSearch** . 
2.  Entrez `msbuild AdventureSearch.sln`.

Pour générer l’exemple à l’aide de Microsoft Visual Studio (par défaut) :

1.  Ouvrez l’Explorateur Windows et accédez au répertoire du projet **AdventureSearch** .
2.  Double-cliquez sur l’icône du fichier AdventureSearch. sln pour ouvrir le projet dans Visual Studio.
    > [!Note]  
    > L’extension de nom de fichier. sln n’est pas affichée sous paramètres de dossier par défaut. Dans ce cas, il peut être identifié par son icône unique ou par sa description de type, « Microsoft Visual Studio solution ».

     

3.  Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1.  Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.
2.  À l’invite de commandes, entrez `AdventureSearch.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de AdventureSearch.exe.
3.  À l’invite de commandes, entrez `GetOSDX.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de GetOSDX.exe.

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

 

 
