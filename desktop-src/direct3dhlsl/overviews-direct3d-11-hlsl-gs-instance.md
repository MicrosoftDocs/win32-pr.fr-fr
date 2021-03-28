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
ms.openlocfilehash: 7858de7d8526a9468d3ebd0a07d57777983a66db
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104990644"
---
# <a name="how-to-instance-a-geometry-shader"></a><span data-ttu-id="432db-103">Comment : instancier un nuanceur Geometry</span><span class="sxs-lookup"><span data-stu-id="432db-103">How To: Instance a Geometry Shader</span></span>

<span data-ttu-id="432db-104">L’instanciation de nuanceur Geometry permet l’exécution de plusieurs exécutions du même nuanceur Geometry par primitive.</span><span class="sxs-lookup"><span data-stu-id="432db-104">Geometry shader instancing allows multiple executions of the same geometry shader to be executed per primitive.</span></span> <span data-ttu-id="432db-105">Pour instancier un nuanceur Geometry, ajoutez un attribut d’instance à la fonction de nuanceur principale et identifiez un paramètre d’index d’instance dans le corps de la fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="432db-105">To instance a geometry shader, add an instance attribute to the main shader function and identify an instance index parameter in the shader function body.</span></span>

<span data-ttu-id="432db-106">Pour instancier un nuanceur Geometry :</span><span class="sxs-lookup"><span data-stu-id="432db-106">To Instance a Geometry Shader:</span></span>

1.  <span data-ttu-id="432db-107">Ajoutez l' [attribut d’instance](sm5-attributes-instance.md) à la fonction main.</span><span class="sxs-lookup"><span data-stu-id="432db-107">Add the [instance attribute](sm5-attributes-instance.md) to the main function.</span></span>

    ```
    [instance(24)]
    ```

    

    <span data-ttu-id="432db-108">Cela définit le nombre d’instances (au maximum 32) à exécuter pour chaque primitive.</span><span class="sxs-lookup"><span data-stu-id="432db-108">This defines the number of instances (a maximum of 32) to be run for each primitive.</span></span>

2.  <span data-ttu-id="432db-109">Attachez la valeur système [SV \_ GSInstanceID](sv-gsinstanceid.md) à une variable dans la liste des paramètres de fonction qui peut être utilisée pour suivre l’ID de l’instance en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="432db-109">Attach the [SV\_GSInstanceID](sv-gsinstanceid.md) system value to a variable in the function parameter list that can be used to track the ID of the instance being executed.</span></span>
    ```
    uint InstanceID : SV_GSInstanceID
    ```

    

3.  <span data-ttu-id="432db-110">Compilez et créez le nuanceur comme vous le feriez pour tout autre nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="432db-110">Compile and create the shader just as you would any other geometry shader.</span></span>

<span data-ttu-id="432db-111">Autres détails :</span><span class="sxs-lookup"><span data-stu-id="432db-111">Other details include:</span></span>

-   <span data-ttu-id="432db-112">Le nombre maximal d’instances est 32.</span><span class="sxs-lookup"><span data-stu-id="432db-112">The maximum instance count is 32.</span></span>
-   <span data-ttu-id="432db-113">Le nombre maximal de vertex est un nombre maximal de vertex par instance.</span><span class="sxs-lookup"><span data-stu-id="432db-113">The maximum vertex count is a per-instance maximum vertex count.</span></span>
-   <span data-ttu-id="432db-114">Chaque appel d’instance (comme tout appel de nuanceur Geometry) augmente le nombre d’appels et génère un RestartStrip implicite ().</span><span class="sxs-lookup"><span data-stu-id="432db-114">Each instance invocation (like any geometry shader invocation) increases the invocation count and generates an implicit RestartStrip().</span></span>

## <a name="related-topics"></a><span data-ttu-id="432db-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="432db-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="432db-116">Fonctionnalités du nuanceur Geometry</span><span class="sxs-lookup"><span data-stu-id="432db-116">Geometry Shader Features</span></span>](overviews-direct3d-11-hlsl-gs-features.md)
</dt> </dl>

 

 




