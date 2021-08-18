---
description: Exemple de filtres de source Push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemple de filtres de source Push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e72a9be7e5fa81d4fe2dc006c6d12e42f4f94d91561823b7f26a8400bbddda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747789"
---
# <a name="push-source-filters-sample"></a>Exemple de filtres de source Push

## <a name="description"></a>Description

Cet exemple se compose d’un ensemble de trois filtres sources qui fournissent les données sources suivantes sous la forme d’un flux vidéo :

-   CPushSourceBitmap : bitmap unique (chargée à partir du répertoire actif)
-   CPushSourceBitmapSet : ensemble de bitmaps (chargé à partir du répertoire actif)
-   CPushSourceDesktop : copie de l’image de bureau actuelle (GDI uniquement)

## <a name="usage"></a>Usage

Pour utiliser un filtre, chargez-le dans GraphEdit et affichez sa broche de sortie. Cela permet de connecter un convertisseur vidéo (et éventuellement un filtre de convertisseur d’espace colorimétrique) et d’afficher la sortie. Si vous souhaitez afficher la sortie dans un fichier AVI, chargez le fichier AVI MUX, chargez un filtre de writer de fichier, fournissez un nom de sortie au writer de fichier et affichez la broche de sortie du filtre PushSource. Vous pouvez également charger et connecter des compresseurs vidéo, des effets vidéo, etc.

> [!Note]  
> Le filtre de capture du Bureau ne prend pas en charge les superpositions matérielles. il ne capture donc pas la vidéo rendue sur une surface de recouvrement ou des curseurs affichés via la superposition matérielle. Il utilise GDI pour convertir l’image de bureau actuelle en une image bitmap, qui est transmise à la broche de sortie en tant qu’exemple de média.

 

## <a name="downloading-the-sample"></a>Téléchargement de l’exemple

pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ \\ \\ \\ PushSource filtres de DirectShow \\ .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Extraits](directshow-samples.md)
</dt> </dl>

 

 



