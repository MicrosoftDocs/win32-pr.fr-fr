---
description: La fonction CommitSpoolData informe le spouleur d’impression qu’une quantité de données spécifiée a été écrite dans un fichier spouleur spécifié et qu’elle est prête à être rendue.
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: CommitSpoolData, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864761"
---
# <a name="commitspooldata-function"></a><span data-ttu-id="39780-103">CommitSpoolData fonction)</span><span class="sxs-lookup"><span data-stu-id="39780-103">CommitSpoolData function</span></span>

<span data-ttu-id="39780-104">La fonction **CommitSpoolData** informe le spouleur d’impression qu’une quantité de données spécifiée a été écrite dans un fichier spouleur spécifié et qu’elle est prête à être rendue.</span><span class="sxs-lookup"><span data-stu-id="39780-104">The **CommitSpoolData** function notifies the print spooler that a specified amount of data has been written to a specified spool file and is ready to be rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="39780-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39780-105">Syntax</span></span>


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a><span data-ttu-id="39780-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39780-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39780-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39780-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39780-108">Handle vers l’imprimante sur laquelle le travail a été soumis.</span><span class="sxs-lookup"><span data-stu-id="39780-108">A handle to the printer to which the job was submitted.</span></span> <span data-ttu-id="39780-109">Il doit s’agir du même handle que celui utilisé pour obtenir *hSpoolFile* avec [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="39780-109">This should be the same handle that was used to obtain *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="39780-110">*hSpoolFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="39780-110">*hSpoolFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39780-111">Handle du fichier de mise en attente en cours de modification.</span><span class="sxs-lookup"><span data-stu-id="39780-111">A handle to the spool file being changed.</span></span> <span data-ttu-id="39780-112">Lors du premier appel de **CommitSpoolData**, il doit s’agir du même handle que celui retourné par [**GetSpoolFileHandle**](getspoolfilehandle.md).</span><span class="sxs-lookup"><span data-stu-id="39780-112">On the first call of **CommitSpoolData**, this should be the same handle that was returned by [**GetSpoolFileHandle**](getspoolfilehandle.md).</span></span> <span data-ttu-id="39780-113">Les appels suivants à **CommitSpoolData** doivent passer le handle retourné par l’appel précédent.</span><span class="sxs-lookup"><span data-stu-id="39780-113">Subsequent calls to **CommitSpoolData** should pass the handle returned by the preceding call.</span></span> <span data-ttu-id="39780-114">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="39780-114">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="39780-115">*cbCommit*</span><span class="sxs-lookup"><span data-stu-id="39780-115">*cbCommit*</span></span> 
</dt> <dd>

<span data-ttu-id="39780-116">Nombre d’octets validés dans le spouleur d’impression.</span><span class="sxs-lookup"><span data-stu-id="39780-116">The number of bytes committed to the print spooler.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39780-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="39780-117">Return value</span></span>

<span data-ttu-id="39780-118">Si la fonction est réussie, elle retourne un handle au fichier de mise en file d’attente.</span><span class="sxs-lookup"><span data-stu-id="39780-118">If the function succeeds, it returns a handle to the spool file.</span></span>

<span data-ttu-id="39780-119">Si la fonction échoue, elle retourne une \_ valeur de handle non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="39780-119">If the function fails, it returns INVALID\_HANDLE\_VALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="39780-120">Notes</span><span class="sxs-lookup"><span data-stu-id="39780-120">Remarks</span></span>

<span data-ttu-id="39780-121">Les applications qui envoient un travail d’impression de spouleur peuvent appeler [**GetSpoolFileHandle**](getspoolfilehandle.md) , puis écrire directement les données dans le handle de fichier de mise en file d’attente en appelant [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span><span class="sxs-lookup"><span data-stu-id="39780-121">Applications submitting a spooler print job can call [**GetSpoolFileHandle**](getspoolfilehandle.md) and then directly write data to the spool file handle by calling [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile).</span></span> <span data-ttu-id="39780-122">Pour informer le spouleur d’impression que le fichier contient des données qui sont prêtes à être rendues, l’application doit appeler **CommitSpoolData** et fournir le nombre d’octets disponibles.</span><span class="sxs-lookup"><span data-stu-id="39780-122">To notify the print spooler that the file contains data which is ready to be rendered, the application must call **CommitSpoolData** and provide the number of available bytes.</span></span>

<span data-ttu-id="39780-123">Si **CommitSpoolData** est appelée plusieurs fois, chaque appel doit utiliser le descripteur de fichier de mise en file d’attente retourné par l’appel précédent.</span><span class="sxs-lookup"><span data-stu-id="39780-123">If **CommitSpoolData** is called multiple times, each call must use the spool file handle returned by the previous call.</span></span> <span data-ttu-id="39780-124">Quand plus aucune donnée n’est écrite dans le fichier de mise en file d’attente, [**CloseSpoolFileHandle**](closespoolfilehandle.md) doit être appelé pour le handle de fichier retourné par le dernier appel à **CommitSpoolData**.</span><span class="sxs-lookup"><span data-stu-id="39780-124">When no more data will be written to the spool file, [**CloseSpoolFileHandle**](closespoolfilehandle.md) should be called for the file handle returned by the last call to **CommitSpoolData**.</span></span>

<span data-ttu-id="39780-125">Avant d’appeler **CommitSpoolData**, les applications doivent définir le pointeur de fichier à la position qu’il avait avant d’écrire des données dans le fichier.</span><span class="sxs-lookup"><span data-stu-id="39780-125">Before calling **CommitSpoolData**, applications must set the file pointer to the position it had before it wrote data to the file.</span></span> <span data-ttu-id="39780-126">Dans le processus de rendu des données dans le fichier du spouleur, le spouleur d’impression déplace le pointeur de fichier spool *cbCommit* octets de la valeur actuelle du pointeur de fichier.</span><span class="sxs-lookup"><span data-stu-id="39780-126">In the process of rendering the data in the spooler file, the print spooler will move the spool file pointer *cbCommit* bytes from the current value of file pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="39780-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="39780-127">Requirements</span></span>



| <span data-ttu-id="39780-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="39780-128">Requirement</span></span> | <span data-ttu-id="39780-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="39780-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="39780-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39780-130">Minimum supported client</span></span><br/> | <span data-ttu-id="39780-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39780-131">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="39780-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="39780-132">Minimum supported server</span></span><br/> | <span data-ttu-id="39780-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="39780-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="39780-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="39780-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="39780-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="39780-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="39780-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="39780-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="39780-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="39780-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="39780-138">DLL</span><span class="sxs-lookup"><span data-stu-id="39780-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39780-139"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="39780-139"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="39780-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="39780-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39780-141">Impression</span><span class="sxs-lookup"><span data-stu-id="39780-141">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="39780-142">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="39780-142">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="39780-143">**GetSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="39780-143">**GetSpoolFileHandle**</span></span>](getspoolfilehandle.md)
</dt> <dt>

[<span data-ttu-id="39780-144">**CloseSpoolFileHandle**</span><span class="sxs-lookup"><span data-stu-id="39780-144">**CloseSpoolFileHandle**</span></span>](closespoolfilehandle.md)
</dt> </dl>

 

