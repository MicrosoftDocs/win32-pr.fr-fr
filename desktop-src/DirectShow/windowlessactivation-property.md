---
description: La propriété WindowlessActivation Initialise l’objet MSWebDVD au moment de la conception pour le mode fenêtre ou sans fenêtre.
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: Propriété WindowlessActivation
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534103"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="dabc8-103">Propriété WindowlessActivation</span><span class="sxs-lookup"><span data-stu-id="dabc8-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="dabc8-104">Ce composant peut être utilisé dans les systèmes d’exploitation Microsoft Windows 2000, Windows XP et Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="dabc8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="dabc8-105">Il sera peut-être modifié ou indisponible dans les versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="dabc8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="dabc8-106">La `WindowlessActivation` propriété Initialise l’objet **mswebdvd** au moment du design pour le mode fenêtre ou sans fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dabc8-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="dabc8-107">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dabc8-107">Return Value</span></span>

<span data-ttu-id="dabc8-108">Retourne une valeur indiquant si l’objet est en mode fenêtre sous forme de valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="dabc8-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="dabc8-109">Notes</span><span class="sxs-lookup"><span data-stu-id="dabc8-109">Remarks</span></span>

<span data-ttu-id="dabc8-110">Cette propriété est en lecture/écriture et sa valeur par défaut est true.</span><span class="sxs-lookup"><span data-stu-id="dabc8-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="dabc8-111">Par conséquent, il vous suffit de définir cette propriété si vous exécutez l’objet **mswebdvd** dans un conteneur en fenêtre.</span><span class="sxs-lookup"><span data-stu-id="dabc8-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="dabc8-112">Lorsqu’il est contenu dans une page Web de Microsoft® Internet Explorer, **mswebdvd** est toujours en mode sans fenêtre, et vous n’avez pas besoin de définir cette propriété.</span><span class="sxs-lookup"><span data-stu-id="dabc8-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



