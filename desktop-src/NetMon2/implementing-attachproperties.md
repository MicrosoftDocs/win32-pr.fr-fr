---
description: Appelle la fonction AttachProperties pour mapper les propriétés qui existent dans une partie des données reconnues.
ms.assetid: f1949904-ceb2-4650-847f-01f597ff3620
title: Implémentation de AttachProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9cc032826a8749630c4951b46d456ca807fd37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534383"
---
# <a name="implementing-attachproperties"></a><span data-ttu-id="bbad4-103">Implémentation de AttachProperties</span><span class="sxs-lookup"><span data-stu-id="bbad4-103">Implementing AttachProperties</span></span>

<span data-ttu-id="bbad4-104">Moniteur réseau appelle la fonction [**AttachProperties**](attachproperties.md) pour mapper les propriétés qui existent dans une partie des données reconnues.</span><span class="sxs-lookup"><span data-stu-id="bbad4-104">Network Monitor calls the [**AttachProperties**](attachproperties.md) function to map the properties that exist in a piece of recognized data.</span></span> <span data-ttu-id="bbad4-105">La fonction [**AttachProperties**](attachproperties.md) mappe les propriétés à un emplacement spécifique.</span><span class="sxs-lookup"><span data-stu-id="bbad4-105">The [**AttachProperties**](attachproperties.md) function maps the properties to a specific location.</span></span>

<span data-ttu-id="bbad4-106">Moniteur réseau utilise le processus suivant pour analyser les données dans un frame.</span><span class="sxs-lookup"><span data-stu-id="bbad4-106">Network Monitor uses the following process to parse the data in a frame.</span></span>

-   <span data-ttu-id="bbad4-107">Tout d’abord, Moniteur réseau appelle [RecognizeFrame](recognizeframe.md) pour reconnaître tous les protocoles qui existent dans un frame.</span><span class="sxs-lookup"><span data-stu-id="bbad4-107">First, Network Monitor calls [RecognizeFrame](recognizeframe.md) to recognize all the protocols that exist in a frame.</span></span>
-   <span data-ttu-id="bbad4-108">Moniteur réseau appelle ensuite [**AttachProperties**](attachproperties.md) pour chaque analyseur qui reconnaît un élément de données.</span><span class="sxs-lookup"><span data-stu-id="bbad4-108">Then, Network Monitor calls [**AttachProperties**](attachproperties.md) for each parser that recognizes a piece of data.</span></span>

<span data-ttu-id="bbad4-109">Lorsque Moniteur réseau appelle la fonction [AttachProperties](attachproperties.md) pour les données reconnues, l’analyseur qui est appelé doit analyser les données, puis mapper chaque propriété existante à un emplacement dans les données reconnues.</span><span class="sxs-lookup"><span data-stu-id="bbad4-109">When Network Monitor calls the [AttachProperties](attachproperties.md) function for the recognized data, the parser that is called must parse the data, and then map each existing property to a location in the recognized data.</span></span> <span data-ttu-id="bbad4-110">L’analyseur détermine les propriétés qui existent et l’emplacement où chaque propriété se trouve dans les données.</span><span class="sxs-lookup"><span data-stu-id="bbad4-110">The parser determines which properties exist, and where each property is located in the data.</span></span> <span data-ttu-id="bbad4-111">L’illustration suivante montre les données identifiées par l’analyseur.</span><span class="sxs-lookup"><span data-stu-id="bbad4-111">The following figure shows parser-recognized data.</span></span>

![données reconnues par l’analyseur](images/attachproperties1.png)

<span data-ttu-id="bbad4-113">Pendant l’implémentation de [**AttachProperties**](attachproperties.md), vous devez appeler l’une des fonctions suivantes pour chaque propriété qui existe dans une trame de données.</span><span class="sxs-lookup"><span data-stu-id="bbad4-113">During the implementation of [**AttachProperties**](attachproperties.md), you must call one of the following functions for each property that exists in a data frame.</span></span>

-   <span data-ttu-id="bbad4-114">Appelez la fonction [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) lorsque vous souhaitez modifier les données de propriété dans un frame.</span><span class="sxs-lookup"><span data-stu-id="bbad4-114">Call the [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) function when you want to modify the property data in a frame.</span></span>
-   <span data-ttu-id="bbad4-115">Appelez la fonction [**AttachPropertyInstance**](attachpropertyinstance.md) lorsque vous ne voulez pas modifier les données de propriété dans un frame.</span><span class="sxs-lookup"><span data-stu-id="bbad4-115">Call the [**AttachPropertyInstance**](attachpropertyinstance.md) function when you do not want to modify the property data in a frame.</span></span>

> [!Note]  
> <span data-ttu-id="bbad4-116">Il est recommandé d’utiliser les données telles qu’elles existent dans la capture.</span><span class="sxs-lookup"><span data-stu-id="bbad4-116">It is recommended that you use the data as it exists in the capture.</span></span>

 

<span data-ttu-id="bbad4-117">La procédure suivante identifie les étapes nécessaires à l’implémentation de [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="bbad4-117">The following procedure identifies the steps necessary to implement [**AttachProperties**](attachproperties.md).</span></span>

<span data-ttu-id="bbad4-118">**Pour implémenter AttachProperties**</span><span class="sxs-lookup"><span data-stu-id="bbad4-118">**To implement AttachProperties**</span></span>

1.  <span data-ttu-id="bbad4-119">Déterminez les propriétés qui existent et l’emplacement de la propriété dans les données.</span><span class="sxs-lookup"><span data-stu-id="bbad4-119">Determine which properties exist, and the property location in the data.</span></span>
2.  <span data-ttu-id="bbad4-120">Appelez [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) pour chaque propriété avec une valeur que vous souhaitez modifier.</span><span class="sxs-lookup"><span data-stu-id="bbad4-120">Call [**AttachPropertyInstanceEx**](attachpropertyinstanceex.md) for each property with a value that you want to modify.</span></span>
3.  <span data-ttu-id="bbad4-121">Appelez [**AttachPropertyInstance**](attachpropertyinstance.md) pour chaque propriété avec une valeur que vous ne souhaitez pas modifier.</span><span class="sxs-lookup"><span data-stu-id="bbad4-121">Call [**AttachPropertyInstance**](attachpropertyinstance.md) for each property with a value that you do not want to modify.</span></span> <span data-ttu-id="bbad4-122">En règle générale, il s’agit de la seule fonction que vous devez appeler.</span><span class="sxs-lookup"><span data-stu-id="bbad4-122">Typically, this is the only function that you need to call.</span></span>

<span data-ttu-id="bbad4-123">Voici une implémentation de base de [**AttachProperties**](attachproperties.md).</span><span class="sxs-lookup"><span data-stu-id="bbad4-123">The following is a basic implementation of [**AttachProperties**](attachproperties.md).</span></span> <span data-ttu-id="bbad4-124">N’oubliez pas que l’exemple n’inclut pas le code pour déterminer quelles propriétés existent, soit le code pour localiser les propriétés.</span><span class="sxs-lookup"><span data-stu-id="bbad4-124">Be aware that the example does not include either the code to determine which properties exist, or the code to locate the properties.</span></span>

``` syntax
#include <windows.h>

LPBYTE BHAPI MyProtocolAttachProperties( HFRAME   hFrame,
                                         LPBYTE   pMacFrame,
                                         LPBYTE   pBLRPLATEFrame,
                                         DWORD    MacType,
                                         DWORD    BytesLeft,
                                         HPROTOCOL  hPreviousProtocol,
                                         DWORD    nPrevProtocolOffset,
                                         DWORD    InstData)
{
  PBLRPLATEHDR pBLRPLATEHdr = (PBLRPLATEHDR)pBLRPLATEFrame;

  // Attach summary property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SUMMARY].hProperty,
                          (WORD)BytesLeft,
                          (LPBYTE)pBLRPLATEFrame,
                          0,        // No Help file.
                          0,        // Indent level.
                          0);      // Data flag.

  // Attach signature property.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_SIGNATURE].hProperty,
                          sizeof(DWORD),
                          &(pBLRPLATEHdr->Signature),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.


  // Attach opcode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_OPCODE].hProperty,
                          sizeof(WORD),
                          &(pBLRPLATEHdr->Opcode),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);        // Data flag.

  // Attach flags summary.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_SUMMARY].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          1,        // Indent level.
                          0);       // Data flag.

// Attach flags decode.
  AttachPropertyInstance( hFrame,
                          BLRPLATEPropertyTable[BLRPLATE_FLAGS_FLAGS].hProperty,
                          sizeof(BYTE),
                          &(pBLRPLATEHdr->Flags),
                          0,        // No Help file.
                          2,        // Indent level.
                          0);       // Data flag.

  RETURN null;

}
```

 

 



