---
description: Les contrôles gamma vous permettent de modifier la façon dont le système affiche le contenu de la surface, sans affecter le contenu de la surface elle-même.
ms.assetid: 74f106be-8f47-4875-9908-32ff35912968
title: Contrôles gamma (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6484bcf7e8fa5e07a3bf4bb718cd361330560f8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516820"
---
# <a name="gamma-controls-direct3d-9"></a>Contrôles gamma (Direct3D 9)

Les contrôles gamma vous permettent de modifier la façon dont le système affiche le contenu de la surface, sans affecter le contenu de la surface elle-même. Considérez ces contrôles comme des filtres très simples que Direct3D applique aux données lorsqu’il quitte une surface et avant qu’il ne soit rendu à l’écran.

Les contrôles gamma sont une propriété d’une chaîne de permutation. Les contrôles gamma permettent de modifier dynamiquement la manière dont les niveaux rouge, vert et bleu d’une surface correspondent aux niveaux réels affichés par le système. En définissant des niveaux gamma, vous pouvez faire en sorte que l’écran de l’utilisateur clignote en rouge lorsque le caractère de l’utilisateur est capturé, en vert lorsque le caractère récupère un nouvel élément, et ainsi de suite, sans copier les nouvelles images dans la mémoire tampon de trame pour obtenir l’effet. Vous pouvez également ajuster les niveaux de couleurs pour appliquer un décalage de couleur aux images de la mémoire tampon d’arrière-plan.

Il y a toujours au moins une chaîne de permutation (la chaîne de permutation implicite) pour chaque appareil, car Direct3D 9 a une chaîne de permutation en tant que propriété de l’appareil. Étant donné que la rampe gamma est une propriété de la chaîne de permutation, la rampe gamma peut être appliquée lorsque la chaîne de permutation est fenêtre. La rampe gamma prend effet immédiatement. Aucune opération de synchronisation verticale n’est en attente.

Les méthodes [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) et [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) vous permettent de manipuler des niveaux de rampe qui affectent les composants de couleur rouge, vert et bleu des pixels de la surface avant qu’ils ne soient envoyés au convertisseur numérique-analogique (DAC) pour l’affichage.

## <a name="gamma-ramp-levels"></a>Niveaux de rampe gamma

Dans Direct3D, le terme rampe gamma décrit un ensemble de valeurs qui mappent le niveau d’un composant de couleur particulier-rouge, vert, bleu-pour tous les pixels de la mémoire tampon de trame aux nouveaux niveaux reçus par la DAC pour l’affichage. Le remappage est effectué par le biais de trois tables de recherche, une pour chaque composant de couleur.

Voici comment cela fonctionne : Direct3D prend un pixel de la mémoire tampon de trame et évalue ses composants de couleur rouge, vert et bleu individuels. Chaque composant est représenté par une valeur comprise entre 0 et 65535. Direct3D prend la valeur d’origine et l’utilise pour indexer un tableau de 256 éléments (rampe), où chaque élément contient une valeur qui remplace la valeur d’origine. Direct3D effectue ce processus de recherche et de remplacement pour chaque composant de couleur de chaque pixel de la mémoire tampon de trame, modifiant ainsi les couleurs finales de tous les pixels de l’écran.

Il est pratique de visualiser les valeurs de rampe en les subgraphies, comme illustré dans les deux graphiques suivants. Le graphique de gauche montre une rampe qui ne modifie pas du tout les couleurs. Le graphique de droite montre une rampe qui impose un écart négatif au composant de couleur auquel elle est appliquée.

![graphiques des valeurs de rampe gamma](images/gammalv.png)

Les éléments de tableau du graphique sur la gauche contiennent des valeurs identiques à leur index-0 dans l’élément à l’index 0, et 65535 à l’index 255. Ce type de rampe est la valeur par défaut, car elle ne modifie pas les valeurs d’entrée avant qu’elles ne soient affichées. Le graphe droit fournit plus de variantes ; son rampe contient des valeurs comprises entre 0 dans le premier élément et 32768 dans le dernier élément, avec des valeurs comprises entre elles. L’effet est que le composant de couleur qui utilise cette rampe apparaît en sourdine sur l’écran. Vous n’êtes pas limité à l’utilisation de graphiques linéaires ; Si votre application peut assigner un mappage arbitraire si nécessaire. Vous pouvez même définir les entrées sur des zéros pour supprimer complètement un composant de couleur de l’affichage.

## <a name="setting-and-retrieving-gamma-ramp-levels"></a>Définition et récupération des niveaux de rampe gamma

Les niveaux de rampe gamma sont des tables de recherche effectives que Direct3D utilise pour mapper les composants de couleur de la mémoire tampon de frame aux nouveaux niveaux qui seront affichés. Vous pouvez définir et récupérer des niveaux de rampe pour la surface principale en appelant les méthodes [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) et [**GetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getgammaramp) . **SetGammaRamp** accepte deux paramètres et **GetGammaRamp** accepte un paramètre. Pour **SetGammaRamp**, le premier paramètre est D3DSGR \_ CALIBRATE ou D3DSGR \_ no \_ étalonnage. Le deuxième paramètre, pRamp, est un pointeur vers une structure [**D3DGAMMARAMP**](d3dgammaramp.md) . La structure **D3DGAMMARAMP** contient des tableaux de mots de 3 256 éléments, un tableau contenant chacun les rampes gamma rouge, vert et bleu. **GetGammaRamp** possède un paramètre qui prend un pointeur vers un type **D3DGAMMARAMP** qui sera rempli avec la rampe gamma actuelle.

Vous pouvez inclure la \_ valeur D3DSGR CALIBRATE pour le premier paramètre de [**SetGammaRamp**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setgammaramp) pour appeler le étalonnage lors de la définition de nouveaux niveaux gamma. L’étalonnage des rampes gamma entraîne une surcharge de traitement et ne doit pas être utilisé fréquemment. La définition d’une rampe gamma étalonnée fournit une valeur gamma cohérente et absolue pour l’utilisateur, indépendamment de la carte graphique et du moniteur.

Tous les systèmes ne prennent pas en charge l’étalonnage gamma. Pour déterminer si l’étalonnage gamma est pris en charge, appelez [**GetDeviceCaps**](/windows/desktop/api), puis examinez le membre Caps2 de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associée après le retour de la méthode. Si l' \_ indicateur de capacité D3DCAPS2 CANCALIBRATEGAMMA est présent, l’étalonnage gamma est pris en charge.

Lorsque vous définissez de nouveaux niveaux de rampe, gardez à l’esprit que les niveaux que vous définissez dans les tableaux sont utilisés uniquement quand votre application est en mode plein écran, en mode exclusif. Chaque fois que votre application passe en mode normal, les niveaux de rampe sont mis de côté et prennent effet à nouveau lorsque l’application rétablit le mode plein écran.

Si l’appareil ne prend pas en charge les rampes gamma dans le mode de présentation actuel de la chaîne de permutation (plein écran ou avec fenêtre), aucune valeur d’erreur n’est retournée. Les applications peuvent vérifier les \_ bits de capacité D3DCAPS2 FULLSCREENGAMMA et D3DCAPS2 \_ CANCALIBRATEGAMMA dans le membre Caps2 du type D3DCAPS9 pour déterminer les fonctionnalités de l’appareil et si un étalonnage est installé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Surfaces Direct3D](direct3d-surfaces.md)
</dt> </dl>

 

 
