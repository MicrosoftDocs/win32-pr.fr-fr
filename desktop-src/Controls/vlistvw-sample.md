---
title: Exemple VListVW
ms.assetid: 5e1d13a6-ae11-4729-b0fc-0a1620cf0738
description: 'En savoir plus sur : exemple VListVW'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefcd39c44e79ab4eec23f7becf202d1a3cd3566f6be9496e9fd61b577c87f4a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957558"
---
# <a name="vlistvw-sample"></a>Exemple VListVW

Cette rubrique décrit l’exemple de code VListVW. Il contient les sections suivantes :

-   [Description](#description)
-   [Configuration minimale requise](#minimum-requirements)
-   [Téléchargement de l’exemple](#downloading-the-sample)
-   [Génération de l'exemple](#building-the-sample)
-   [Rubriques connexes](#related-topics)

## <a name="description"></a>Description

L’exemple VListVW montre comment implémenter un contrôle List-View virtuel simple dans une application. Un contrôle List-View virtuel est un contrôle List-View standard avec le style **LVS \_ OWNERDATA** . Cet exemple crée un contrôle List-View qui « virtuellement » contient 100 000 éléments. Les éléments ne sont jamais ajoutés. Au lieu de cela, le contrôle de liste virtuelle est « dit » le nombre d’éléments qu’il contient avec le message [**\_ SETITEMCOUNT LVM**](lvm-setitemcount.md) . Lorsqu’un élément doit être dessiné, le contrôle List-View interroge la fenêtre parente pour obtenir des informations sur l’affichage avec la notification [LVN \_ GETDISPINFO](lvn-getdispinfo.md) .

## <a name="minimum-requirements"></a>Configuration minimale requise



| Produit          | Version                               |
|------------------|---------------------------------------|
| DLL              | comctl32.dll version 4,70             |
| Système d'exploitation | Windows 95, Microsoft Windows NT 3,51 |



 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

l’exemple VListVW est disponible sur github dans le [référentiel d’exemples classiques Windows](https://github.com/microsoft/Windows-classic-samples). Vous trouverez des exemples d’éléments de contrôle List View [ici](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/controls/common/vlistvw)

 

## <a name="building-the-sample"></a>Génération de l'exemple

Pour générer l’exemple à l’aide de l’invite de commandes :

1.  Ouvrez la fenêtre d’invite de commandes et accédez au répertoire du projet.
2.  Entrez `msbuild [project file]`.

Pour générer l’exemple à l’aide de Visual Studio :

1.  ouvrez Windows Explorer et accédez au répertoire du projet.
2.  Double-cliquez sur l’icône du fichier. vcproj pour ouvrir le projet dans Visual Studio.
3.  Dans le menu **générer** , sélectionnez **générer la solution** pour générer la solution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos des contrôles List-View](list-view-controls-overview.md)
</dt> </dl>

 

 




