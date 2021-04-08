---
title: ReaderScroll fonction de rappel
description: Fonction de rappel définie par l’application utilisée lorsque le pointeur de la souris est déplacé dans la partie de la fenêtre en mode lecteur qui a été déclarée comme zone de défilement active.
ms.assetid: b1feb661-e3bc-4fcd-9acf-ac000c3066bd
keywords:
- Contrôles Windows de fonction de rappel ReaderScroll
topic_type:
- apiref
api_name:
- ReaderScroll
- PFNREADERSCROLL
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0db5a80b84a30362e3bdbce45fe7485ad0dd6884
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942065"
---
# <a name="readerscroll-callback-function"></a><span data-ttu-id="2914e-104">ReaderScroll fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="2914e-104">ReaderScroll callback function</span></span>

<span data-ttu-id="2914e-105">\[*ReaderScroll* peut être utilisé dans les systèmes d’exploitation spécifiés dans la section Configuration requise.</span><span class="sxs-lookup"><span data-stu-id="2914e-105">\[*ReaderScroll* is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="2914e-106">Il sera peut-être modifié ou indisponible dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="2914e-106">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="2914e-107">Fonction de rappel définie par l’application utilisée lorsque le pointeur de la souris est déplacé dans la partie de la fenêtre en mode lecteur qui a été déclarée comme zone de défilement active.</span><span class="sxs-lookup"><span data-stu-id="2914e-107">An application-defined callback function used when the mouse pointer is moved within the portion of the reader mode window that has been declared as the active scrolling area.</span></span>

## <a name="syntax"></a><span data-ttu-id="2914e-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2914e-108">Syntax</span></span>


```C++
BOOL CALLBACK ReaderScroll(
  _In_ PREADERMODEINFO prmi,
  _In_ int             dx,
  _In_ int             dy
);
```



## <a name="parameters"></a><span data-ttu-id="2914e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2914e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2914e-110">*PRMI* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2914e-110">*prmi* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2914e-111">Type : **PREADERMODEINFO**</span><span class="sxs-lookup"><span data-stu-id="2914e-111">Type: **PREADERMODEINFO**</span></span>

<span data-ttu-id="2914e-112">Pointeur vers la structure [**READERMODEINFO**](readermodeinfo.md) qui a été passée à la fonction [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="2914e-112">A pointer to the [**READERMODEINFO**](readermodeinfo.md) structure that was passed to the [**DoReaderMode**](doreadermode.md) function.</span></span> <span data-ttu-id="2914e-113">Cette structure définit la fenêtre du mode lecteur et la zone de défilement active.</span><span class="sxs-lookup"><span data-stu-id="2914e-113">This structure defines the reader mode window and the active scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="2914e-114">*DX* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2914e-114">*dx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2914e-115">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="2914e-115">Type: **int**</span></span>

<span data-ttu-id="2914e-116">Distance à faire défiler horizontalement.</span><span class="sxs-lookup"><span data-stu-id="2914e-116">The distance to scroll horizontally.</span></span> <span data-ttu-id="2914e-117">Si l' \_ indicateur RMF VERTICALONLY est défini dans la structure [**READERMODEINFO**](readermodeinfo.md) , cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="2914e-117">If the RMF\_VERTICALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> <dt>

<span data-ttu-id="2914e-118">*dy* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2914e-118">*dy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2914e-119">Type : **int**</span><span class="sxs-lookup"><span data-stu-id="2914e-119">Type: **int**</span></span>

<span data-ttu-id="2914e-120">Distance à faire défiler verticalement.</span><span class="sxs-lookup"><span data-stu-id="2914e-120">The distance to scroll vertically.</span></span> <span data-ttu-id="2914e-121">Si l' \_ indicateur RMF HORIZONTALONLY est défini dans la structure [**READERMODEINFO**](readermodeinfo.md) , cette valeur est toujours 0.</span><span class="sxs-lookup"><span data-stu-id="2914e-121">If the RMF\_HORIZONTALONLY flag is set in the [**READERMODEINFO**](readermodeinfo.md) structure, this value is always 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2914e-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2914e-122">Return value</span></span>

<span data-ttu-id="2914e-123">Type : **[ **bool**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="2914e-123">Type: **[**BOOL**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="2914e-124">Cette fonction doit toujours retourner **true**.</span><span class="sxs-lookup"><span data-stu-id="2914e-124">This function should always return **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="2914e-125">Notes</span><span class="sxs-lookup"><span data-stu-id="2914e-125">Remarks</span></span>

<span data-ttu-id="2914e-126">Lorsque l’application reçoit une notification de cette fonction, l’application est chargée de faire défiler la fenêtre en mode lecteur dans le sens spécifié par les paramètres *DX* et *dy* .</span><span class="sxs-lookup"><span data-stu-id="2914e-126">When the application receives notification from this function, the application is responsible for scrolling the reader mode window in the direction specified by the *dx* and *dy* parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="2914e-127">Exemples</span><span class="sxs-lookup"><span data-stu-id="2914e-127">Examples</span></span>

<span data-ttu-id="2914e-128">L’exemple suivant présente une implémentation de cette fonction à l’aide d’une fonction personnalisée pour effectuer le défilement.</span><span class="sxs-lookup"><span data-stu-id="2914e-128">The following example outlines an implementation of this function using a custom function to accomplish the scrolling.</span></span>


```C++
BOOL CALLBACK
ReaderScrollCallback(PREADERMODEINFO prmi, int dx, int dy)
{
    if (prmi == NULL) 
        return FALSE;

    // Call custom ScrollWindow method to scroll the window
    ScrollWindow(prmi->hwnd, dx, dy);
    
    return TRUE;
}
```



## <a name="requirements"></a><span data-ttu-id="2914e-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2914e-129">Requirements</span></span>



| <span data-ttu-id="2914e-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2914e-130">Requirement</span></span> | <span data-ttu-id="2914e-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="2914e-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="2914e-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2914e-132">Minimum supported client</span></span><br/> | <span data-ttu-id="2914e-133">Windows Vista, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2914e-133">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="2914e-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2914e-134">Minimum supported server</span></span><br/> | <span data-ttu-id="2914e-135">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2914e-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

