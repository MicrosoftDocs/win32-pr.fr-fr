---
description: Les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la \_ structure du type de média am \_ .
ms.assetid: 4dbea5b4-bf78-4253-be48-d81b77be6e77
title: Fonctions de type de média (mtype. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Media
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a39fe9a9599a1d85c14a226106f5c8d7080b721f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540963"
---
# <a name="media-type-functions"></a><span data-ttu-id="afe2d-103">Fonctions de type de média</span><span class="sxs-lookup"><span data-stu-id="afe2d-103">Media Type Functions</span></span>

<span data-ttu-id="afe2d-104">Les classes de base DirectShow fournissent des fonctions d’assistance pour gérer la structure du [**\_ \_ type de média am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="afe2d-104">The DirectShow base classes provides helper functions for handling the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span>

<span data-ttu-id="afe2d-105">La structure du **\_ \_ type de média am** contient un pointeur (le membre **pbFormat** ) vers un autre bloc de mémoire, appelé le *bloc de format*.</span><span class="sxs-lookup"><span data-stu-id="afe2d-105">The **AM\_MEDIA\_TYPE** structure contains a pointer (the **pbFormat** member) to another block of memory, which is called the *format block*.</span></span> <span data-ttu-id="afe2d-106">Par conséquent, lorsque vous utilisez cette structure, vous devez faire attention à l’allocation de mémoire afin d’éviter les fuites de mémoire.</span><span class="sxs-lookup"><span data-stu-id="afe2d-106">When you work with this structure, therefore, you must be careful about memory allocation in order to avoid memory leaks.</span></span>

<span data-ttu-id="afe2d-107">Les fonctions suivantes allouent de la mémoire :</span><span class="sxs-lookup"><span data-stu-id="afe2d-107">The following functions allocate memory:</span></span>

-   <span data-ttu-id="afe2d-108">**CreateMediaType** alloue une nouvelle structure **de \_ \_ type de média am** et le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="afe2d-108">**CreateMediaType** allocates a new **AM\_MEDIA\_TYPE** structure and the format block.</span></span>
-   <span data-ttu-id="afe2d-109">**CopyMediaType** copie dans une structure **de \_ \_ type de média am** existante, mais alloue le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="afe2d-109">**CopyMediaType** copies to an existing **AM\_MEDIA\_TYPE** structure, but allocates the format block.</span></span>
-   <span data-ttu-id="afe2d-110">**CreateAudioMediaType** Initialise une structure de **\_ \_ type de média am** existante et alloue éventuellement le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="afe2d-110">**CreateAudioMediaType** initializes an existing **AM\_MEDIA\_TYPE** structure, and optionally allocates the format block.</span></span>

<span data-ttu-id="afe2d-111">La mémoire disponible pour les fonctions suivantes :</span><span class="sxs-lookup"><span data-stu-id="afe2d-111">The following functions free memory:</span></span>

-   <span data-ttu-id="afe2d-112">**FreeMediaType** libère le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="afe2d-112">**FreeMediaType** releases the format block.</span></span>
-   <span data-ttu-id="afe2d-113">**DeleteMediaType** libère une structure **de \_ \_ type de média am** , y compris le bloc de format.</span><span class="sxs-lookup"><span data-stu-id="afe2d-113">**DeleteMediaType** frees an **AM\_MEDIA\_TYPE** structure, including the format block.</span></span>



| <span data-ttu-id="afe2d-114">Fonction</span><span class="sxs-lookup"><span data-stu-id="afe2d-114">Function</span></span>                                             | <span data-ttu-id="afe2d-115">Description</span><span class="sxs-lookup"><span data-stu-id="afe2d-115">Description</span></span>                                                                                                 |
|------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afe2d-116">**CopyMediaType**</span><span class="sxs-lookup"><span data-stu-id="afe2d-116">**CopyMediaType**</span></span>](copymediatype.md)               | <span data-ttu-id="afe2d-117">Copie une structure de **type de \_ média \_ am** allouée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="afe2d-117">Copies a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                      |
| [<span data-ttu-id="afe2d-118">**CreateAudioMediaType**</span><span class="sxs-lookup"><span data-stu-id="afe2d-118">**CreateAudioMediaType**</span></span>](createaudiomediatype.md) | <span data-ttu-id="afe2d-119">Initialise une structure de type de média en fonction d’une structure de format Wave.</span><span class="sxs-lookup"><span data-stu-id="afe2d-119">Initializes a media type structure given a wave format structure.</span></span>                                           |
| [<span data-ttu-id="afe2d-120">**CreateMediaType**</span><span class="sxs-lookup"><span data-stu-id="afe2d-120">**CreateMediaType**</span></span>](createmediatype.md)           | <span data-ttu-id="afe2d-121">Alloue et Initialise une structure de **\_ \_ type de média am** , à partir d’une structure de **\_ \_ type de média am** existante.</span><span class="sxs-lookup"><span data-stu-id="afe2d-121">Allocates and initializes an **AM\_MEDIA\_TYPE** structure, from an existing **AM\_MEDIA\_TYPE** structure.</span></span> |
| [<span data-ttu-id="afe2d-122">**DeleteMediaType**</span><span class="sxs-lookup"><span data-stu-id="afe2d-122">**DeleteMediaType**</span></span>](deletemediatype.md)           | <span data-ttu-id="afe2d-123">Supprime une structure de **\_ \_ type de média am** allouée par la tâche.</span><span class="sxs-lookup"><span data-stu-id="afe2d-123">Deletes a task-allocated **AM\_MEDIA\_TYPE** structure.</span></span>                                                     |
| [<span data-ttu-id="afe2d-124">**FreeMediaType**</span><span class="sxs-lookup"><span data-stu-id="afe2d-124">**FreeMediaType**</span></span>](freemediatype.md)               | <span data-ttu-id="afe2d-125">Libère une structure de **\_ \_ type de média am** allouée à la tâche à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="afe2d-125">Frees a task-allocated **AM\_MEDIA\_TYPE** structure from memory.</span></span>                                           |



 

## <a name="requirements"></a><span data-ttu-id="afe2d-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="afe2d-126">Requirements</span></span>



| <span data-ttu-id="afe2d-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="afe2d-127">Requirement</span></span> | <span data-ttu-id="afe2d-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="afe2d-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afe2d-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="afe2d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="afe2d-130"><dt>Mtype. h (include streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="afe2d-130"><dt>Mtype.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="afe2d-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="afe2d-131">Library</span></span><br/> | <dl> <span data-ttu-id="afe2d-132"><dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt></span><span class="sxs-lookup"><span data-stu-id="afe2d-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




