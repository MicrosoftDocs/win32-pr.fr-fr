---
title: ITTSNotifySinkW
description: ITTSNotifySinkW
ms.assetid: 6305dad6-c162-458a-899e-628f6486680e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5820f262779f86deeeca9982d0551b16d3a3406
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381579"
---
# <a name="ittsnotifysinkw"></a><span data-ttu-id="88de6-103">ITTSNotifySinkW</span><span class="sxs-lookup"><span data-stu-id="88de6-103">ITTSNotifySinkW</span></span>

<span data-ttu-id="88de6-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88de6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="88de6-105">Le moteur doit appeler [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**)et [**Visual**](https://www.bing.com/search?q=**Visual**).</span><span class="sxs-lookup"><span data-stu-id="88de6-105">The engine must call out through [**AudioStop**](https://www.bing.com/search?q=**AudioStop**), [**AudioStart**](https://www.bing.com/search?q=**AudioStart**), and [**Visual**](https://www.bing.com/search?q=**Visual**).</span></span> <span data-ttu-id="88de6-106">Le rappel **visuel** doit fournir des phonèmes de la Loi.</span><span class="sxs-lookup"><span data-stu-id="88de6-106">The **Visual** callback must provide IPA phonemes.</span></span> <span data-ttu-id="88de6-107">(Alphabet \[ phonétique international \] La Loi sur la Loi est une notation universelle pour décrire le contenu phonétique de la communication orale.</span><span class="sxs-lookup"><span data-stu-id="88de6-107">(The International Phonetic Alphabet \[IPA\] is a universal notation for describing the phonetic content of spoken communication.</span></span> <span data-ttu-id="88de6-108">Tous les phonèmes parlants ont des représentations dans la Loi sur la Loi.</span><span class="sxs-lookup"><span data-stu-id="88de6-108">All speakable phonemes have representations in IPA.</span></span> <span data-ttu-id="88de6-109">Pour plus d’informations sur la Loi, consultez la section Spécification de l’API Microsoft Speech \[ du kit de développement logiciel (SDK) speech 4,0 \] à l’adresse [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx) .)</span><span class="sxs-lookup"><span data-stu-id="88de6-109">Details of IPA are in the Microsoft Speech API specification \[part of the Speech SDK 4.0 download\] at [https://www.microsoft.com/speech/](https://msdn.microsoft.com/library/ee705648.aspx).)</span></span>

<span data-ttu-id="88de6-110">Bien que la notification [**visuelle**](https://www.bing.com/search?q=**Visual**) soit assez riche, Microsoft Agent utilise uniquement la valeur **cIPAPhoneme** pour animer la bouche à mesure que le caractère parle.</span><span class="sxs-lookup"><span data-stu-id="88de6-110">Although the [**Visual**](https://www.bing.com/search?q=**Visual**) notification is fairly rich, Microsoft Agent uses only the **cIPAPhoneme** value to animate the mouth as the character speaks.</span></span> <span data-ttu-id="88de6-111">Tout moteur compatible avec Microsoft Agent doit fournir un flux de notifications **visuelles** étroitement synchronisé reflétant le contenu phonétique de l’énoncé généré.</span><span class="sxs-lookup"><span data-stu-id="88de6-111">Any Microsoft Agent-compatible engine must provide a closely synchronized stream of **Visual** notifications reflecting the phonetic content of the produced utterance.</span></span> <span data-ttu-id="88de6-112">Dans ce cas, la « notification relativement opportune » n’est pas appropriée, car les conférenciers sont assez sensibles aux différences entre la position de la bouche et le contenu acoustique.</span><span class="sxs-lookup"><span data-stu-id="88de6-112">In this case, "relatively timely notification" is not adequate, because speaker-hearers are fairly sensitive to discrepancies between mouth position and acoustic content.</span></span> <span data-ttu-id="88de6-113">Les notifications **visuelles** doivent être retournées rapidement.</span><span class="sxs-lookup"><span data-stu-id="88de6-113">**Visual** notifications need to be returned promptly.</span></span>

 

 




