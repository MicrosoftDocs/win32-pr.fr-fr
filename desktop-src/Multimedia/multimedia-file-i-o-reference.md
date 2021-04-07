---
title: Référence d’e/s de fichier multimédia
description: Référence d’e/s de fichier multimédia
ms.assetid: 1f24432e-7407-4b97-80ab-0a0c40c09253
keywords:
- Windows Multimedia, informations de référence sur les e/s de fichier
- multimédia, référence d’e/s de fichier
- entrée multimédia, référence d’e/s de fichier
- e/s de fichier multimédia, référence
- e/s de fichier, référence
- entrée et sortie (e/s), référence
- E/s (entrée et sortie), référence
- référence pour les e/s de fichier multimédia, à propos de
- informations de référence sur les e/s de fichier multimédia, à propos de
- Référence des e/s de fichier, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a0f833b7fb6677e064c19897e276d3961038cfc
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724820"
---
# <a name="multimedia-file-io-reference"></a><span data-ttu-id="3f46f-113">Référence d’e/s de fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="3f46f-113">Multimedia File I/O Reference</span></span>

<span data-ttu-id="3f46f-114">Cette section décrit les fonctions, les macros, les messages et les structures associés à l’entrée et à la sortie d’un fichier multimédia.</span><span class="sxs-lookup"><span data-stu-id="3f46f-114">This section describes the functions, macros, messages, and structures associated with multimedia file input and output.</span></span> <span data-ttu-id="3f46f-115">Ces éléments sont regroupés comme suit.</span><span class="sxs-lookup"><span data-stu-id="3f46f-115">These elements are grouped as follows.</span></span>

## <a name="basic-io"></a><span data-ttu-id="3f46f-116">E/s de base</span><span class="sxs-lookup"><span data-stu-id="3f46f-116">Basic I/O</span></span>

-   [<span data-ttu-id="3f46f-117">**mmioClose**</span><span class="sxs-lookup"><span data-stu-id="3f46f-117">**mmioClose**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose)
-   [<span data-ttu-id="3f46f-118">**mmioOpen**</span><span class="sxs-lookup"><span data-stu-id="3f46f-118">**mmioOpen**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen)
-   [<span data-ttu-id="3f46f-119">**mmioRead**</span><span class="sxs-lookup"><span data-stu-id="3f46f-119">**mmioRead**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread)
-   [<span data-ttu-id="3f46f-120">**mmioRename**</span><span class="sxs-lookup"><span data-stu-id="3f46f-120">**mmioRename**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiorename)
-   [<span data-ttu-id="3f46f-121">**mmioSeek**</span><span class="sxs-lookup"><span data-stu-id="3f46f-121">**mmioSeek**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek)
-   [<span data-ttu-id="3f46f-122">**mmioWrite**</span><span class="sxs-lookup"><span data-stu-id="3f46f-122">**mmioWrite**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite)

## <a name="buffered-io"></a><span data-ttu-id="3f46f-123">E/s mises en mémoire tampon</span><span class="sxs-lookup"><span data-stu-id="3f46f-123">Buffered I/O</span></span>

-   [<span data-ttu-id="3f46f-124">**mmioAdvance**</span><span class="sxs-lookup"><span data-stu-id="3f46f-124">**mmioAdvance**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioadvance)
-   [<span data-ttu-id="3f46f-125">**mmioFlush**</span><span class="sxs-lookup"><span data-stu-id="3f46f-125">**mmioFlush**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioflush)
-   [<span data-ttu-id="3f46f-126">**mmioGetInfo**</span><span class="sxs-lookup"><span data-stu-id="3f46f-126">**mmioGetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiogetinfo)
-   <span data-ttu-id="3f46f-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f46f-127">[**MMIOINFO**](/previous-versions//dd757322(v=vs.85))</span></span>
-   [<span data-ttu-id="3f46f-128">**mmioSetBuffer**</span><span class="sxs-lookup"><span data-stu-id="3f46f-128">**mmioSetBuffer**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetbuffer)
-   [<span data-ttu-id="3f46f-129">**mmioSetInfo**</span><span class="sxs-lookup"><span data-stu-id="3f46f-129">**mmioSetInfo**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosetinfo)

## <a name="riff-io"></a><span data-ttu-id="3f46f-130">E/S RIFF</span><span class="sxs-lookup"><span data-stu-id="3f46f-130">RIFF I/O</span></span>

-   [<span data-ttu-id="3f46f-131">**mmioAscend**</span><span class="sxs-lookup"><span data-stu-id="3f46f-131">**mmioAscend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend)
-   [<span data-ttu-id="3f46f-132">**MMCKINFO**</span><span class="sxs-lookup"><span data-stu-id="3f46f-132">**MMCKINFO**</span></span>](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo)
-   [<span data-ttu-id="3f46f-133">**mmioCreateChunk**</span><span class="sxs-lookup"><span data-stu-id="3f46f-133">**mmioCreateChunk**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk)
-   [<span data-ttu-id="3f46f-134">**mmioDescend**</span><span class="sxs-lookup"><span data-stu-id="3f46f-134">**mmioDescend**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiodescend)
-   [<span data-ttu-id="3f46f-135">**mmioFOURCC**</span><span class="sxs-lookup"><span data-stu-id="3f46f-135">**mmioFOURCC**</span></span>](/windows/win32/api/vfw/nf-vfw-mmiofourcc)
-   [<span data-ttu-id="3f46f-136">**mmioStringToFOURCC**</span><span class="sxs-lookup"><span data-stu-id="3f46f-136">**mmioStringToFOURCC**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiostringtofourcc)

## <a name="custom-io-procedures"></a><span data-ttu-id="3f46f-137">Procédures d’e/s personnalisées</span><span class="sxs-lookup"><span data-stu-id="3f46f-137">Custom I/O Procedures</span></span>

-   <span data-ttu-id="3f46f-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3f46f-138">[**IOProc**](/previous-versions//dd757098(v=vs.85))</span></span>
-   [<span data-ttu-id="3f46f-139">**mmioInstallIOProc**</span><span class="sxs-lookup"><span data-stu-id="3f46f-139">**mmioInstallIOProc**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)
-   [<span data-ttu-id="3f46f-140">**MMIOM \_ Fermer**</span><span class="sxs-lookup"><span data-stu-id="3f46f-140">**MMIOM\_CLOSE**</span></span>](mmiom-close.md)
-   [<span data-ttu-id="3f46f-141">**MMIOM \_ ouvrir**</span><span class="sxs-lookup"><span data-stu-id="3f46f-141">**MMIOM\_OPEN**</span></span>](mmiom-open.md)
-   [<span data-ttu-id="3f46f-142">**\_lecture MMIOM**</span><span class="sxs-lookup"><span data-stu-id="3f46f-142">**MMIOM\_READ**</span></span>](mmiom-read.md)
-   [<span data-ttu-id="3f46f-143">**MMIOM \_ REnommer**</span><span class="sxs-lookup"><span data-stu-id="3f46f-143">**MMIOM\_RENAME**</span></span>](mmiom-rename.md)
-   [<span data-ttu-id="3f46f-144">**MMIOM \_ Seek**</span><span class="sxs-lookup"><span data-stu-id="3f46f-144">**MMIOM\_SEEK**</span></span>](mmiom-seek.md)
-   [<span data-ttu-id="3f46f-145">**\_écriture MMIOM**</span><span class="sxs-lookup"><span data-stu-id="3f46f-145">**MMIOM\_WRITE**</span></span>](mmiom-write.md)
-   [<span data-ttu-id="3f46f-146">**MMIOM \_ WRITEFLUSH**</span><span class="sxs-lookup"><span data-stu-id="3f46f-146">**MMIOM\_WRITEFLUSH**</span></span>](mmiom-writeflush.md)
-   [<span data-ttu-id="3f46f-147">**mmioSendMessage**</span><span class="sxs-lookup"><span data-stu-id="3f46f-147">**mmioSendMessage**</span></span>](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage)

## <a name="related-topics"></a><span data-ttu-id="3f46f-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3f46f-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3f46f-149">E/s de fichier multimédia</span><span class="sxs-lookup"><span data-stu-id="3f46f-149">Multimedia File I/O</span></span>](multimedia-file-i-o.md)
</dt> </dl>

 

 