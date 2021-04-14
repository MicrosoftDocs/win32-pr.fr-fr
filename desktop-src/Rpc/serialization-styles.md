---
title: Styles de sérialisation
description: Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation.
ms.assetid: 40b609b2-abad-4967-a5d1-948ac26fd65c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc825c24b591cdfea96a603835f0836eda68b3ba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380149"
---
# <a name="serialization-styles"></a><span data-ttu-id="f0470-103">Styles de sérialisation</span><span class="sxs-lookup"><span data-stu-id="f0470-103">Serialization Styles</span></span>

<span data-ttu-id="f0470-104">Il existe trois styles que vous pouvez utiliser pour manipuler les descripteurs de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="f0470-104">There are three styles you can use to manipulate serialization handles.</span></span> <span data-ttu-id="f0470-105">Celles-ci sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0470-105">These are:</span></span>

-   [<span data-ttu-id="f0470-106">Sérialisation de mémoire tampon fixe</span><span class="sxs-lookup"><span data-stu-id="f0470-106">Fixed Buffer Serialization</span></span>](fixed-buffer-serialization.md)
-   [<span data-ttu-id="f0470-107">Sérialisation de mémoire tampon dynamique</span><span class="sxs-lookup"><span data-stu-id="f0470-107">Dynamic Buffer Serialization</span></span>](dynamic-buffer-serialization.md)
-   [<span data-ttu-id="f0470-108">Sérialisation incrémentielle</span><span class="sxs-lookup"><span data-stu-id="f0470-108">Incremental Serialization</span></span>](incremental-serialization.md)

<span data-ttu-id="f0470-109">Quel que soit le style que vous utilisez, vous devez créer un handle de sérialisation, sérialiser les données, puis libérer le handle.</span><span class="sxs-lookup"><span data-stu-id="f0470-109">Regardless of the style you use, you must create a serialization handle, serialize the data, and then free the handle.</span></span> <span data-ttu-id="f0470-110">Le style est défini lorsque votre programme crée le descripteur et définit la façon dont une mémoire tampon est manipulée.</span><span class="sxs-lookup"><span data-stu-id="f0470-110">The style is set when your program creates the handle and defines the way a buffer is manipulated.</span></span> <span data-ttu-id="f0470-111">Le handle gère le contexte approprié associé à chacun des trois styles de sérialisation.</span><span class="sxs-lookup"><span data-stu-id="f0470-111">The handle maintains the appropriate context associated with each of the three serialization styles.</span></span>

 

 




