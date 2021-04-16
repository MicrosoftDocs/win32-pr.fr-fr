---
title: Fonctions d’e/s de fichier multimédia
description: Fonctions d’e/s de fichier multimédia
ms.assetid: a5d51906-881f-4fe0-a988-c10776a3b40d
keywords:
- Windows Multimedia, fonctions d’e/s de fichier
- multimédia, fonctions d’e/s de fichier
- entrée multimédia, fonctions d’e/s de fichier
- e/s de fichier multimédia, fonctions
- e/s de fichier, fonctions
- entrées et sorties (e/s), fonctions
- E/s (entrée et sortie), fonctions
- référence pour les e/s de fichier multimédia, fonctions
- informations de référence sur les e/s de fichier multimédia, fonctions
- Référence des e/s de fichier, fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62b8daf8e84953acebcca9106165f27b350ef2f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104507874"
---
# <a name="multimedia-file-io-functions"></a><span data-ttu-id="a92ed-113">Fonctions d’e/s de fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="a92ed-113">Multimedia File I/O Functions</span></span>

<span data-ttu-id="a92ed-114">Les fonctions suivantes sont utilisées avec les e/s de fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="a92ed-114">The following functions are used with multimedia file I/O.</span></span>

-   <span data-ttu-id="a92ed-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="a92ed-115">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="a92ed-116">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="a92ed-116">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="a92ed-117">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="a92ed-117">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="a92ed-118">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="a92ed-118">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="a92ed-119">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="a92ed-119">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="a92ed-120">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="a92ed-120">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="a92ed-121">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="a92ed-121">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="a92ed-122">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="a92ed-122">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   [<span data-ttu-id="a92ed-123">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="a92ed-123">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="a92ed-124">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="a92ed-124">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="a92ed-125">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="a92ed-125">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="a92ed-126">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="a92ed-126">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="a92ed-127">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="a92ed-127">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="a92ed-128">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="a92ed-128">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)
-   [<span data-ttu-id="a92ed-129">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="a92ed-129">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="a92ed-130">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="a92ed-130">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)
-   [<span data-ttu-id="a92ed-131">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="a92ed-131">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)
-   [<span data-ttu-id="a92ed-132">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="a92ed-132">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="related-topics"></a><span data-ttu-id="a92ed-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a92ed-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a92ed-134">Référence d’e/s de fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="a92ed-134">Multimedia File I/O Reference</span></span>](multimedia-file-i-o-reference.md)
</dt> </dl>

 

 