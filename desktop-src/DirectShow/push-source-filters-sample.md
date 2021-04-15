---
description: Exemple de filtres de source Push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemple de filtres de source Push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521332"
---
# <a name="push-source-filters-sample"></a>Exemple de filtres de source Push

## <a name="description"></a>Description

Cet exemple se compose d’un ensemble de trois filtres sources qui fournissent les données sources suivantes sous la forme d’un flux vidéo :

-   CPushSourceBitmap : bitmap unique (chargée à partir du répertoire actif)
-   CPushSourceBitmapSet : ensemble de bitmaps (chargé à partir du répertoire actif)
-   CPushSourceDesktop : copie de l’image de bureau actuelle (GDI uniquement)

## <a name="usage"></a>Utilisation

Pour utiliser un filtre, chargez-le dans GraphEdit et affichez sa broche de sortie. Cela permet de connecter un convertisseur vidéo (et éventuellement un filtre de convertisseur d’espace colorimétrique) et d’afficher la sortie. Si vous souhaitez afficher la sortie dans un fichier AVI, chargez le fichier AVI MUX, chargez un filtre de writer de fichier, fournissez un nom de sortie au writer de fichier et affichez la broche de sortie du filtre PushSource. Vous pouvez également charger et connecter des compresseurs vidéo, des effets vidéo, etc.

> [!Note]  
> Le filtre de capture du Bureau ne prend pas en charge les superpositions matérielles. il ne capture donc pas la vidéo rendue sur une surface de recouvrement ou des curseurs affichés via la superposition matérielle. Il utilise GDI pour convertir l’image de bureau actuelle en une image bitmap, qui est transmise à la broche de sortie en tant qu’exemple de média.

 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ fichiers de \\ \\ \\ filtres DirectShow \\ PushSource.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples DirectShow](directshow-samples.md)
</dt> </dl>

 

 



