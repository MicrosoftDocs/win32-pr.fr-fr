---
description: La fonction GetPrinterDriverDirectory récupère le chemin d’accès du répertoire du pilote d’imprimante.
ms.assetid: 69c9cc87-d7e3-496a-b631-b3ae30cdb3fd
title: GetPrinterDriverDirectory, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverDirectory
- GetPrinterDriverDirectoryA
- GetPrinterDriverDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 7acc68f99f9791ba4231bcfea2b1788cfb37011c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530242"
---
# <a name="getprinterdriverdirectory-function"></a><span data-ttu-id="80080-103">GetPrinterDriverDirectory fonction)</span><span class="sxs-lookup"><span data-stu-id="80080-103">GetPrinterDriverDirectory function</span></span>

<span data-ttu-id="80080-104">La fonction **GetPrinterDriverDirectory** récupère le chemin d’accès du répertoire du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="80080-104">The **GetPrinterDriverDirectory** function retrieves the path of the printer-driver directory.</span></span>

## <a name="syntax"></a><span data-ttu-id="80080-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80080-105">Syntax</span></span>


```C++
BOOL GetPrinterDriverDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pDriverDirectory,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="80080-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="80080-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80080-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80080-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote d’imprimante réside.</span><span class="sxs-lookup"><span data-stu-id="80080-108">A pointer to a null-terminated string that specifies the name of the server on which the printer driver resides.</span></span> <span data-ttu-id="80080-109">Si ce paramètre a la **valeur null**, le chemin d’accès au répertoire du pilote local est récupéré.</span><span class="sxs-lookup"><span data-stu-id="80080-109">If this parameter is **NULL**, the local driver-directory path is retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="80080-110">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80080-110">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement (par exemple, Windows x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="80080-111">A pointer to a null-terminated string that specifies the environment (for example, Windows x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="80080-112">Si ce paramètre a la **valeur null**, l’environnement actuel de l’application appelante et de l’ordinateur client (pas du serveur d’impression et de l’application de destination) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="80080-112">If this parameter is **NULL**, the current environment of the calling application and client machine (not of the destination application and print server) is used.</span></span>

</dd> <dt>

<span data-ttu-id="80080-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80080-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-114">Niveau de la structure.</span><span class="sxs-lookup"><span data-stu-id="80080-114">The structure level.</span></span> <span data-ttu-id="80080-115">Cette valeur doit être 1.</span><span class="sxs-lookup"><span data-stu-id="80080-115">This value must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="80080-116">*pDriverDirectory* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80080-116">*pDriverDirectory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-117">Pointeur vers une mémoire tampon qui reçoit le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="80080-117">A pointer to a buffer that receives the path.</span></span>

</dd> <dt>

<span data-ttu-id="80080-118">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="80080-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-119">Taille de la mémoire tampon à laquelle *pDriverDirectory* pointe.</span><span class="sxs-lookup"><span data-stu-id="80080-119">The size of the buffer to which *pDriverDirectory* points.</span></span>

</dd> <dt>

<span data-ttu-id="80080-120">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="80080-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80080-121">Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie, ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="80080-121">A pointer to a value that specifies the number of bytes copied if the function succeeds, or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80080-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="80080-122">Return value</span></span>

<span data-ttu-id="80080-123">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="80080-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="80080-124">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="80080-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="80080-125">Notes</span><span class="sxs-lookup"><span data-stu-id="80080-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="80080-126">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="80080-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="80080-127">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="80080-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="80080-128">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="80080-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="80080-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80080-129">Requirements</span></span>



| <span data-ttu-id="80080-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80080-130">Requirement</span></span> | <span data-ttu-id="80080-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="80080-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80080-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80080-132">Minimum supported client</span></span><br/> | <span data-ttu-id="80080-133">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80080-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80080-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80080-134">Minimum supported server</span></span><br/> | <span data-ttu-id="80080-135">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="80080-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80080-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="80080-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="80080-137"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="80080-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="80080-138">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="80080-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="80080-139"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="80080-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="80080-140">DLL</span><span class="sxs-lookup"><span data-stu-id="80080-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80080-141"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="80080-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="80080-142">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="80080-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="80080-143">**GetPrinterDriverDirectoryW** (Unicode) et **GetPrinterDriverDirectoryA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="80080-143">**GetPrinterDriverDirectoryW** (Unicode) and **GetPrinterDriverDirectoryA** (ANSI)</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="80080-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80080-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80080-145">Impression</span><span class="sxs-lookup"><span data-stu-id="80080-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="80080-146">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="80080-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="80080-147">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="80080-147">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> </dl>

 

 




