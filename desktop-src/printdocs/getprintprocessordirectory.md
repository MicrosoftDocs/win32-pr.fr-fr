---
description: La fonction GetPrintProcessorDirectory récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: GetPrintProcessorDirectory, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868537"
---
# <a name="getprintprocessordirectory-function"></a><span data-ttu-id="e05ab-103">GetPrintProcessorDirectory fonction)</span><span class="sxs-lookup"><span data-stu-id="e05ab-103">GetPrintProcessorDirectory function</span></span>

<span data-ttu-id="e05ab-104">La fonction **GetPrintProcessorDirectory** récupère le chemin d’accès au répertoire du processeur d’impression sur le serveur spécifié.</span><span class="sxs-lookup"><span data-stu-id="e05ab-104">The **GetPrintProcessorDirectory** function retrieves the path to the print processor directory on the specified server.</span></span>

## <a name="syntax"></a><span data-ttu-id="e05ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e05ab-105">Syntax</span></span>


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="e05ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e05ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e05ab-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="e05ab-108">A pointer to a null-terminated string that specifies the name of the server.</span></span> <span data-ttu-id="e05ab-109">Si ce paramètre a la **valeur null**, un chemin d’accès local est retourné.</span><span class="sxs-lookup"><span data-stu-id="e05ab-109">If this parameter is **NULL**, a local path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e05ab-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e05ab-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="e05ab-112">Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="e05ab-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="e05ab-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-114">Niveau de la structure.</span><span class="sxs-lookup"><span data-stu-id="e05ab-114">The structure level.</span></span> <span data-ttu-id="e05ab-115">Cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="e05ab-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="e05ab-116">*pPrintProcessorInfo* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-116">*pPrintProcessorInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-117">Pointeur vers une mémoire tampon qui reçoit le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="e05ab-117">A pointer to a buffer that receives the path.</span></span> <span data-ttu-id="e05ab-118">Notez que, pour les systèmes d’exploitation antérieurs à Windows Server 2003 SP 1, le chemin d’accès est au format local pour le serveur, et non dans le format à distance réel.</span><span class="sxs-lookup"><span data-stu-id="e05ab-118">Note that, for operating systems prior to Windows Server 2003 SP 1, the path is in the local format for the server, not the true remote format.</span></span> <span data-ttu-id="e05ab-119">Par exemple, le chemin d’accès est spécifié sous la forme « % windir% \\ system32 \\ spool \\ prtprocs \\ % environnement% » au lieu de « \\ \\ nom_serveur \\ Print $ \\ prtprocs \\ % environnement% », même lorsqu’il est appelé pour un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="e05ab-119">For example, the path is given as "%Windir%\\System32\\Spool\\Prtprocs\\%Environment%" instead of "\\\\ServerName\\Print$\\Prtprocs\\%Environment%", even when called for a remote server.</span></span> <span data-ttu-id="e05ab-120">Pour les systèmes d’exploitation Windows Server 2003 SP 1 et versions ultérieures, le chemin d’accès distant réel est retourné.</span><span class="sxs-lookup"><span data-stu-id="e05ab-120">For the operating systems Windows Server 2003 SP 1 and later, the true remote path is returned.</span></span>

</dd> <dt>

<span data-ttu-id="e05ab-121">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-121">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-122">Taille de la mémoire tampon vers laquelle pointe *pPrintProcessorInfo*.</span><span class="sxs-lookup"><span data-stu-id="e05ab-122">The size of the buffer pointed to by *pPrintProcessorInfo*.</span></span>

</dd> <dt>

<span data-ttu-id="e05ab-123">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-123">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e05ab-124">Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie, ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="e05ab-124">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e05ab-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e05ab-125">Return value</span></span>

<span data-ttu-id="e05ab-126">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e05ab-126">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e05ab-127">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="e05ab-127">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e05ab-128">Notes</span><span class="sxs-lookup"><span data-stu-id="e05ab-128">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e05ab-129">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e05ab-129">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e05ab-130">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="e05ab-130">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e05ab-131">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="e05ab-131">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e05ab-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e05ab-132">Requirements</span></span>



| <span data-ttu-id="e05ab-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e05ab-133">Requirement</span></span> | <span data-ttu-id="e05ab-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="e05ab-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e05ab-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e05ab-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e05ab-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e05ab-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e05ab-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e05ab-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e05ab-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e05ab-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="e05ab-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="e05ab-140"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e05ab-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e05ab-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e05ab-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="e05ab-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e05ab-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e05ab-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e05ab-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e05ab-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e05ab-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e05ab-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e05ab-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e05ab-146">**GetPrintProcessorDirectoryW** (Unicode) et **GetPrintProcessorDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e05ab-146">**GetPrintProcessorDirectoryW** (Unicode) and **GetPrintProcessorDirectoryA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="e05ab-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e05ab-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e05ab-148">Impression</span><span class="sxs-lookup"><span data-stu-id="e05ab-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e05ab-149">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="e05ab-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e05ab-150">**AddPrintProcessor**</span><span class="sxs-lookup"><span data-stu-id="e05ab-150">**AddPrintProcessor**</span></span>](addprintprocessor.md)
</dt> </dl>

 

 




