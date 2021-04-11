---
description: En définissant la propriété Factoid sur None, le module de reconnaissance de caractères reconnaît l’écriture manuscrite caractère par caractère.
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: Word et reconnaissance de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112874"
---
# <a name="word-vs-character-recognition"></a><span data-ttu-id="aa7aa-103">Word et reconnaissance de caractères</span><span class="sxs-lookup"><span data-stu-id="aa7aa-103">Word vs. Character Recognition</span></span>

<span data-ttu-id="aa7aa-104">En définissant la propriété [Factoid](/previous-versions/ms835848(v=msdn.10)) sur **None**, le module de reconnaissance de caractères reconnaît l’écriture manuscrite caractère par caractère.</span><span class="sxs-lookup"><span data-stu-id="aa7aa-104">By setting the [Factoid](/previous-versions/ms835848(v=msdn.10)) property to **None**, the character recognizer recognizes handwriting on a character-by-character basis.</span></span>

<span data-ttu-id="aa7aa-105">La propriété [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) dans Automation) spécifie le nombre de millisecondes de délai entre le dernier [trait](/previous-versions/ms552692(v=vs.100)) et la fin de l’entrée d’écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="aa7aa-105">The [RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) property specifies the number of milliseconds of delay between the last [Stroke](/previous-versions/ms552692(v=vs.100)) and the end of handwriting input.</span></span> <span data-ttu-id="aa7aa-106">Vous pouvez augmenter cette valeur pour reconnaître du texte avant l’écriture de mots ou de phrases entiers.</span><span class="sxs-lookup"><span data-stu-id="aa7aa-106">You can increase this value to recognize text before entire words or sentences are written.</span></span> <span data-ttu-id="aa7aa-107">Vous pouvez également forcer la reconnaissance de l’encre immédiatement à l’aide de la méthode [Recognize](/previous-versions/ms836275(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="aa7aa-107">You can also force the recognition of ink immediately by using the [Recognize](/previous-versions/ms836275(v=msdn.10)) method.</span></span>

 

 
