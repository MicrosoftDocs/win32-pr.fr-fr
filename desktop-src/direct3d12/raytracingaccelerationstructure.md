---
title: RaytracingAccelerationStructure
description: Type de ressource qui peut être déclaré en HLSL et passé dans TraceRay pour indiquer la ressource d’accélération de niveau supérieur générée à l’aide de BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106525785"
---
# <a name="raytracingaccelerationstructure"></a><span data-ttu-id="4cd31-103">RaytracingAccelerationStructure</span><span class="sxs-lookup"><span data-stu-id="4cd31-103">RaytracingAccelerationStructure</span></span>

<span data-ttu-id="4cd31-104">Type de ressource qui peut être déclaré en HLSL et passé dans [**TraceRay**](traceray-function.md) pour indiquer la ressource d’accélération de niveau supérieur générée à l’aide de **BuildRaytracingAccelerationStructure**.</span><span class="sxs-lookup"><span data-stu-id="4cd31-104">A resource type that can be declared in HLSL and passed into [**TraceRay**](traceray-function.md) to indicate the top-level acceleration resource built using **BuildRaytracingAccelerationStructure**.</span></span> <span data-ttu-id="4cd31-105">Il est lié en tant que tampon brut SRV dans une table de descripteurs ou un descripteur racine SRV.</span><span class="sxs-lookup"><span data-stu-id="4cd31-105">It is bound as a raw buffer SRV in a descriptor table or root descriptor SRV.</span></span>  <span data-ttu-id="4cd31-106">La déclaration en langage HLSL est la suivante :</span><span class="sxs-lookup"><span data-stu-id="4cd31-106">The declaration in HLSL is as follows:</span></span>


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

<span data-ttu-id="4cd31-107">Cet exemple montre un tableau de taille illimitée de structures d’accélération, ce qui implique de venir d’un tas de descripteur puisque les descripteurs racine ne peuvent pas être indexés.</span><span class="sxs-lookup"><span data-stu-id="4cd31-107">This example shows an unbounded size array of acceleration structures, which implies coming from a descriptor heap since root descriptors can’t be indexed.</span></span>

<span data-ttu-id="4cd31-108">**RaytracingAccelerationStructure** est une ressource opaque sans aucune méthode disponible pour les nuanceurs.</span><span class="sxs-lookup"><span data-stu-id="4cd31-108">**RaytracingAccelerationStructure** is an opaque resource with no methods available to shaders.</span></span>


 

 




