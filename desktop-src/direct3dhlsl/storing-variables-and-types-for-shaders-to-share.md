---
title: Stockage des variables et des types pour les nuanceurs à partager
description: L’objet de liaison de classe est un espace de noms pour les variables et les types que plusieurs nuanceurs peuvent partager.
ms.assetid: 8b61677b-a466-4646-b0b2-19097669f8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f9423154cd42de28b2d447776fe21a7b8e57620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104971783"
---
# <a name="storing-variables-and-types-for-shaders-to-share"></a>Stockage des variables et des types pour les nuanceurs à partager

L’objet de liaison de classe est un espace de noms pour les variables et les types que plusieurs nuanceurs peuvent partager. Quand vous transmettez un objet de liaison de classe dans un appel pour créer un nuanceur, le runtime recueille une liste de variables et de types qui peuvent implémenter chaque interface dans le nuanceur et stocke les noms de ces variables et types dans l’objet de liaison de classe.

Par conséquent, lorsque vous appelez la méthode [**ID3D11ClassLinkage :: GetClassInstance**](/windows/desktop/api/d3d11/nf-d3d11-id3d11classlinkage-getclassinstance) pour générer des instances de classe à partir de l’objet de liaison de classe, le runtime peut récupérer la variable ou le type qui correspond au nom fourni dans chaque nuanceur (si ce nom est valide pour un nuanceur donné) et qui est créé avec l’objet de liaison de classe donné.

Par exemple, supposons que vous avez une classe **Light** qui implémente une interface de **couleur** , et que vous utilisez cette classe dans votre nuanceur de sommets et votre nuanceur de pixels. Quand vous créez un nuanceur (par exemple, en appelant [**ID3D11Device :: CreatePixelShader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createpixelshader)), le runtime détermine que le type de classe **Light** est disponible dans les nuanceurs vertex et pixel et ajoute le type de classe **Light** à l’objet de liaison de classe. Vous pouvez ensuite créer une instance de **lumière** à l’emplacement de votre choix, lier les ressources pour les deux nuanceurs et passer cette instance dans le tableau d’instances de classe lorsque vous définissez le nuanceur sur l’appareil (par exemple, en appelant [**ID3D11DeviceContext ::P ssetshader**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshader)). Le runtime exécute ensuite la séquence suivante :

1.  Vérifie que l’instance a été créée avec le même objet de liaison de classe.
2.  Vérifie que le type de classe **Light** est disponible dans les nuanceurs de sommets et de pixels.
3.  Sélectionne les tables de fonctions appropriées, qui peuvent être différentes pour les nuanceurs vertex et pixel.
4.  Envoie les offsets fournis par l’instance.

L’objet de liaison de classe est finalement un référentiel de noms de type et de variable. Le nombre maximal de noms disponibles pour chaque élément (type et variable) est de 64 Ko. Plus les noms de type et de variable sont longs, plus l’exigence de stockage est importante pour les métadonnées d’interface stockées par nuanceur. Cela est dû au fait que le runtime doit stocker un mappage pour ces noms pour chaque nuanceur.

## <a name="related-topics"></a>Rubriques connexes

[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)


## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liaison dynamique](overviews-direct3d-11-hlsl-dynamic-linking.md)
</dt> </dl>

 

 