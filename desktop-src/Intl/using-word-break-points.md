---
description: Lorsque l’application traite des mots entiers, les positions valides pour le signe insertion sont marquées par la valeur du membre fWordStop de la \_ structure script LOGATTR. Cette valeur est récupérée en effectuant un appel à ScriptBreak.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Utilisation des points d’arrêt de mot
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210932"
---
# <a name="using-word-break-points"></a><span data-ttu-id="62485-104">Utilisation des points d’arrêt de mot</span><span class="sxs-lookup"><span data-stu-id="62485-104">Using Word Break Points</span></span>

<span data-ttu-id="62485-105">Lorsque l’application traite des mots entiers, les positions valides pour le signe insertion sont marquées par la valeur du membre **fWordStop** de la structure [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) .</span><span class="sxs-lookup"><span data-stu-id="62485-105">When the application is dealing with whole words, valid positions for the caret are marked by the value of the **fWordStop** member of the [**SCRIPT\_LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr) structure.</span></span> <span data-ttu-id="62485-106">Cette valeur est récupérée en effectuant un appel à [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="62485-106">This value is retrieved by making a call to [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

<span data-ttu-id="62485-107">Les positions valides pour les sauts de ligne entre les mots sont marquées par la valeur **fSoftBreak** récupérée par [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span><span class="sxs-lookup"><span data-stu-id="62485-107">Valid positions for breaking lines between words are marked by the **fSoftBreak** value retrieved by [**ScriptBreak**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62485-108">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="62485-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62485-109">Utilisation de Uniscribe</span><span class="sxs-lookup"><span data-stu-id="62485-109">Using Uniscribe</span></span>](using-uniscribe.md)
</dt> </dl>

 

 



