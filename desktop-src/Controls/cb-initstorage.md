---
title: Message CB_INITSTORAGE (winuser. h)
description: Une application envoie le \_ message CB INITSTORAGE avant l’ajout d’un grand nombre d’éléments à la partie zone de liste d’une zone de liste déroulante. Ce message alloue de la mémoire pour le stockage des éléments de zone de liste.
ms.assetid: fb289968-a95b-4ca0-977d-b8651166f357
keywords:
- CB_INITSTORAGE les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_INITSTORAGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e78c2ae2592d89ba7a0f6392666dac0404d52e39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103628"
---
# <a name="cb_initstorage-message"></a><span data-ttu-id="ab040-105">Message de la CB- \_ INITSTORAGE</span><span class="sxs-lookup"><span data-stu-id="ab040-105">CB\_INITSTORAGE message</span></span>

<span data-ttu-id="ab040-106">Une application envoie le message **CB \_ INITSTORAGE** avant l’ajout d’un grand nombre d’éléments à la partie zone de liste d’une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ab040-106">An application sends the **CB\_INITSTORAGE** message before adding a large number of items to the list box portion of a combo box.</span></span> <span data-ttu-id="ab040-107">Ce message alloue de la mémoire pour le stockage des éléments de zone de liste.</span><span class="sxs-lookup"><span data-stu-id="ab040-107">This message allocates memory for storing list box items.</span></span>

## <a name="parameters"></a><span data-ttu-id="ab040-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab040-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab040-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ab040-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab040-110">Nombre d’éléments à ajouter.</span><span class="sxs-lookup"><span data-stu-id="ab040-110">The number of items to add.</span></span>

</dd> <dt>

<span data-ttu-id="ab040-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ab040-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ab040-112">Quantité de mémoire à allouer pour les chaînes d’élément, en octets.</span><span class="sxs-lookup"><span data-stu-id="ab040-112">The amount of memory to allocate for item strings, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab040-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab040-113">Return value</span></span>

<span data-ttu-id="ab040-114">Si le message est réussi, la valeur de retour est le nombre total d’éléments pour lesquels la mémoire a été préallouée, c’est-à-dire le nombre total d’éléments ajoutés par tous les messages **CB \_ INITSTORAGE** réussis.</span><span class="sxs-lookup"><span data-stu-id="ab040-114">If the message is successful, the return value is the total number of items for which memory has been pre-allocated, that is, the total number of items added by all successful **CB\_INITSTORAGE** messages.</span></span>

<span data-ttu-id="ab040-115">Si le message échoue, la valeur de retour est CB \_ ERRSPACE.</span><span class="sxs-lookup"><span data-stu-id="ab040-115">If the message fails, the return value is CB\_ERRSPACE.</span></span>

<span data-ttu-id="ab040-116">Le message alloue de la mémoire et retourne les valeurs de réussite et d’erreur décrites ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="ab040-116">The message allocates memory and returns the success and error values described above.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab040-117">Notes</span><span class="sxs-lookup"><span data-stu-id="ab040-117">Remarks</span></span>

<span data-ttu-id="ab040-118">Le message **CB \_ INITSTORAGE** permet d’accélérer l’initialisation des zones de liste déroulante qui ont un grand nombre d’éléments (plus de 100).</span><span class="sxs-lookup"><span data-stu-id="ab040-118">The **CB\_INITSTORAGE** message helps speed up the initialization of combo boxes that have a large number of items (over 100).</span></span> <span data-ttu-id="ab040-119">Il réserve la quantité de mémoire spécifiée afin que les messages [**CB \_ ADDSTRING**](cb-addstring.md), [**CB \_ INSERTSTRING**](cb-insertstring.md)et [**CB \_ dir**](cb-dir.md) suivants prennent le plus de temps possible.</span><span class="sxs-lookup"><span data-stu-id="ab040-119">It reserves the specified amount of memory so that subsequent [**CB\_ADDSTRING**](cb-addstring.md), [**CB\_INSERTSTRING**](cb-insertstring.md), and [**CB\_DIR**](cb-dir.md) messages take the shortest possible time.</span></span> <span data-ttu-id="ab040-120">Vous pouvez utiliser des estimations pour les paramètres *wParam* et *lParam* .</span><span class="sxs-lookup"><span data-stu-id="ab040-120">You can use estimates for the *wParam* and *lParam* parameters.</span></span> <span data-ttu-id="ab040-121">Si vous surestime, la mémoire supplémentaire est allouée, si vous sous-estimez que l’allocation normale est utilisée pour les éléments qui dépassent la quantité demandée.</span><span class="sxs-lookup"><span data-stu-id="ab040-121">If you overestimate, the extra memory is allocated, if you underestimate, the normal allocation is used for items that exceed the requested amount.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab040-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab040-122">Requirements</span></span>



| <span data-ttu-id="ab040-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab040-123">Requirement</span></span> | <span data-ttu-id="ab040-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab040-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab040-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab040-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ab040-126">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab040-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="ab040-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab040-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ab040-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab040-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="ab040-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab040-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab040-130"><dt>Winuser. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab040-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab040-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab040-131">See also</span></span>

<dl> <dt>

<span data-ttu-id="ab040-132">**Référence**</span><span class="sxs-lookup"><span data-stu-id="ab040-132">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ab040-133">**$ \_ ADDSTRING**</span><span class="sxs-lookup"><span data-stu-id="ab040-133">**CB\_ADDSTRING**</span></span>](cb-addstring.md)
</dt> <dt>

[<span data-ttu-id="ab040-134">**\_Rép.**</span><span class="sxs-lookup"><span data-stu-id="ab040-134">**CB\_DIR**</span></span>](cb-dir.md)
</dt> <dt>

[<span data-ttu-id="ab040-135">**\_INSERTSTRING CB**</span><span class="sxs-lookup"><span data-stu-id="ab040-135">**CB\_INSERTSTRING**</span></span>](cb-insertstring.md)
</dt> </dl>

 

 





