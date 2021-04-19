---
description: Supprime un package de pilotes d’imprimante du magasin de pilotes.
ms.assetid: a43a94d1-097e-457c-bce9-d4c434ecfa93
title: DeletePrinterDriverPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDriverPackage
- DeletePrinterDriverPackageA
- DeletePrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 54d1cda53795f4feab60e397ce7e38402f22374f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531924"
---
# <a name="deleteprinterdriverpackage-function"></a><span data-ttu-id="4420e-103">DeletePrinterDriverPackage fonction)</span><span class="sxs-lookup"><span data-stu-id="4420e-103">DeletePrinterDriverPackage function</span></span>

<span data-ttu-id="4420e-104">Supprime un package de pilotes d’imprimante du magasin de pilotes.</span><span class="sxs-lookup"><span data-stu-id="4420e-104">Deletes a printer driver package from the driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="4420e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4420e-105">Syntax</span></span>


```C++
HRESULT DeletePrinterDriverPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszEnvironment
);
```



## <a name="parameters"></a><span data-ttu-id="4420e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4420e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4420e-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4420e-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4420e-108">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression à partir duquel le package de pilotes est supprimé.</span><span class="sxs-lookup"><span data-stu-id="4420e-108">A pointer to a constant, null-terminated string that specifies the name of the print server from which the driver package is being deleted.</span></span> <span data-ttu-id="4420e-109">Une valeur de pointeur **null** signifie l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4420e-109">A **NULL** pointer value means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="4420e-110">*pszInfPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4420e-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4420e-111">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès au \* fichier. inf du pilote.</span><span class="sxs-lookup"><span data-stu-id="4420e-111">A pointer to a constant, null-terminated string that specifies the path to the driver's \*.inf file.</span></span>

</dd> <dt>

<span data-ttu-id="4420e-112">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4420e-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4420e-113">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="4420e-113">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="4420e-114">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4420e-114">This can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4420e-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4420e-115">Return value</span></span>

<span data-ttu-id="4420e-116">\_OK si l’opération a échoué.</span><span class="sxs-lookup"><span data-stu-id="4420e-116">S\_OK, if the operation succeeds.</span></span>

<span data-ttu-id="4420e-117">E \_ ACCESSDENIED, si le package a été fourni avec Windows.</span><span class="sxs-lookup"><span data-stu-id="4420e-117">E\_ACCESSDENIED, if the package was shipped with Windows.</span></span>

<span data-ttu-id="4420e-118">\_Code HRESULT (erreur \_ \_ d’impression \_ \_ du package de pilotes en cours d' \_ utilisation), si le package est utilisé.</span><span class="sxs-lookup"><span data-stu-id="4420e-118">HRESULT\_CODE(ERROR\_PRINT\_DRIVER\_PACKAGE\_IN\_USE), if the package is being used.</span></span>

<span data-ttu-id="4420e-119">Sinon, **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4420e-119">Otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="4420e-120">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="4420e-120">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4420e-121">Notes</span><span class="sxs-lookup"><span data-stu-id="4420e-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4420e-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4420e-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4420e-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="4420e-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4420e-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="4420e-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4420e-125">Le magasin de pilotes correspond généralement à% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="4420e-125">The driver store is typically %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="4420e-126">Impossible de supprimer un package de pilotes fourni avec Windows avec cette fonction.</span><span class="sxs-lookup"><span data-stu-id="4420e-126">A driver package that shipped with Windows cannot be removed with this function.</span></span>

<span data-ttu-id="4420e-127">L’utilisateur doit disposer de privilèges d’administration d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="4420e-127">The user must have printer administration privileges.</span></span>

## <a name="requirements"></a><span data-ttu-id="4420e-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4420e-128">Requirements</span></span>



| <span data-ttu-id="4420e-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4420e-129">Requirement</span></span> | <span data-ttu-id="4420e-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="4420e-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4420e-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4420e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4420e-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4420e-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4420e-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4420e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4420e-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4420e-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4420e-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="4420e-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4420e-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4420e-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4420e-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4420e-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="4420e-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4420e-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4420e-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4420e-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4420e-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4420e-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4420e-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4420e-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4420e-142">**DeletePrinterDriverPackageW** (Unicode) et **DeletePrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4420e-142">**DeletePrinterDriverPackageW** (Unicode) and **DeletePrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4420e-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4420e-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4420e-144">Impression</span><span class="sxs-lookup"><span data-stu-id="4420e-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4420e-145">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4420e-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

