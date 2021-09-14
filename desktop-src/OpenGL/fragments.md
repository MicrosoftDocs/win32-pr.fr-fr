---
title: Fragments
description: Fragments
ms.assetid: bc400251-32c4-4477-ba0c-a0046fe85327
keywords:
- OpenGL, fragments
- Pipeline de traitement OpenGL, fragments
- fragments OpenGL
- framebuffers, fragments modifiant les pixels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e2b4c2dc36e24c4fd9baa82b28fa4d336f69b5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011509"
---
# <a name="fragments"></a>Fragments

Un fragment produit par rastérisation modifie le pixel correspondant dans le trame uniquement s’il réussit les tests suivants :

-   [Test de propriété des pixels](pixel-ownership-test.md)
-   [Test de ciseaux](scissor-test.md)
-   [Test alpha](alpha-test.md)
-   [Test de stencil](stencil-test.md)
-   [Test de la mémoire tampon de profondeur](depth-buffer-test.md)

En cas de réussite, les données du fragment peuvent remplacer les valeurs trame existantes, ou vous pouvez les combiner avec des données existantes dans le trame, en fonction de l’état de certains modes. Vous pouvez combiner le fragment avec les données de trame de la façon suivante :

-   [Fusion](blending.md)
-   [Tramage](dithering.md)
-   [Opérations logiques](logical-operations.md)

 

 




