---
description: 'L’exemple de code ReindexMatchingUrls montre comment fournir trois manières de spécifier les fichiers à réindexer : les URL qui correspondent à un type de fichier, un type MIME ou une clause WHERE spécifiée.'
ms.assetid: f7b3a8a6-b464-46d4-a99c-fc56eea9b1ec
title: ReindexMatchingUrls
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a7bb6ae3148f6969fc5349e1ebdf666a527282
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313213"
---
# <a name="reindexmatchingurls"></a>ReindexMatchingUrls

L’exemple de code ReindexMatchingUrls montre comment fournir trois manières de spécifier les fichiers à réindexer : les URL qui correspondent à un type de fichier, un type MIME ou une clause WHERE spécifiée.

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

| Emplacement      | URL du chemin                                                                      |
|---------------|-------------------------------------------------------------------------------|
| GitHub  | [Exemple ReindexMatchingUrls](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/ReindexMatchingUrls) |

> [!NOTE]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. ouvrez Windows Explorer et accédez au répertoire du projet **ReindexMatchingUrls** . Par exemple, le chemin d’installation complet par défaut est `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\WindowsSearch\ReindexMatchingUrls` .
2. Double-cliquez sur l’icône du fichier REINDEX. sln pour ouvrir le projet dans Visual Studio.
  
    > [!NOTE]  
    > le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version ultérieure. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2. à l’invite de commandes, entrez `Reindex.exe` ou dans Windows Explorer, double-cliquez sur l’icône de Reindex.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Référence

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**ISearchPersistentItemsChangedSink**](/windows/desktop/api/Searchapi/nn-searchapi-isearchpersistentitemschangedsink)

[**ISearchViewChangedSink**](/windows/desktop/api/searchapi/nn-searchapi-isearchviewchangedsink)

[**définir la priorité des \_ indicateurs**](/windows/win32/api/searchapi/ne-searchapi-tagprioritize_flags)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
