---
title: Message LB_ADDFILE (winuser. h)
description: Ajoute le nom de fichier spécifié à une zone de liste qui contient une liste de répertoires.
ms.assetid: 60426293-779b-4a4b-95a2-4901b5f6a13b
keywords:
- LB_ADDFILE les contrôles de message Windows
topic_type:
- apiref
api_name:
- LB_ADDFILE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18b3d66c6a6c8495c67df2078370911ca9cd31df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466338"
---
# <a name="lb_addfile-message"></a><span data-ttu-id="0b06d-104">\_Message ADDFILE lb</span><span class="sxs-lookup"><span data-stu-id="0b06d-104">LB\_ADDFILE message</span></span>

<span data-ttu-id="0b06d-105">Ajoute le nom de fichier spécifié à une zone de liste qui contient une liste de répertoires.</span><span class="sxs-lookup"><span data-stu-id="0b06d-105">Adds the specified filename to a list box that contains a directory listing.</span></span>

## <a name="parameters"></a><span data-ttu-id="0b06d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0b06d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b06d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0b06d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b06d-108">Ce paramètre n'est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="0b06d-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0b06d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0b06d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0b06d-110">Pointeur vers une mémoire tampon qui spécifie le nom du fichier à ajouter.</span><span class="sxs-lookup"><span data-stu-id="0b06d-110">A pointer to a buffer that specifies the name of the file to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b06d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0b06d-111">Return value</span></span>

<span data-ttu-id="0b06d-112">La valeur de retour est l’index de base zéro du fichier qui a été ajouté ou LB \_ Err si une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="0b06d-112">The return value is the zero-based index of the file that was added, or LB\_ERR if an error occurs.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b06d-113">Notes</span><span class="sxs-lookup"><span data-stu-id="0b06d-113">Remarks</span></span>

<span data-ttu-id="0b06d-114">La zone de liste à laquelle *lParam* est ajouté doit avoir été remplie par la fonction [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) .</span><span class="sxs-lookup"><span data-stu-id="0b06d-114">The list box to which *lParam* is added must have been filled by the [**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista) function.</span></span>

<span data-ttu-id="0b06d-115">Le message [**lb \_ INITSTORAGE**](lb-initstorage.md) permet d’accélérer l’initialisation des zones de liste qui comportent un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="0b06d-115">The [**LB\_INITSTORAGE**](lb-initstorage.md) message helps speed up the initialization of list boxes that have a large number of items (more than 100).</span></span> <span data-ttu-id="0b06d-116">Il réserve la quantité de mémoire spécifiée afin que les **messages \_ ADDFILE** suivants prennent le plus rapidement possible.</span><span class="sxs-lookup"><span data-stu-id="0b06d-116">It reserves the specified amount of memory so that subsequent **LB\_ADDFILE** messages take the shortest possible time.</span></span> <span data-ttu-id="0b06d-117">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="0b06d-117">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="0b06d-118">Si vous surestime, la mémoire supplémentaire est allouée. Si vous sous-estimez, l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="0b06d-118">If you overestimate, the extra memory is allocated; if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

<span data-ttu-id="0b06d-119">Pour une application ANSI, le système convertit le texte d’une zone de liste en Unicode à l’aide de CP \_ ACP.</span><span class="sxs-lookup"><span data-stu-id="0b06d-119">For an ANSI application, the system converts the text in a list box to Unicode using CP\_ACP.</span></span> <span data-ttu-id="0b06d-120">Cela peut entraîner des problèmes.</span><span class="sxs-lookup"><span data-stu-id="0b06d-120">This can cause problems.</span></span> <span data-ttu-id="0b06d-121">Par exemple, les caractères romains accentués dans une zone de liste non Unicode dans les fenêtres japonaises sont tronqués.</span><span class="sxs-lookup"><span data-stu-id="0b06d-121">For example, accented Roman characters in a non-Unicode list box in Japanese Windows will come out garbled.</span></span> <span data-ttu-id="0b06d-122">Pour résoudre ce problème, compilez l’application en Unicode ou utilisez une zone de liste owner-drawn.</span><span class="sxs-lookup"><span data-stu-id="0b06d-122">To fix this, either compile the application as Unicode or use an owner-drawn list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b06d-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0b06d-123">Requirements</span></span>



| <span data-ttu-id="0b06d-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0b06d-124">Requirement</span></span> | <span data-ttu-id="0b06d-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0b06d-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b06d-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b06d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0b06d-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b06d-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0b06d-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0b06d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0b06d-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0b06d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0b06d-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="0b06d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b06d-131"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b06d-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b06d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0b06d-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="0b06d-133">**Référence**</span><span class="sxs-lookup"><span data-stu-id="0b06d-133">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0b06d-134">**DlgDirList**</span><span class="sxs-lookup"><span data-stu-id="0b06d-134">**DlgDirList**</span></span>](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> <dt>

[<span data-ttu-id="0b06d-135">**LB \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="0b06d-135">**LB\_ADDSTRING**</span></span>](lb-addstring.md)
</dt> </dl>

 

 





