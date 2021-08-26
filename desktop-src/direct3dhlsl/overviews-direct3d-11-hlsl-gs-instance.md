---
title: Comment instancier un nuanceur Geometry
description: L’instanciation de nuanceur Geometry permet l’exécution de plusieurs exécutions du même nuanceur Geometry par primitive.
ms.assetid: e3d8616b-7129-40e9-99fc-2852914a80b0
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 866b0cedb4de0fe2f8bf9087df6637d3a6340505289b4b773eaccd380fa4b367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067919"
---
# <a name="how-to-instance-a-geometry-shader"></a>Comment : instancier un nuanceur Geometry

L’instanciation de nuanceur Geometry permet l’exécution de plusieurs exécutions du même nuanceur Geometry par primitive. Pour instancier un nuanceur Geometry, ajoutez un attribut d’instance à la fonction de nuanceur principale et identifiez un paramètre d’index d’instance dans le corps de la fonction de nuanceur.

Pour instancier un nuanceur Geometry :

1.  Ajoutez l' [attribut d’instance](sm5-attributes-instance.md) à la fonction main.

    ```
    [instance(24)]
    ```

    

    Cela définit le nombre d’instances (au maximum 32) à exécuter pour chaque primitive.

2.  Attachez la valeur système [SV \_ GSInstanceID](sv-gsinstanceid.md) à une variable dans la liste des paramètres de fonction qui peut être utilisée pour suivre l’ID de l’instance en cours d’exécution.
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  Compilez et créez le nuanceur comme vous le feriez pour tout autre nuanceur Geometry.

Autres détails :

-   Le nombre maximal d’instances est 32.
-   Le nombre maximal de vertex est un nombre maximal de vertex par instance.
-   Chaque appel d’instance (comme tout appel de nuanceur Geometry) augmente le nombre d’appels et génère un RestartStrip implicite ().

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités du nuanceur Geometry](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




