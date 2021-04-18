---
description: La fonction AddPrintProcessor installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.
ms.assetid: 99899cee-f74d-4405-8ea5-616e3769aba9
title: AddPrintProcessor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrintProcessor
- AddPrintProcessorA
- AddPrintProcessorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 871df9fee211ae13e1552978ce651840d7f542f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536602"
---
# <a name="addprintprocessor-function"></a><span data-ttu-id="a2179-103">AddPrintProcessor fonction)</span><span class="sxs-lookup"><span data-stu-id="a2179-103">AddPrintProcessor function</span></span>

<span data-ttu-id="a2179-104">La fonction **AddPrintProcessor** installe un processeur d’impression sur le serveur spécifié et ajoute le nom du processeur d’impression à la liste des processeurs d’impression pris en charge.</span><span class="sxs-lookup"><span data-stu-id="a2179-104">The **AddPrintProcessor** function installs a print processor on the specified server and adds the print-processor name to the list of supported print processors.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2179-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2179-105">Syntax</span></span>


```C++
BOOL AddPrintProcessor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPathName,
  _In_ LPTSTR pPrintProcessorName
);
```



## <a name="parameters"></a><span data-ttu-id="a2179-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2179-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2179-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2179-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2179-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le processeur d’impression doit être installé.</span><span class="sxs-lookup"><span data-stu-id="a2179-108">A pointer to a null-terminated string that specifies the name of the server on which the print processor should be installed.</span></span> <span data-ttu-id="a2179-109">Si ce paramètre a la **valeur null**, le processeur d’impression est installé localement.</span><span class="sxs-lookup"><span data-stu-id="a2179-109">If this parameter is **NULL**, the print processor is installed locally.</span></span>

</dd> <dt>

<span data-ttu-id="a2179-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2179-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2179-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="a2179-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="a2179-112">Si ce paramètre a la **valeur null**, l’environnement actuel de l’appelant/client (pas du serveur/de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="a2179-112">If this parameter is **NULL**, the current environment of the caller/client (not of the destination/server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="a2179-113">*pPathName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2179-113">*pPathName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2179-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fichier qui contient le processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="a2179-114">A pointer to a null-terminated string that specifies the name of the file that contains the print processor.</span></span> <span data-ttu-id="a2179-115">Ce fichier doit se trouver dans le répertoire du processeur d’impression système.</span><span class="sxs-lookup"><span data-stu-id="a2179-115">This file must be in the system print-processor directory.</span></span>

</dd> <dt>

<span data-ttu-id="a2179-116">*pPrintProcessorName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2179-116">*pPrintProcessorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2179-117">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du processeur d’impression.</span><span class="sxs-lookup"><span data-stu-id="a2179-117">A pointer to a null-terminated string that specifies the name of the print processor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2179-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2179-118">Return value</span></span>

<span data-ttu-id="a2179-119">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a2179-119">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="a2179-120">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2179-120">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="a2179-121">Notes</span><span class="sxs-lookup"><span data-stu-id="a2179-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a2179-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="a2179-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="a2179-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="a2179-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="a2179-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="a2179-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="a2179-125">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="a2179-125">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="a2179-126">Avant d’appeler la fonction **AddPrintProcessor** , une application doit vérifier que le fichier contenant le processeur d’impression est stocké dans le répertoire du processeur d’impression système.</span><span class="sxs-lookup"><span data-stu-id="a2179-126">Before calling the **AddPrintProcessor** function, an application should verify that the file containing the print processor is stored in the system print-processor directory.</span></span> <span data-ttu-id="a2179-127">Une application peut récupérer le nom du répertoire du processeur d’impression système en appelant la fonction [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="a2179-127">An application can retrieve the name of the system print-processor directory by calling the [**GetPrintProcessorDirectory**](getprintprocessordirectory.md) function.</span></span>

<span data-ttu-id="a2179-128">Une application peut déterminer le nom de processeurs d’impression existants en appelant la fonction [**EnumPrintProcessors**](enumprintprocessors.md) .</span><span class="sxs-lookup"><span data-stu-id="a2179-128">An application can determine the name of existing print processors by calling the [**EnumPrintProcessors**](enumprintprocessors.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2179-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2179-129">Requirements</span></span>



| <span data-ttu-id="a2179-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2179-130">Requirement</span></span> | <span data-ttu-id="a2179-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2179-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2179-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2179-132">Minimum supported client</span></span><br/> | <span data-ttu-id="a2179-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2179-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a2179-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2179-134">Minimum supported server</span></span><br/> | <span data-ttu-id="a2179-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2179-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a2179-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2179-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2179-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2179-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="a2179-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a2179-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="a2179-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a2179-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="a2179-140">DLL</span><span class="sxs-lookup"><span data-stu-id="a2179-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2179-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="a2179-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="a2179-142">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="a2179-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="a2179-143">**AddPrintProcessorW** (Unicode) et **AddPrintProcessorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="a2179-143">**AddPrintProcessorW** (Unicode) and **AddPrintProcessorA** (ANSI)</span></span><br/>                             |



## <a name="see-also"></a><span data-ttu-id="a2179-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2179-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a2179-145">Impression</span><span class="sxs-lookup"><span data-stu-id="a2179-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="a2179-146">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="a2179-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="a2179-147">**EnumPrintProcessors**</span><span class="sxs-lookup"><span data-stu-id="a2179-147">**EnumPrintProcessors**</span></span>](enumprintprocessors.md)
</dt> <dt>

[<span data-ttu-id="a2179-148">**GetPrintProcessorDirectory**</span><span class="sxs-lookup"><span data-stu-id="a2179-148">**GetPrintProcessorDirectory**</span></span>](getprintprocessordirectory.md)
</dt> </dl>

 

