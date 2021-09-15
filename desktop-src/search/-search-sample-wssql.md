---
description: l’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via langage SQL (SQL).
ms.assetid: 28663608-66b3-4404-9426-5a4b5f52a408
title: WSSQL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ac8f76b995d21a562f843344d1722cecec433af
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313193"
---
# <a name="wssql"></a>WSSQL

l’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via langage SQL (SQL).

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
| GitHub        | [Exemple WSSQL](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/WSSQL)           |

> [!NOTE]  
> pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. ouvrez Windows Explorer et accédez au répertoire du projet **WSSQL** .
2. Double-cliquez sur l’icône du fichier WSSQL. sln pour ouvrir le projet dans Visual Studio.
    > [!NOTE]  
    > le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version ultérieure. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **Générer**, sélectionnez **Générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de Windows Explorer.
2. à l’invite de commandes, entrez `WSSQL.exe` ou dans Windows Explorer, double-cliquez sur l’icône de WSSQL.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="conceptual"></a>Conceptuel

[utilisation de la syntaxe de SQL de recherche Windows](-search-sql-windowssearch-entry.md)

[Informations générales sur le langage de requête](-search-sql-generalqueryinfo.md)

[Vue d’ensemble de la programmation OLE DB](/cpp/data/oledb/ole-db-programming-overview)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
