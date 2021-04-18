---
description: Les identificateurs globaux uniques (GUID) suivants sont utilisés par le journal Windows pour identifier les propriétés personnalisées sur les traits ou les attributs de dessin.
ms.assetid: a7488c26-b61f-47d8-a19b-d630a8c00875
title: GUID de propriété personnalisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eb1d9069f2c655f658752a6ae3891910ff68103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536587"
---
# <a name="custom-property-guids"></a><span data-ttu-id="c5c82-103">GUID de propriété personnalisée</span><span class="sxs-lookup"><span data-stu-id="c5c82-103">Custom Property GUIDs</span></span>

<span data-ttu-id="c5c82-104">Les identificateurs globaux uniques (GUID) suivants sont utilisés par le journal Windows pour identifier les propriétés personnalisées sur les traits ou les attributs de dessin.</span><span class="sxs-lookup"><span data-stu-id="c5c82-104">The following globally unique identifiers (GUIDs) are used by Windows Journal to identify custom properties on strokes or drawing attributes.</span></span>

## <a name="guid_stroke_timestamp"></a><span data-ttu-id="c5c82-105">\_horodateur du trait GUID \_</span><span class="sxs-lookup"><span data-stu-id="c5c82-105">GUID\_STROKE\_TIMESTAMP</span></span>


```C++
GUID_STROKE_TIMESTAMP = {4EA66C4-F33A-461B-B8FE-68070D9C7575}
```



<span data-ttu-id="c5c82-106">Il s’agit d’une structure [**fileTime**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) qui indique l’heure à laquelle le trait a été créé ou ajouté au document.</span><span class="sxs-lookup"><span data-stu-id="c5c82-106">This is a [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) structure that indicates the time at which the stroke was created or added to the document.</span></span>


```C++
typedef struct _FILETIME {
    DWORD dwLowDateTime;
    DWORD dwHighDateTime;
} FILETIME, *PFILETIME;
```



## <a name="guid_stroke_timeid"></a><span data-ttu-id="c5c82-107">\_TimeID traits \_ GUID</span><span class="sxs-lookup"><span data-stu-id="c5c82-107">GUID\_STROKE\_TIMEID</span></span>


```C++
GUID_STROKE_TIMEID = {50B6BC8-3B7D-4816-8C61-BC7E905B2132}
```



<span data-ttu-id="c5c82-108">Il s’agit d’une structure **TimeID** .</span><span class="sxs-lookup"><span data-stu-id="c5c82-108">This is a **TIMEID** structure.</span></span> <span data-ttu-id="c5c82-109">Cela permet de conserver l’ordre des traits dans les opérations de collage et de suppression.</span><span class="sxs-lookup"><span data-stu-id="c5c82-109">It allows stroke order to be maintained across paste and drop operations.</span></span> <span data-ttu-id="c5c82-110">Sans la structure **TimeID** , l’horodateur de tous les objets d' [**interface IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) coupés et collés dans une [collection InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) sera le même.</span><span class="sxs-lookup"><span data-stu-id="c5c82-110">Without the **TIMEID** structure, the timestamp for all [**IInkStrokeDisp Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects cut and pasted in a [InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) will be the same.</span></span>


```C++
typedef struct tagTIMEID {
    FILETIME  tmFiletime;
    ULONG     uiOrder;
} TIMEID;
```



## <a name="guid_highlighter"></a><span data-ttu-id="c5c82-111">\_Surligneur GUID</span><span class="sxs-lookup"><span data-stu-id="c5c82-111">GUID\_HIGHLIGHTER</span></span>

<span data-ttu-id="c5c82-112">Il s’agit d’un **bool**, où **true**= encre du surligneur, **false**= entrée normale.</span><span class="sxs-lookup"><span data-stu-id="c5c82-112">This is a **BOOL**, where **TRUE**=highlighter ink, **FALSE**=regular ink.</span></span> <span data-ttu-id="c5c82-113">Cela s’applique aux attributs de dessin.</span><span class="sxs-lookup"><span data-stu-id="c5c82-113">This is applied to drawing attributes.</span></span>


```C++
GUID_HIGHLIGHTER = {9B6267B8-3968-4048-AB74-F490406A2DFA}
```



## <a name="guid_ink_style_bold"></a><span data-ttu-id="c5c82-114">STYLE de l’encre du GUID \_ \_ \_ gras</span><span class="sxs-lookup"><span data-stu-id="c5c82-114">GUID\_INK\_STYLE\_BOLD</span></span>

<span data-ttu-id="c5c82-115">Il s’agit d’un **bool**, où **true**= écriture manuscrite, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="c5c82-115">This is a **BOOL**, where **TRUE**=bold ink, **FALSE**=normal.</span></span> <span data-ttu-id="c5c82-116">Cela s’applique aux attributs de dessin.</span><span class="sxs-lookup"><span data-stu-id="c5c82-116">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_BOLD = {E02FB5C1-9693-4312-A434-00DE7F3AD493}
```



## <a name="guid_ink_style_italics"></a><span data-ttu-id="c5c82-117">STYLE de l’encre du GUID \_ \_ \_ italique</span><span class="sxs-lookup"><span data-stu-id="c5c82-117">GUID\_INK\_STYLE\_ITALICS</span></span>

<span data-ttu-id="c5c82-118">Il s’agit d’un **bool**, où **true**= encre en italique, **false**= normal.</span><span class="sxs-lookup"><span data-stu-id="c5c82-118">This is a **BOOL**, where **TRUE**=italicized ink, **FALSE**=normal.</span></span> <span data-ttu-id="c5c82-119">Cela s’applique aux attributs de dessin.</span><span class="sxs-lookup"><span data-stu-id="c5c82-119">This is applied to drawing attributes.</span></span>


```C++
GUID_INK_STYLE_ITALICS = {05253B51-49C6-4A04-8993-64DD9ABD842A}
```



## <a name="related-topics"></a><span data-ttu-id="c5c82-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c5c82-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c5c82-121">**Interface IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="c5c82-121">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> </dl>

 

 
