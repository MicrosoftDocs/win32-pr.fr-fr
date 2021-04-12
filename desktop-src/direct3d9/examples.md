---
description: Deux exemples de définitions de modèle binaire et un exemple d’objet de données binaire suivent.
ms.assetid: vs|directx_sdk|~\examples.htm
title: Exemples (graphiques Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d26fbb8cbe45881243e17f80fd302c0fb4640685
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109162"
---
# <a name="examples-direct3d-9-graphics"></a><span data-ttu-id="3d351-103">Exemples (graphiques Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="3d351-103">Examples (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="3d351-104">Deux exemples de définitions de modèle binaire et un exemple d’objet de données binaire suivent.</span><span class="sxs-lookup"><span data-stu-id="3d351-104">Two example binary template definitions and an example of a binary data object follow.</span></span>

> [!Note]  
> <span data-ttu-id="3d351-105">Les données sont stockées au format Little endian, ce qui n’est pas illustré dans ces exemples.</span><span class="sxs-lookup"><span data-stu-id="3d351-105">Data is stored in little-endian format, which is not shown in these examples.</span></span>

 

<span data-ttu-id="3d351-106">Le modèle RGB fermé est identifié par l’UUID {55b6d780-37ec-11D0-AB39-0020af71e433} et a trois membres-r, g et b-chacun de type float.</span><span class="sxs-lookup"><span data-stu-id="3d351-106">The closed template RGB is identified by the UUID {55b6d780-37ec-11d0-ab39-0020af71e433} and has three members - r, g, and b - each of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



<span data-ttu-id="3d351-107">Le modèle Matrix4x4 fermé est identifié par l’UUID {55b6d781-37ec-11D0-AB39-0020af71e433} et possède un membre-un tableau à deux dimensions nommé Matrix-of de type float.</span><span class="sxs-lookup"><span data-stu-id="3d351-107">The closed template Matrix4x4 is identified by the UUID {55b6d781-37ec-11d0-ab39-0020af71e433} and has one member - a two-dimensional array named matrix - of type float.</span></span>


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



<span data-ttu-id="3d351-108">L’objet de données binaires qui suit montre une instance du modèle RGB défini précédemment.</span><span class="sxs-lookup"><span data-stu-id="3d351-108">The binary data object that follows shows an instance of the RGB template defined earlier.</span></span> <span data-ttu-id="3d351-109">L’objet d’exemple est nommé Blue, et ses trois membres-r, g et b ont les valeurs 0,0, 0,0 et 1,0, respectivement.</span><span class="sxs-lookup"><span data-stu-id="3d351-109">The example object is named blue, and its three members - r, g, and b - have the values 0.0, 0.0, and 1.0, respectively.</span></span>


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a><span data-ttu-id="3d351-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3d351-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3d351-111">Encodage Binaire</span><span class="sxs-lookup"><span data-stu-id="3d351-111">Binary Encoding</span></span>](binary-encoding.md)
</dt> </dl>

 

 



