---
title: S’assurer que le texte est affiché avec le sens de lecture correct
description: Certains langages, tels que l’arabe et l’hébreu, requièrent un sens de lecture de droite à gauche.
ms.assetid: fa9a3dd6-575a-4877-a488-22845c6726c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5d97eee49a830986718c04b4adab7443e488093
ms.sourcegitcommit: 43b2f5209d67eae96b17c03bac2a2afab1f4d30a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730172"
---
# <a name="ensure-text-is-displayed-with-the-correct-reading-direction"></a><span data-ttu-id="cc11d-103">S’assurer que le texte est affiché avec le sens de lecture correct</span><span class="sxs-lookup"><span data-stu-id="cc11d-103">Ensure text is displayed with the correct reading direction</span></span>

<span data-ttu-id="cc11d-104">Certains langages, tels que l’arabe et l’hébreu, requièrent un sens de lecture de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="cc11d-104">Some languages, such as Arabic and Hebrew, require a right-to-left reading direction.</span></span> <span data-ttu-id="cc11d-105">Pour un objet de format de texte [DirectWrite](direct-write-portal.md) , le sens de lecture par défaut est de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="cc11d-105">For a [DirectWrite](direct-write-portal.md) text format object, the default reading direction is left-to-right.</span></span> <span data-ttu-id="cc11d-106">DirectWrite ne déduit pas automatiquement le sens de lecture des paramètres régionaux. vous devez donc le faire vous-même.</span><span class="sxs-lookup"><span data-stu-id="cc11d-106">DirectWrite does not automatically infer the reading direction from the locale, so you must do this yourself.</span></span>

<span data-ttu-id="cc11d-107">Tout d’abord, récupérez les indicateurs de style étendus pour la fenêtre dans laquelle le texte sera rendu à l’aide de la macro GetWindowStyleEx définie dans windowsx. h.</span><span class="sxs-lookup"><span data-stu-id="cc11d-107">First, get the extended style flags for the window that the text will be rendered to by using the GetWindowStyleEx macro defined in windowsx.h.</span></span>


```C++
// Get the window extended style flagsfor the current window.
DWORD dwStyle = GetWindowExStyle(hwnd_);
```



<span data-ttu-id="cc11d-108">La macro retourne une valeur DWORD composée de plusieurs indicateurs associés à des opérations de bits or.</span><span class="sxs-lookup"><span data-stu-id="cc11d-108">The macro returns a DWORD value made up of several flags combined with bitwise OR operations.</span></span> <span data-ttu-id="cc11d-109">Vous devez déterminer si les indicateurs spécifiques qui affectent le sens de lecture sont là.</span><span class="sxs-lookup"><span data-stu-id="cc11d-109">You must determine if the specific flags affecting reading direction are there.</span></span>

<span data-ttu-id="cc11d-110">Il existe 2 indicateurs différents associés à la direction de lecture : WS \_ ex \_ LAYOUTRTL et WS \_ ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="cc11d-110">There are 2 different flags that are related to the reading direction: WS\_EX\_LAYOUTRTL and WS\_EX\_RTLREADING.</span></span>

<span data-ttu-id="cc11d-111">Utilisez l’opérateur and au niveau du bit (&) avec la variable dwStyle et la \_ macro WS ex \_ LAYOUTRTL pour stocker une valeur bool qui indique si la disposition est mise en miroir.</span><span class="sxs-lookup"><span data-stu-id="cc11d-111">Use the bitwise AND operator (&) with the dwStyle variable and the WS\_EX\_LAYOUTRTL macro to store a BOOL value that indicates if the layout is mirrored.</span></span>


```C++
// Is the WS_EX_LAYOUTRTL flag present?
BOOL bWSLayout = dwStyle & WS_EX_LAYOUTRTL;
```



<span data-ttu-id="cc11d-112">Faites la même chose pour l' \_ indicateur WS ex \_ RTLREADING.</span><span class="sxs-lookup"><span data-stu-id="cc11d-112">Do the same thing for the WS\_EX\_RTLREADING flag.</span></span>


```C++
// Is the WS_EX_RLTREADING flag present?
BOOL bWSReading = dwStyle & WS_EX_RTLREADING;
```



<span data-ttu-id="cc11d-113">Définissez le sens de lecture à l’aide de la méthode [**IDWriteTextFormat :: SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) .</span><span class="sxs-lookup"><span data-stu-id="cc11d-113">Set the reading direction by using the [**IDWriteTextFormat::SetReadingDirection**](/windows/win32/api/dwrite/nf-dwrite-idwritetextformat-setreadingdirection) method.</span></span> <span data-ttu-id="cc11d-114">La valeur par défaut est de gauche à droite. vous devez donc uniquement définir la direction de lecture si elle est de droite à gauche.</span><span class="sxs-lookup"><span data-stu-id="cc11d-114">The default is left-to-right, so you only need to set the reading direction if it is right-to-left.</span></span>

> [!Note]  
> <span data-ttu-id="cc11d-115">WS \_ ex \_ LAYOUTRTL reflète la totalité de la disposition et implique un sens de lecture de droite à gauche. par conséquent, définissez le sens de lecture uniquement si l’un de ces indicateurs est présent.</span><span class="sxs-lookup"><span data-stu-id="cc11d-115">WS\_EX\_LAYOUTRTL mirrors the whole layout and implies right-to-left reading direction, so set the reading direction only if one of these flags is present.</span></span> <span data-ttu-id="cc11d-116">Si les deux sont présents, ils s’annulent l’un l’autre et le sens de lecture du format texte doit être de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="cc11d-116">If both are present, they cancel one another out and the reading direction for the text format should be left-to-right.</span></span>

 


```C++
// If either the WS_EX_LAYOUTRTL flag or the WS_EX_RLTREADING flag is present,
// but NOT BOTH, set the reading direction to right to left.
if ((bWSLayout && !bWSReading)
||  (!bWSLayout && bWSReading))
{
    pTextFormat_->SetReadingDirection(DWRITE_READING_DIRECTION_RIGHT_TO_LEFT);
}
```



 

 
