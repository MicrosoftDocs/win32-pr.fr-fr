---
title: Fonctions de boîte de dialogue communes
description: . | Fonctions de boîte de dialogue communes
ms.assetid: 4a94330b-e0d5-48d7-80f3-86ba6ca1f0f9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 109f0ca24f319bb27955ba117a8035df3042fb44
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106539845"
---
# <a name="common-dialog-box-functions"></a><span data-ttu-id="76ea9-104">Fonctions de boîte de dialogue communes</span><span class="sxs-lookup"><span data-stu-id="76ea9-104">Common Dialog Box Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="76ea9-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="76ea9-105">In this section</span></span>

-   [<span data-ttu-id="76ea9-106">*CCHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-106">*CCHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcchookproc)
-   [<span data-ttu-id="76ea9-107">*CFHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-107">*CFHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpcfhookproc)
-   <span data-ttu-id="76ea9-108">[**Les ChooseColor.**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76ea9-108">[**ChooseColor**](/previous-versions/windows/desktop/legacy/ms646912(v=vs.85))</span></span>
-   [<span data-ttu-id="76ea9-109">**ChooseFont**</span><span class="sxs-lookup"><span data-stu-id="76ea9-109">**ChooseFont**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="76ea9-110">**CommDlgExtendedError**</span><span class="sxs-lookup"><span data-stu-id="76ea9-110">**CommDlgExtendedError**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-commdlgextendederror)
-   [<span data-ttu-id="76ea9-111">**FindText**</span><span class="sxs-lookup"><span data-stu-id="76ea9-111">**FindText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-findtexta)
-   [<span data-ttu-id="76ea9-112">*FRHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-112">*FRHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpfrhookproc)
-   [<span data-ttu-id="76ea9-113">**GetFileTitle**</span><span class="sxs-lookup"><span data-stu-id="76ea9-113">**GetFileTitle**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getfiletitlea)
-   [<span data-ttu-id="76ea9-114">**GetOpenFileName**</span><span class="sxs-lookup"><span data-stu-id="76ea9-114">**GetOpenFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getopenfilenamea)
-   [<span data-ttu-id="76ea9-115">**GetSaveFileName**</span><span class="sxs-lookup"><span data-stu-id="76ea9-115">**GetSaveFileName**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-getsavefilenamea)
-   [<span data-ttu-id="76ea9-116">*OFNHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-116">*OFNHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpofnhookproc)
-   <span data-ttu-id="76ea9-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76ea9-117">[*OFNHookProcOldStyle*](/previous-versions/windows/desktop/legacy/ms646932(v=vs.85))</span></span>
-   [<span data-ttu-id="76ea9-118">**PagePaintHook**</span><span class="sxs-lookup"><span data-stu-id="76ea9-118">**PagePaintHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagepainthook)
-   <span data-ttu-id="76ea9-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76ea9-119">[**PageSetupDlg**](/previous-versions/windows/desktop/legacy/ms646937(v=vs.85))</span></span>
-   [<span data-ttu-id="76ea9-120">**PageSetupHook**</span><span class="sxs-lookup"><span data-stu-id="76ea9-120">**PageSetupHook**</span></span>](/windows/win32/api/commdlg/nc-commdlg-lppagesetuphook)
-   <span data-ttu-id="76ea9-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76ea9-121">[**PrintDlg**](/previous-versions/windows/desktop/legacy/ms646940(v=vs.85))</span></span>
-   <span data-ttu-id="76ea9-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76ea9-122">[**PrintDlgEx**](/previous-versions/windows/desktop/legacy/ms646942(v=vs.85))</span></span>
-   [<span data-ttu-id="76ea9-123">*PrintHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-123">*PrintHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpprinthookproc)
-   [<span data-ttu-id="76ea9-124">**Frappe**</span><span class="sxs-lookup"><span data-stu-id="76ea9-124">**ReplaceText**</span></span>](/windows/desktop/api/Commdlg/nf-commdlg-replacetexta)
-   [<span data-ttu-id="76ea9-125">*SetupHookProc*</span><span class="sxs-lookup"><span data-stu-id="76ea9-125">*SetupHookProc*</span></span>](/windows/win32/api/commdlg/nc-commdlg-lpsetuphookproc)

 

 
