---
title: Comment indexer plusieurs Flux de sortie
description: Dans le nuancier Model 5, un nuanceur Geometry peut prendre en charge jusqu’à 4 flux distincts. Cela signifie qu’un seul nuanceur peut sortir d’un à quatre flux de sortie, selon le nombre de flux déclarés.
ms.assetid: 2ddde992-6746-4033-9190-bde7d7b14add
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37aefd8b7cdcab05515bda6f81fa6c679751dc95
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473395"
---
# <a name="how-to-index-multiple-output-streams"></a>Comment : indexer plusieurs Flux de sortie

Dans le nuancier Model 5, un nuanceur Geometry peut prendre en charge jusqu’à 4 flux distincts. Cela signifie qu’un seul nuanceur peut sortir d’un à quatre flux de sortie, selon le nombre de flux déclarés.

Pour indexer plusieurs flux de sortie

1.  Définissez un flux de données à l’aide d’un type de modèle de flux.

    ```
        inout PointStream<OutVertex1> myStream1, 
    ```

    

2.  Définissez un deuxième flux de données à l’aide d’un type de modèle de flux.

    ```
        inout PointStream<OutVertex2> myStream2 )
    ```

    

3.  Données de sortie pour les flux (ou les deux) à l’aide des fonctions intrinsèques de l’objet de sortie de flux (par exemple, Append ou RestartStrip).

    ```
    void MyGS( 
        InVertex verts[2], 
        inout PointStream<OutVertex1> myStream1, 
        inout PointStream<OutVertex2> myStream2 )
    {
        OutVertex1 myVert1 = TransformVertex1( verts[0] );
        OutVertex2 myVert2 = TransformVertex2( verts[1] );
        myStream1.Append( myVert1 );
        myStream2.Append( myVert2 );
    }
    ```

    

Lorsque vous utilisez un seul flux de sortie, vous pouvez émettre des franges de triangle, des bandes ou des listes de points. Lorsque vous stockez des bandes triangulaires et des franges dans le tampon de sortie de flux, elles sont développées respectivement en triangle et en listes de lignes. Vous pouvez également pixelliser un flux et ne pas l’envoyer à une mémoire tampon.

Lorsque vous utilisez plusieurs flux de sortie, tous les flux doivent contenir des points, et un flux de sortie jusqu’à un peut être envoyé au rastériseur. Plus généralement, une application ne pixellise aucun flux.

Une fois que vous avez diffusé des données dans une mémoire tampon, vous pouvez utiliser ces données pour restituer n’importe quel type primitif, pas seulement le type primitif que vous avez utilisé pour remplir la mémoire tampon.

La sortie totale du nuanceur Geometry est limitée à 1024 scalaires. Lorsque plusieurs flux existent, le nombre de scalaires est calculé à partir du plus grand type de flux multiplié par le nombre maximal de vertex.




| | | Différences entre le Shader Model 4 et le Shader Model 5 :<br /> Nuanceur modèle 4 :<br /><ul><li>Le nombre maximal de scalaires pour la sortie du flux est de 64.</li><li>Le masque de Registre par composant doit correspondre dans la plage d’index.</li></ul>Nuancier modèle 5 :<br /><ul><li>Le nombre maximal de scalaires pour la sortie du flux est de 128.</li><li>Le masque de Registre par composant ne doit pas nécessairement correspondre à la plage d’index.</li><li>L’indexation dynamique des sorties doit être légale sur tous les flux.</li><li>Les modes d’interpolation n’ont pas besoin d’être identiques pour les flux.</li></ul> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités du nuanceur Geometry](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 





