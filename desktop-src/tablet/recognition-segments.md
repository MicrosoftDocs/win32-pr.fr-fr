---
description: Un segment de reconnaissance est l’unité d’encre de base qu’un module de reconnaissance utilise en interne pour produire un résultat de reconnaissance pour un objet d’encre particulier.
ms.assetid: 5215a0bd-6dff-4cda-b2e5-c54f64680e02
title: Segments de reconnaissance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f7037849378477950b906b85efe6980c4246421
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523417"
---
# <a name="recognition-segments"></a><span data-ttu-id="34278-103">Segments de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="34278-103">Recognition Segments</span></span>

<span data-ttu-id="34278-104">Un segment de reconnaissance est l’unité d’encre de base qu’un module de reconnaissance utilise en interne pour produire un résultat de reconnaissance pour un objet d’encre particulier.</span><span class="sxs-lookup"><span data-stu-id="34278-104">A recognition segment is the basic ink unit that a recognizer uses internally to produce a recognition result for a particular Ink object.</span></span> <span data-ttu-id="34278-105">Un segment de reconnaissance est une collection de traits d’encre.</span><span class="sxs-lookup"><span data-stu-id="34278-105">A recognition segment is a collection of ink strokes.</span></span> <span data-ttu-id="34278-106">Par exemple, un module de reconnaissance capable de reconnaître l’écriture manuscrite en anglais peut utiliser un mot comme segment de reconnaissance de base.</span><span class="sxs-lookup"><span data-stu-id="34278-106">For example, a recognizer that is capable of recognizing English cursive handwriting might use a word as the basic recognition segment.</span></span>

<span data-ttu-id="34278-107">D’autres peuvent utiliser des parties de mots composites comme segments de base.</span><span class="sxs-lookup"><span data-stu-id="34278-107">Other recognizers may use parts of composite words as basic segments.</span></span> <span data-ttu-id="34278-108">Par exemple, en espagnol, les mots courts sont couramment combinés pour fournir des mots composites plus longs.</span><span class="sxs-lookup"><span data-stu-id="34278-108">For example, in Spanish, short words are commonly combined to provide longer composite words.</span></span> <span data-ttu-id="34278-109">« Damelo » est un mot espagnol qui est composé de trois mots « da me lo » (je le donne), mais il est écrit sous la forme d’un mot unique.</span><span class="sxs-lookup"><span data-stu-id="34278-109">"Damelo" is a Spanish word that is composed of three words "da me lo" (give me that), but it is written as a single word.</span></span> <span data-ttu-id="34278-110">Un module de reconnaissance espagnol peut reconnaître chaque sous-mot en tant que segment.</span><span class="sxs-lookup"><span data-stu-id="34278-110">A Spanish recognizer could recognize each subword as a segment.</span></span>

<span data-ttu-id="34278-111">Un module de reconnaissance peut trouver plusieurs façons de diviser un échantillon d’encre en segments de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="34278-111">A recognizer may find several ways to break an ink sample into recognition segments.</span></span> <span data-ttu-id="34278-112">Étant donné que l’ambiguïté est impliquée dans la reconnaissance de l’entrée prévue de l’utilisateur, le module de reconnaissance peut retourner de nombreuses autres correspondances.</span><span class="sxs-lookup"><span data-stu-id="34278-112">Because ambiguity is involved in recognizing the user's intended input, the recognizer can return many alternate matches.</span></span>

<span data-ttu-id="34278-113">Pour plus d’informations sur les alternatives, consultez [alternatives](alternates.md).</span><span class="sxs-lookup"><span data-stu-id="34278-113">For more information about alternates, see [Alternates](alternates.md).</span></span>

 

 



