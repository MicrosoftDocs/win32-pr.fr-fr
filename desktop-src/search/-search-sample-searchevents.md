---
description: L’exemple de code SearchEvents montre comment hiérarchiser les événements d’indexation.
ms.assetid: a352c3e2-5860-4b9c-a3c7-a806f69b4f7d
title: SearchEvents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21472d113694a41a3c7855c0fdaf8f2fa2b3b2e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512941"
---
# <a name="searchevents"></a>SearchEvents

L’exemple de code SearchEvents montre comment hiérarchiser les événements d’indexation.

Cette rubrique contient les sections suivantes.

- [Configuration requise](#requirements)
- [Téléchargement de l’exemple](#downloading-the-sample)
- [Génération de l'exemple](#building-the-sample)
- [Exécution de l’exemple](#running-the-sample)
- [Rubriques connexes](#related-topics)

## <a name="requirements"></a>Configuration requise

| Produit     | Version du produit          |
|-------------|--------------------------|
| Windows     | Windows 7, 8.1 ou 10    |
| Kit de développement logiciel (SDK) Windows | 7,0 ou version ultérieure           |

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Cet exemple est disponible à l’emplacement suivant.

| Emplacement      | URL du chemin                                                                  |
|---------------|---------------------------------------------------------------------------|
| GitHub        | [Exemple SearchEvents](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/SearchEvents)    |

> [!NOTE]  
> Pour toutes les versions de Windows, y compris Windows 7, nous vous recommandons de télécharger les exemples directement à partir de GitHub pour obtenir la version la plus récente.

## <a name="building-the-sample"></a>Génération de l'exemple

1. Ouvrez l’Explorateur Windows et accédez au répertoire du projet **SearchEvents** .
2. Double-cliquez sur l’icône du fichier Eventing. sln pour ouvrir le projet dans Visual Studio.
  
    > [!NOTE]  
    > Le fichier sln a été créé sous une version antérieure de Visual Studio. par conséquent, la mise à niveau est requise si vous exécutez Visual Studio 2012 ou une version plus récente. Cela n’aura pas d’impact sur le comportement de l’exemple.

3. Dans le menu **générer** , sélectionnez **générer la solution**.

## <a name="running-the-sample"></a>Exécution de l'exemple

1. Accédez au répertoire qui contient le nouveau fichier exécutable à l’aide de la fenêtre d’invite de commandes ou de l’Explorateur Windows.
2. À l’invite de commandes, entrez `Eventing.exe` , ou à partir de l’Explorateur Windows, double-cliquez sur l’icône de Eventing.exe.

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Informations de référence

[**IRowsetEvents**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetevents)

[**IRowsetPrioritization**](/windows/desktop/api/Searchapi/nn-searchapi-irowsetprioritization)

[**niveau de priorité \_**](/windows/win32/api/searchapi/ne-searchapi-priority_level)

[**ROWSETEVENT \_ ITEMSTATE**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_itemstate)

[**\_type ROWSETEVENT**](/windows/win32/api/searchapi/ne-searchapi-rowsetevent_type)

### <a name="other-samples"></a>Autres exemples

[Rechercher des exemples de code](-search-samples-ovw.md)
