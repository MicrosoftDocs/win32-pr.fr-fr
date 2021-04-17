---
title: READERMODEINFO, structure
description: Contient les informations requises pour initialiser la fonction DoReaderMode.
ms.assetid: 7b9c73bc-b093-4592-befd-67508fb86fe0
keywords:
- Contrôles Windows de la structure READERMODEINFO
- Contrôles Windows du pointeur de structure PREADERMODEINFO
topic_type:
- apiref
api_name:
- READERMODEINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2dacf0fc59ef62447ca12b7a470689e13967d687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466066"
---
# <a name="readermodeinfo-structure"></a><span data-ttu-id="76a27-105">READERMODEINFO, structure</span><span class="sxs-lookup"><span data-stu-id="76a27-105">READERMODEINFO structure</span></span>

<span data-ttu-id="76a27-106">\[**READERMODEINFO** est pris en charge par Windows XP avec Service Pack 2 (SP2).</span><span class="sxs-lookup"><span data-stu-id="76a27-106">\[**READERMODEINFO** is supported through Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="76a27-107">Il est possible qu’il ne soit pas pris en charge dans les versions ultérieures.\]</span><span class="sxs-lookup"><span data-stu-id="76a27-107">It might be unsupported in subsequent versions.\]</span></span>

<span data-ttu-id="76a27-108">Contient les informations requises pour initialiser la fonction [**DoReaderMode**](doreadermode.md) .</span><span class="sxs-lookup"><span data-stu-id="76a27-108">Contains information required to initialize the [**DoReaderMode**](doreadermode.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a27-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="76a27-109">Syntax</span></span>


```C++
typedef struct tagReaderModeInfo {
  UINT                       cbSize;
  HWND                       hwnd;
  DWORD                      fFlags;
  LPRECT                     prc;
  PFNREADERSCROLL            pfnScroll;
  PFNREADERTRANSLATEDISPATCH fFlags;
  LPARAM                     lParam;
} READERMODEINFO, *PREADERMODEINFO;
```



## <a name="members"></a><span data-ttu-id="76a27-110">Membres</span><span class="sxs-lookup"><span data-stu-id="76a27-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="76a27-111">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="76a27-111">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-112">Type : **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76a27-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-113">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76a27-113">Required.</span></span> <span data-ttu-id="76a27-114">Taille de la structure en octets.</span><span class="sxs-lookup"><span data-stu-id="76a27-114">The size of the structure, in bytes.</span></span> <span data-ttu-id="76a27-115">Affectez à ce paramètre la valeur **sizeof (READERMODE)** avant d’appeler [**DoReaderMode**](doreadermode.md).</span><span class="sxs-lookup"><span data-stu-id="76a27-115">Set this parameter to **sizeof(READERMODE)** before you call [**DoReaderMode**](doreadermode.md).</span></span>

</dd> <dt>

<span data-ttu-id="76a27-116">**HWND**</span><span class="sxs-lookup"><span data-stu-id="76a27-116">**hwnd**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-117">Type : **[ **HWND**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76a27-117">Type: **[**HWND**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-118">Obligatoire.</span><span class="sxs-lookup"><span data-stu-id="76a27-118">Required.</span></span> <span data-ttu-id="76a27-119">Handle de la fenêtre à utiliser pour le mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="76a27-119">The handle of the window to be used for reader mode.</span></span>

</dd> <dt>

<span data-ttu-id="76a27-120">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="76a27-120">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-121">Type : **[ **DWORD**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76a27-121">Type: **[**DWORD**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-122">Indicateurs personnalisant les fonctionnalités de la fenêtre du mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="76a27-122">Flags customizing the functionality of the reader mode window.</span></span> <span data-ttu-id="76a27-123">Ce paramètre peut avoir la valeur 0 ; Sinon, une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="76a27-123">This parameter can be 0; otherwise, one or more of the following values.</span></span>



| <span data-ttu-id="76a27-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a27-124">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="76a27-125">Signification</span><span class="sxs-lookup"><span data-stu-id="76a27-125">Meaning</span></span>                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RMF_ZEROCURSOR"></span><span id="rmf_zerocursor"></span><dl> <span data-ttu-id="76a27-126"><dt>**RMF \_ ZEROCURSOR**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="76a27-126"><dt>**RMF\_ZEROCURSOR**</dt> <dt>0x01</dt></span></span> </dl>             | <span data-ttu-id="76a27-127">Définit le curseur au centre de la zone spécifiée en **PRC**.</span><span class="sxs-lookup"><span data-stu-id="76a27-127">Sets the cursor in the center of the area specified in **prc**.</span></span> <span data-ttu-id="76a27-128">Si cet indicateur n’est pas spécifié, la position du curseur reste inchangée.</span><span class="sxs-lookup"><span data-stu-id="76a27-128">If this flag is not specified, the cursor position remains unchanged.</span></span><br/> |
| <span id="RMF_VERTICALONLY"></span><span id="rmf_verticalonly"></span><dl> <span data-ttu-id="76a27-129"><dt>**RMF \_ VERTICALONLY**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="76a27-129"><dt>**RMF\_VERTICALONLY**</dt> <dt>0x02</dt></span></span> </dl>       | <span data-ttu-id="76a27-130">Autorise uniquement le défilement vertical.</span><span class="sxs-lookup"><span data-stu-id="76a27-130">Allows only vertical scrolling.</span></span><br/>                                                                                                       |
| <span id="RMF_HORIZONTALONLY"></span><span id="rmf_horizontalonly"></span><dl> <span data-ttu-id="76a27-131"><dt>**RMF \_ HORIZONTALONLY**</dt> <dt>0x04</dt></span><span class="sxs-lookup"><span data-stu-id="76a27-131"><dt>**RMF\_HORIZONTALONLY**</dt> <dt>0x04</dt></span></span> </dl> | <span data-ttu-id="76a27-132">Autorise uniquement le défilement horizontal.</span><span class="sxs-lookup"><span data-stu-id="76a27-132">Allows only horizontal scrolling.</span></span><br/>                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="76a27-133">**République**</span><span class="sxs-lookup"><span data-stu-id="76a27-133">**prc**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-134">Type : **LPRECT**</span><span class="sxs-lookup"><span data-stu-id="76a27-134">Type: **LPRECT**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-135">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) qui spécifie la zone de défilement dans la fenêtre du mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="76a27-135">A pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure that specifies the scrolling area in the reader mode window.</span></span> <span data-ttu-id="76a27-136">Si ce membre a la **valeur null**, la fenêtre entière est utilisée comme zone de défilement.</span><span class="sxs-lookup"><span data-stu-id="76a27-136">If this member is **NULL**, then the entire window is used as the scrolling area.</span></span>

</dd> <dt>

<span data-ttu-id="76a27-137">**pfnScroll**</span><span class="sxs-lookup"><span data-stu-id="76a27-137">**pfnScroll**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-138">Type : **PFNREADERSCROLL**</span><span class="sxs-lookup"><span data-stu-id="76a27-138">Type: **PFNREADERSCROLL**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-139">Pointeur vers une fonction de rappel [*ReaderScroll*](readerscroll.md) définie par l’application, utilisée pour notifier l’application que la fenêtre doit faire défiler dans une direction particulière.</span><span class="sxs-lookup"><span data-stu-id="76a27-139">A pointer to an application-defined [*ReaderScroll*](readerscroll.md) callback function used to notify the application that the window needs to be scrolled in a particular direction.</span></span>

</dd> <dt>

<span data-ttu-id="76a27-140">**fFlags**</span><span class="sxs-lookup"><span data-stu-id="76a27-140">**fFlags**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-141">Type : **PFNREADERTRANSLATEDISPATCH**</span><span class="sxs-lookup"><span data-stu-id="76a27-141">Type: **PFNREADERTRANSLATEDISPATCH**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-142">Pointeur vers une fonction de rappel [*TranslateDispatch*](translatedispatch.md) définie par l’application, utilisée pour obtenir la première notification de tous les messages envoyés à la fenêtre du mode lecteur.</span><span class="sxs-lookup"><span data-stu-id="76a27-142">A pointer to an application-defined [*TranslateDispatch*](translatedispatch.md) callback function used to get first notification of any messages sent to the reader mode window.</span></span>

</dd> <dt>

<span data-ttu-id="76a27-143">**lParam**</span><span class="sxs-lookup"><span data-stu-id="76a27-143">**lParam**</span></span>
</dt> <dd>

<span data-ttu-id="76a27-144">Type : **[ **lParam**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="76a27-144">Type: **[**LPARAM**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="76a27-145">Informations supplémentaires requises par l’application, lues par l’appelant dans la fonction de rappel [*ReaderScroll*](readerscroll.md) .</span><span class="sxs-lookup"><span data-stu-id="76a27-145">Additional information as needed by the application, read by the caller in the [*ReaderScroll*](readerscroll.md) callback function.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="76a27-146">Notes</span><span class="sxs-lookup"><span data-stu-id="76a27-146">Remarks</span></span>

<span data-ttu-id="76a27-147">Cette structure n’est pas déclarée dans un en-tête public.</span><span class="sxs-lookup"><span data-stu-id="76a27-147">This structure is not declared in any public header.</span></span> <span data-ttu-id="76a27-148">Pour l’utiliser, vous devez inclure la déclaration ci-dessus dans votre propre en-tête.</span><span class="sxs-lookup"><span data-stu-id="76a27-148">To use it, you must include the declaration shown above in your own header.</span></span>

## <a name="requirements"></a><span data-ttu-id="76a27-149">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="76a27-149">Requirements</span></span>



| <span data-ttu-id="76a27-150">Condition requise</span><span class="sxs-lookup"><span data-stu-id="76a27-150">Requirement</span></span> | <span data-ttu-id="76a27-151">Valeur</span><span class="sxs-lookup"><span data-stu-id="76a27-151">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="76a27-152">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a27-152">Minimum supported client</span></span><br/> | <span data-ttu-id="76a27-153">Windows Vista, applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a27-153">Windows Vista, Windows Vista \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="76a27-154">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="76a27-154">Minimum supported server</span></span><br/> | <span data-ttu-id="76a27-155">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="76a27-155">Windows Server 2003 \[desktop apps only\]</span></span><br/>          |



 

