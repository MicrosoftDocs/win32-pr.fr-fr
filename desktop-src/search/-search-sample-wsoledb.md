---
description: l’exemple de code WSOleDB montre Active Template Library (ATL) OLE DB l’accès aux applications de recherche Windows et illustre deux méthodes supplémentaires pour récupérer les résultats de Windows recherche.
ms.assetid: c81bf3af-e023-4384-8c89-0fa9c8f08773
title: WSOleDB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6cecfc308fdfa9af796e64ab8bc6273f9c4d94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313194"
---
# <a name="wsoledb"></a>WSOleDB

l’exemple de code WSOleDB montre Active Template Library (ATL) OLE DB l’accès aux applications de recherche Windows et illustre deux méthodes supplémentaires pour récupérer les résultats de Windows recherche.

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

| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Exemple WSOleDB](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSOleDB)         |

> [!NOTE]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. ouvrez Windows Explorer et accédez au répertoire du projet **WSOleDB** .
2. Double-cliquez sur l’icône du fichier WSOleDB. sln pour ouvrir le projet dans Visual Studio.
  
    > [!NOTE]  
    > le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version ultérieure. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2. à l’invite de commandes, entrez `WSOleDB.exe` ou dans Windows Explorer, double-cliquez sur l’icône de WSOleDB.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Référence

[**ISearchCatalogManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager)

[**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)

[**ISearchManager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager)

[**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)

### <a name="conceptual"></a>Conceptuel

[Vue d’ensemble de la programmation OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
