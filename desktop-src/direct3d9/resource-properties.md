---
description: Toutes les ressources partagent les propriétés suivantes.
ms.assetid: 6ef6ce68-44fa-4964-8b61-2a37382eda1c
title: Propriétés de ressource (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e7b53a23e489b5f53495c5d2626da1e2633c9cf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747165"
---
# <a name="resource-properties-direct3d-9"></a>Propriétés de ressource (Direct3D 9)

Toutes les ressources partagent les propriétés suivantes.

-   L’utilisation. La façon dont une ressource est utilisée, par exemple, comme une texture ou une cible de rendu.
-   Formater. Format des données, par exemple, le format de pixel d’une surface 2D.
-   Pool. Type de mémoire où la ressource est allouée.
-   Type. Type de ressource, par exemple, une mémoire tampon de vertex ou une cible de rendu.

Les utilisations de ressources sont appliquées. Une application qui utilisera une ressource dans une certaine opération doit spécifier cette opération au moment de la création de ressources. Pour obtenir la liste des constantes d’utilisation définies pour les ressources, consultez [**D3DUSAGE**](d3dusage.md).

Les \_ constantes D3DUSAGE RTPATCHES, D3DUSAGE \_ NPATCHES et D3DUSAGE \_ points indiquent au pilote que les données de ces mémoires tampons sont susceptibles d’être utilisées pour les correctifs de grille ou triangulaires, les N-patchs ou les points sprites, respectivement. Ces indicateurs sont fournis si le matériel ne peut pas exécuter ces opérations sans traitement de l’hôte. Par conséquent, le pilote souhaite allouer ces surfaces dans la mémoire système afin que le processeur puisse y accéder. Si le pilote peut effectuer ces opérations entièrement dans le matériel, il peut allouer ces surfaces dans la vidéo ou la mémoire AGP pour éviter une copie de l’hôte et améliorer les performances au moins double. Notez que les informations fournies par ces indicateurs ne sont pas absolument nécessaires. Un pilote peut détecter que ces opérations sont effectuées sur les données, et il déplace la mémoire tampon vers la mémoire système pour les trames suivantes.

Pour plus d’informations sur les indicateurs d’utilisation et sur la façon dont ils sont liés à des ressources spécifiques, consultez les pages de référence sur les méthodes de création de ressources individuelles.

Pour plus d’informations sur le format de surface des ressources, consultez le type énuméré [D3DFORMAT](d3dformat.md) .

La classe de mémoire qui contient les mémoires tampons d’une ressource est appelée un pool. Les valeurs de pool sont définies par le type énuméré [**D3DPOOL**](./d3dpool.md) . Un pool ne peut pas être mélangé pour différents objets contenus dans une ressource unique, c’est-à-dire des niveaux MIP dans un mipmap, et lorsqu’un pool est choisi pour une ressource, le pool ne peut pas être modifié.

Les types de ressources sont définis implicitement au moment de l’exécution lorsque l’application appelle une méthode de création de ressource telle que [**IDirect3DDevice9 :: CreateCubeTexture**](/windows/desktop/api). Les types de ressources sont définis par le type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) . Les applications peuvent interroger ces types au moment de l’exécution ; Toutefois, il est prévu que la plupart des scénarios ne nécessitent pas la vérification de type au moment de l’exécution.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources Direct3D](direct3d-resources.md)
</dt> </dl>

 

 
