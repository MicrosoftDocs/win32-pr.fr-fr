---
description: La fonction GetSpoolFileHandle récupère un handle pour le fichier de mise en file d’attente associé au travail actuellement soumis par l’application.
ms.assetid: df6f28b3-66a6-4fb7-bdde-40cd7d934c5f
title: GetSpoolFileHandle, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetSpoolFileHandle
- GetSpoolFileHandleA
- GetSpoolFileHandleW
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9ac4dd4b0db9a59cc0140872ff04f89adaf8b6c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035224"
---
# <a name="getspoolfilehandle-function"></a><span data-ttu-id="d744d-103">GetSpoolFileHandle fonction)</span><span class="sxs-lookup"><span data-stu-id="d744d-103">GetSpoolFileHandle function</span></span>

<span data-ttu-id="d744d-104">La fonction **GetSpoolFileHandle** récupère un handle pour le fichier de mise en file d’attente associé au travail actuellement soumis par l’application.</span><span class="sxs-lookup"><span data-stu-id="d744d-104">The **GetSpoolFileHandle** function retrieves a handle for the spool file associated with the job currently submitted by the application.</span></span>

## <a name="syntax"></a><span data-ttu-id="d744d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d744d-105">Syntax</span></span>


```C++
HANDLE GetSpoolFileHandle(
  _In_ HANDLE hPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="d744d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d744d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d744d-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d744d-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d744d-108">Handle vers l’imprimante sur laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="d744d-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="d744d-109">Il doit s’agir du même handle que celui utilisé pour envoyer le travail.</span><span class="sxs-lookup"><span data-stu-id="d744d-109">This should be the same handle that was used to submit the job.</span></span> <span data-ttu-id="d744d-110">(Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.)</span><span class="sxs-lookup"><span data-stu-id="d744d-110">(Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d744d-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d744d-111">Return value</span></span>

<span data-ttu-id="d744d-112">Si la fonction est réussie, elle retourne un handle au fichier de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="d744d-112">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="d744d-113">Si la fonction échoue, elle retourne **une \_ \_ valeur de handle non valide**.</span><span class="sxs-lookup"><span data-stu-id="d744d-113">If the function fails, it returns **INVALID\_HANDLE\_VALUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d744d-114">Notes</span><span class="sxs-lookup"><span data-stu-id="d744d-114">Remarks</span></span>

<span data-ttu-id="d744d-115">Avec le descripteur du fichier de mise en file d’attente, votre application peut écrire dans le fichier de mise en file d’attente avec des appels à [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) suivis de [**CommitSpoolData**](commitspooldata.md).</span><span class="sxs-lookup"><span data-stu-id="d744d-115">With the handle to the spool file, your application can write to the spool file with calls to [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile) followed by [**CommitSpoolData**](commitspooldata.md).</span></span>

<span data-ttu-id="d744d-116">Votre application ne doit pas appeler [**ClosePrinter**](closeprinter.md) sur *hPrinter* tant qu’elle n’a pas accédé au fichier spool pour la dernière fois.</span><span class="sxs-lookup"><span data-stu-id="d744d-116">Your application must not call [**ClosePrinter**](closeprinter.md) on *hPrinter* until after it has accessed the spool file for the last time.</span></span> <span data-ttu-id="d744d-117">Ensuite, il doit appeler [**CloseSpoolFileHandle**](closespoolfilehandle.md) suivi de **ClosePrinter**.</span><span class="sxs-lookup"><span data-stu-id="d744d-117">Then it should call [**CloseSpoolFileHandle**](closespoolfilehandle.md) followed by **ClosePrinter**.</span></span> <span data-ttu-id="d744d-118">Toute tentative d’accès au descripteur de fichier de mise en file d’attente après la fermeture du *hPrinter* d’origine échoue, même si le descripteur de fichier lui-même n’a pas été fermé.</span><span class="sxs-lookup"><span data-stu-id="d744d-118">Attempts to access the spool file handle after the original *hPrinter* has been closed will fail even if the file handle itself has not been closed.</span></span> <span data-ttu-id="d744d-119">**CloseSpoolFileHandle** échouera même si **ClosePrinter** est appelé en premier.</span><span class="sxs-lookup"><span data-stu-id="d744d-119">**CloseSpoolFileHandle** will itself fail if **ClosePrinter** is called first.</span></span>

<span data-ttu-id="d744d-120">Cette fonction échoue si elle est appelée avant la fin de la mise en attente du travail d’impression.</span><span class="sxs-lookup"><span data-stu-id="d744d-120">This function will fail if it is called before the print job has finished spooling.</span></span>

## <a name="requirements"></a><span data-ttu-id="d744d-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d744d-121">Requirements</span></span>



| <span data-ttu-id="d744d-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d744d-122">Requirement</span></span> | <span data-ttu-id="d744d-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d744d-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d744d-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d744d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d744d-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d744d-125">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="d744d-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d744d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d744d-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d744d-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d744d-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="d744d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="d744d-129"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d744d-129"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d744d-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d744d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="d744d-131"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d744d-131"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d744d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d744d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d744d-133"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d744d-133"><dt>WinSpool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d744d-134">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d744d-134">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d744d-135">**GetSpoolFileHandleW** (Unicode) et **GetSpoolFileHandleA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d744d-135">**GetSpoolFileHandleW** (Unicode) and **GetSpoolFileHandleA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="d744d-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d744d-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d744d-137">Impression</span><span class="sxs-lookup"><span data-stu-id="d744d-137">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d744d-138">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d744d-138">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d744d-139">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d744d-139">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d744d-140">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="d744d-140">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="d744d-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="d744d-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="d744d-142">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="d744d-142">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="d744d-143">**CommitSpoolData**</span><span class="sxs-lookup"><span data-stu-id="d744d-143">**CommitSpoolData**</span></span>](commitspooldata.md)
</dt> </dl>

 

