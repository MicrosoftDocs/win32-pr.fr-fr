---
description: Le verrouillage d’une ressource signifie accorder l’accès de l’UC à son stockage.
ms.assetid: b17d8262-e514-4b9c-9237-653a4258a14e
title: Verrouillage des ressources (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70d66a7a420a33cb908d0974f9d942597019aded
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514721"
---
# <a name="locking-resources-direct3d-9"></a>Verrouillage des ressources (Direct3D 9)

Le verrouillage d’une ressource signifie accorder l’accès de l’UC à son stockage. Les options de verrouillage suivantes sont définies pour les ressources :

-   D3DLOCK \_ Ignorer
-   D3DLOCK en \_ lecture seule
-   D3DLOCK \_ NOOVERWRITE
-   D3DLOCK \_ NOSYSLOCK
-   D3DLOCK \_ aucune \_ \_ mise à jour incorrecte

Pour plus d’informations sur les indicateurs de verrouillage et sur la façon dont ils sont liés à des ressources spécifiques, consultez les pages de référence sur les méthodes de verrouillage des ressources individuelles. Les développeurs d’applications doivent noter que les \_ indicateurs D3DLOCK Discard, D3DLOCK \_ ReadOnly et D3DLOCK \_ NOOVERWRITE ne sont que des indicateurs. Le temps d’exécution ne vérifie pas si les applications suivent les fonctionnalités spécifiées par ces indicateurs. Une application qui spécifie D3DLOCK \_ ReadOnly, mais qui écrit dans la ressource doit attendre des résultats indéfinis. En général, l’utilisation des indicateurs de verrouillage, y compris les indicateurs d’utilisation de verrouillage, n’est pas garantie dans les versions ultérieures et peut entraîner une baisse significative des performances.

Une opération de verrouillage est suivie d’une opération de déverrouillage. Par exemple, après avoir verrouillé une texture, l’application abandonne par la suite un accès direct aux textures verrouillées en les déverrouillant. Outre l’octroi de l’accès au processeur, toute autre opération impliquant cette ressource est sérialisée pour la durée d’un verrou. Un seul verrou pour une ressource est autorisé, même pour les régions qui ne se chevauchent pas, et aucune opération d’accélérateur sur une surface ne peut être poursuivie pendant qu’une opération de verrouillage est en suspens sur cette surface.

Chaque interface de ressource a des méthodes pour verrouiller les mémoires tampons contenues. Chaque ressource de texture peut également verrouiller une sous-partie de cette ressource. les ressources 2D (surfaces) permettent le verrouillage des sous-rectangles, tandis que les ressources de volume permettent de verrouiller des sous-volumes ou des zones. Chaque méthode de verrouillage retourne une structure qui contient un pointeur vers le stockage qui stocke la ressource et des valeurs représentant les distances entre les lignes ou les plans de données, selon le type de ressource. Pour plus d’informations, consultez les listes de méthodes pour les interfaces de ressource. Le pointeur retourné pointe toujours vers l’octet supérieur gauche dans les sous-régions verrouillées.

Lorsque vous utilisez des mémoires tampons d’index et de vertex, vous pouvez effectuer plusieurs appels de verrouillage. Toutefois, vous devez vous assurer que le nombre d’appels de verrous correspond au nombre d’appels de déverrouillage.

Le DXTn stocke les pixels dans des blocs 4x4 encodés et peut uniquement être verrouillé sur des limites de 4 x 4.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> </dl>

 

 



