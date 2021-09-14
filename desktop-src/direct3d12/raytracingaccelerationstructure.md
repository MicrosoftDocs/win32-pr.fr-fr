---
title: RaytracingAccelerationStructure
description: Type de ressource qui peut être déclaré en HLSL et passé dans TraceRay pour indiquer la ressource d’accélération de niveau supérieur générée à l’aide de BuildRaytracingAccelerationStructure.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: beb6f5e397126223e9c0e6959e16a6cca3145517
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012905"
---
# <a name="raytracingaccelerationstructure"></a>RaytracingAccelerationStructure

Type de ressource qui peut être déclaré en HLSL et passé dans [**TraceRay**](traceray-function.md) pour indiquer la ressource d’accélération de niveau supérieur générée à l’aide de **BuildRaytracingAccelerationStructure**. Il est lié en tant que tampon brut SRV dans une table de descripteurs ou un descripteur racine SRV.  La déclaration en langage HLSL est la suivante :


```
RaytracingAccelerationStructure MyScene[] : register(t3,space1);
```

Cet exemple montre un tableau de taille illimitée de structures d’accélération, ce qui implique de venir d’un tas de descripteur puisque les descripteurs racine ne peuvent pas être indexés.

**RaytracingAccelerationStructure** est une ressource opaque sans aucune méthode disponible pour les nuanceurs.


 

 




