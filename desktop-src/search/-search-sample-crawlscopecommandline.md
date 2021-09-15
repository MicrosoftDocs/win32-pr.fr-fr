---
description: L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM).
ms.assetid: 8c82fe18-8676-43d2-a3da-027a733ee0a4
title: CrawlScopeCommandLine
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb770c44f82af320e2b39fe679b632cf03825e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127523397"
---
# <a name="crawlscopecommandline"></a>CrawlScopeCommandLine

L’exemple de code CrawlScopeCommandLine montre comment définir des options de ligne de commande pour les opérations d’indexation du gestionnaire de portée d’analyse (CSM).

Cette rubrique contient les sections suivantes.

- [Configuration requise](#requirements)
- [Téléchargement de l’exemple](#downloading-the-sample)
- [Génération de l'exemple](#building-the-sample)
- [Exécution de l’exemple](#running-the-sample)
- [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Spécifications

| Produit     | Version du produit          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 ou 10    |
| Kit de développement logiciel (SDK) Windows | 7,0 ou version ultérieure           |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible à l’emplacement suivant.

| Emplacement | Chemin d’accès ou URL                                                                |
|----------|----------------------------------------------------------------------------|
| GitHub   |    [Exemple CrawlScopeCommandLine](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/CrawlScopeCommandLine)|

> [!NOTE]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. ouvrez Windows Explorer et accédez au répertoire du projet **CrawlScopeCommandLine** .
2. Double-cliquez sur l’icône du fichier csmcmd. sln pour ouvrir le projet dans Visual Studio.
  
    > [!NOTE]  
    > le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version ultérieure. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2. à l’invite de commandes, entrez `csmcmd.exe` ou dans Windows Explorer, double-cliquez sur l’icône de csmcmd.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Informations de référence

[**IEnumSearchRoots**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchroots)

[**IEnumSearchScopeRules**](/windows/desktop/api/Searchapi/nn-searchapi-ienumsearchscoperules)

[**ISearchCrawlScopeManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager)

[**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2)

[**ISearchRoot**](/windows/desktop/api/Searchapi/nn-searchapi-isearchroot)

[**ISearchScopeRule**](/windows/desktop/api/Searchapi/nn-searchapi-isearchscoperule)

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
