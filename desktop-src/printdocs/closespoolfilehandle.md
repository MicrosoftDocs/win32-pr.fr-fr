---
description: La fonction CloseSpoolFileHandle ferme un handle vers un fichier de mise en file d’attente associé au travail d’impression actuellement soumis par l’application.
ms.assetid: e2c0e68f-b72e-4a97-ba18-8943bc5789c1
title: CloseSpoolFileHandle, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CloseSpoolFileHandle
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: c808bddde5b9b4e4a87a8608c1efb3999ce1f391
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544829"
---
# <a name="closespoolfilehandle-function"></a><span data-ttu-id="1186d-103">CloseSpoolFileHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="1186d-103">CloseSpoolFileHandle function</span></span>

<span data-ttu-id="1186d-104">La fonction **CloseSpoolFileHandle** ferme un handle vers un fichier de mise en file d’attente associé au travail d’impression actuellement soumis par l’application.</span><span class="sxs-lookup"><span data-stu-id="1186d-104">The **CloseSpoolFileHandle** function closes a handle to a spool file associated with the print job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="1186d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1186d-105">Syntax</span></span>


```C++
BOOL CloseSpoolFileHandle(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile
);
```



## <a name="parameters"></a><span data-ttu-id="1186d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1186d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1186d-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1186d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1186d-108">Handle vers l’imprimante sur laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="1186d-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="1186d-109">Il doit s’agir du même handle que celui utilisé pour obtenir *hSpoolFile* avec [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="1186d-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="1186d-110">*hSpoolFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1186d-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1186d-111">Handle du fichier spouleur en cours de fermeture.</span><span class="sxs-lookup"><span data-stu-id="1186d-111">A handle to the spool file being closed.</span></span> <span data-ttu-id="1186d-112">Si [**CommitSpoolData**](commitspooldata.md) n’a pas été appelé depuis l’appel de [**GetSpoolFileHandle**](getspoolfilehandle.md) , il doit s’agir du même handle que celui retourné par **GetSpoolFileHandle**.</span><span class="sxs-lookup"><span data-stu-id="1186d-112">If [**CommitSpoolData**](commitspooldata.md) has not been called since [**GetSpoolFileHandle**](getspoolfilehandle.md) was called, then this should be the same handle that was returned by **GetSpoolFileHandle**.</span></span> <span data-ttu-id="1186d-113">Dans le cas contraire, il doit s’agir du handle qui a été retourné par l’appel le plus récent à **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="1186d-113">Otherwise, it should be the handle that was returned by the most recent call to **CommitSpoolData**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1186d-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1186d-114">Return value</span></span>

<span data-ttu-id="1186d-115">**True**, si elle est réussie, **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="1186d-115">**TRUE**, if it succeeds, **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="1186d-116">Notes</span><span class="sxs-lookup"><span data-stu-id="1186d-116">Remarks</span></span>

<span data-ttu-id="1186d-117">Votre application ne doit pas appeler [**ClosePrinter**](closeprinter.md) sur *hPrinter* tant qu’elle n’a pas accédé au fichier spool pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="1186d-117">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="1186d-118">Ensuite, il doit appeler **CloseSpoolFileHandle** suivi de **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="1186d-118">Then it should call **CloseSpoolFileHandle** followed by **ClosePrinter**.</span></span> <span data-ttu-id="1186d-119">Toute tentative d’accès au descripteur de fichier de mise en file d’attente après la fermeture du *hPrinter* d’origine échoue, même si le descripteur de fichier lui-même n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="1186d-119">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="1186d-120">**CloseSpoolFileHandle** échoue si **ClosePrinter** est appelé en premier.</span><span class="sxs-lookup"><span data-stu-id="1186d-120">**CloseSpoolFileHandle** will fail if **ClosePrinter** is called first.</span></span>

## <a name="requirements"></a><span data-ttu-id="1186d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1186d-121">Requirements</span></span>



| <span data-ttu-id="1186d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1186d-122">Requirement</span></span> | <span data-ttu-id="1186d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="1186d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1186d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1186d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="1186d-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1186d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="1186d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1186d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="1186d-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1186d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="1186d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="1186d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="1186d-129"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1186d-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="1186d-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1186d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="1186d-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1186d-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="1186d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="1186d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1186d-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="1186d-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="1186d-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1186d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1186d-135">Impression</span><span class="sxs-lookup"><span data-stu-id="1186d-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="1186d-136">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="1186d-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="1186d-137">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="1186d-137">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="1186d-138">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="1186d-138">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> </dl>

 

 




