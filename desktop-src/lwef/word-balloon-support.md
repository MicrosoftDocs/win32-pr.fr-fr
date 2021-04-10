---
title: Prise en charge des bulles Word
description: Prise en charge des bulles Word
ms.assetid: deac032f-0480-4a0d-bc69-e26f12666bbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f78316c509ece6fc8f9b0cefd50b1564a50697a3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196537"
---
# <a name="word-balloon-support"></a><span data-ttu-id="92622-103">Prise en charge des bulles Word</span><span class="sxs-lookup"><span data-stu-id="92622-103">Word Balloon Support</span></span>

<span data-ttu-id="92622-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="92622-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="92622-105">La sortie orale peut également apparaître sous forme de texte sous la forme d’une bulle de texte animé.</span><span class="sxs-lookup"><span data-stu-id="92622-105">Spoken output can also appear as textual output in the form of a cartoon word balloon.</span></span> <span data-ttu-id="92622-106">Cela peut être utilisé pour compléter la sortie orale d’un caractère ou comme une alternative à la sortie audio lorsque vous utilisez la méthode [**Speak**](speak-method.md) .</span><span class="sxs-lookup"><span data-stu-id="92622-106">This can be used to supplement the spoken output of a character or as an alternative to audio output when you use the [**Speak**](speak-method.md) method.</span></span>

![Oui, bulle d’un mot principal](images/f3ballon.gif)

<span data-ttu-id="92622-108">Vous pouvez également utiliser une bulle de mot pour communiquer ce qu’un caractère est en « pensant » à l’aide de la méthode de [**réflexion**](think-method.md) .</span><span class="sxs-lookup"><span data-stu-id="92622-108">You can also use a word balloon to communicate what a character is "thinking" using the [**Think**](think-method.md) method.</span></span> <span data-ttu-id="92622-109">Cela affiche le texte que vous fournissez dans une bulle toujours « pensée ».</span><span class="sxs-lookup"><span data-stu-id="92622-109">This displays the text you supply in a still "thought" balloon.</span></span> <span data-ttu-id="92622-110">La méthode de **réflexion** diffère également de la méthode [**Speak**](speak-method.md) en ce qu’elle ne produit pas de sortie audio.</span><span class="sxs-lookup"><span data-stu-id="92622-110">The **Think** method also differs from the [**Speak**](speak-method.md) method in that it produces no audio output.</span></span>

<span data-ttu-id="92622-111">Les bulles de mots ne prennent en charge que les communications sous-titrages à partir du caractère, et non des entrées utilisateur.</span><span class="sxs-lookup"><span data-stu-id="92622-111">Word balloons support only captioned communication from the character, not user input.</span></span> <span data-ttu-id="92622-112">Par conséquent, le mot Balloon ne prend pas en charge les contrôles d’entrée.</span><span class="sxs-lookup"><span data-stu-id="92622-112">Therefore, the word balloon does not support input controls.</span></span> <span data-ttu-id="92622-113">Toutefois, vous pouvez facilement fournir une entrée d’utilisateur pour un caractère, en utilisant les interfaces de votre langage de programmation ou les autres services d’entrée fournis par Microsoft Agent, tels que le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="92622-113">However, you can easily provide user input for a character, using interfaces from your programming language or the other input services provided by Microsoft Agent, such as the pop-up menu.</span></span>

<span data-ttu-id="92622-114">Lorsque vous définissez un caractère, vous pouvez spécifier s’il faut inclure la prise en charge des bulles de mots.</span><span class="sxs-lookup"><span data-stu-id="92622-114">When you define a character, you can specify whether to include word balloon support.</span></span> <span data-ttu-id="92622-115">Toutefois, si vous utilisez un caractère qui comprend la prise en charge des bulles de mots, vous ne pouvez pas désactiver la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="92622-115">However, if you use a character that includes word balloon support, you cannot disable the support.</span></span>

 

 




