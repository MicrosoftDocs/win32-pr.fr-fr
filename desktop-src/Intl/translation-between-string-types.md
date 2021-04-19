---
description: Les fonctions énumérées dans le tableau suivant traduisent les chaînes de caractères d’un type de chaîne en un autre.
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: Conversion entre types chaîne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524259"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="f61a7-103">Conversion entre types chaîne</span><span class="sxs-lookup"><span data-stu-id="f61a7-103">Translation Between String Types</span></span>

<span data-ttu-id="f61a7-104">Les fonctions énumérées dans le tableau suivant traduisent les chaînes de caractères d’un type de chaîne en un autre.</span><span class="sxs-lookup"><span data-stu-id="f61a7-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="f61a7-105">Fonction</span><span class="sxs-lookup"><span data-stu-id="f61a7-105">Function</span></span>                                           | <span data-ttu-id="f61a7-106">Description</span><span class="sxs-lookup"><span data-stu-id="f61a7-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="f61a7-107">**FoldString devant**</span><span class="sxs-lookup"><span data-stu-id="f61a7-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="f61a7-108">Convertit une chaîne de caractères en une autre.</span><span class="sxs-lookup"><span data-stu-id="f61a7-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="f61a7-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="f61a7-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="f61a7-110">Mappe une chaîne de caractères par paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="f61a7-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="f61a7-111">**ToUnicode**</span><span class="sxs-lookup"><span data-stu-id="f61a7-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="f61a7-112">Traduit un code de touche virtuelle en un caractère Unicode.</span><span class="sxs-lookup"><span data-stu-id="f61a7-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="f61a7-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="f61a7-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="f61a7-114">Mappe une chaîne multioctet à une chaîne Unicode.</span><span class="sxs-lookup"><span data-stu-id="f61a7-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="f61a7-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="f61a7-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="f61a7-116">Mappe une chaîne Unicode à une chaîne multioctet.</span><span class="sxs-lookup"><span data-stu-id="f61a7-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="f61a7-117">Les fonctions [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) et [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) sont particulièrement utiles pour les applications qui prennent en charge plusieurs types de chaînes.</span><span class="sxs-lookup"><span data-stu-id="f61a7-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="f61a7-118">ANSI C définit également les fonctions de conversion **wcstombs** et **mbstowcs**, mais elles peuvent uniquement être converties vers et à partir du jeu de caractères pris en charge par la bibliothèque C standard.</span><span class="sxs-lookup"><span data-stu-id="f61a7-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f61a7-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f61a7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f61a7-120">Unicode dans l'API Windows</span><span class="sxs-lookup"><span data-stu-id="f61a7-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
