---
description: La fonction ReadPrinter récupère les données de l’imprimante spécifiée.
ms.assetid: d7c3f186-c53e-424b-89bf-6742babb998f
title: ReadPrinter, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ReadPrinter
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ddbdfc03b80557583c60f461f0c7e3a6fe2473fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528189"
---
# <a name="readprinter-function"></a><span data-ttu-id="ff9d2-103">ReadPrinter fonction)</span><span class="sxs-lookup"><span data-stu-id="ff9d2-103">ReadPrinter function</span></span>

<span data-ttu-id="ff9d2-104">La fonction **ReadPrinter** récupère les données de l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-104">The **ReadPrinter** function retrieves data from the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9d2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff9d2-105">Syntax</span></span>


```C++
BOOL ReadPrinter(
  _In_  HANDLE  hPrinter,
  _Out_ LPVOID  pBuf,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pNoBytesRead
);
```



## <a name="parameters"></a><span data-ttu-id="ff9d2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ff9d2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff9d2-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9d2-108">Handle de l’objet Printer pour lequel récupérer des données.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-108">A handle to the printer object for which to retrieve data.</span></span> <span data-ttu-id="ff9d2-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) pour récupérer un handle d’objet Printer.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-109">Use the [**OpenPrinter**](openprinter.md) function to retrieve a printer object handle.</span></span> <span data-ttu-id="ff9d2-110">Utilisez le format : nom_imprimante, Job xxxx.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-110">Use the format: Printername, Job xxxx.</span></span>

</dd> <dt>

<span data-ttu-id="ff9d2-111">*pBuf* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-111">*pBuf* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9d2-112">Pointeur vers une mémoire tampon qui reçoit les données de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-112">A pointer to a buffer that receives the printer data.</span></span>

</dd> <dt>

<span data-ttu-id="ff9d2-113">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-113">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9d2-114">Taille, en octets, de la mémoire tampon vers laquelle *pBuf* pointe.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-114">The size, in bytes, of the buffer to which *pBuf* points.</span></span>

</dd> <dt>

<span data-ttu-id="ff9d2-115">*pNoBytesRead* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-115">*pNoBytesRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ff9d2-116">Pointeur vers une variable qui reçoit le nombre d’octets de données copiés dans le tableau vers lequel *pBuf* pointe.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-116">A pointer to a variable that receives the number of bytes of data copied into the array to which *pBuf* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff9d2-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ff9d2-117">Return value</span></span>

<span data-ttu-id="ff9d2-118">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ff9d2-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff9d2-120">Notes</span><span class="sxs-lookup"><span data-stu-id="ff9d2-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ff9d2-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ff9d2-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ff9d2-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ff9d2-124">**ReadPrinter** renvoie une erreur si l’appareil ou l’imprimante n’est pas bidirectionnel.</span><span class="sxs-lookup"><span data-stu-id="ff9d2-124">**ReadPrinter** returns an error if the device or the printer is not bidirectional.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff9d2-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff9d2-125">Requirements</span></span>



| <span data-ttu-id="ff9d2-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff9d2-126">Requirement</span></span> | <span data-ttu-id="ff9d2-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff9d2-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff9d2-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff9d2-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ff9d2-129">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ff9d2-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff9d2-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ff9d2-131">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ff9d2-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ff9d2-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff9d2-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ff9d2-133"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff9d2-133"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ff9d2-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff9d2-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="ff9d2-135"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ff9d2-135"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ff9d2-136">DLL</span><span class="sxs-lookup"><span data-stu-id="ff9d2-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff9d2-137"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff9d2-137"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="ff9d2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ff9d2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff9d2-139">Impression</span><span class="sxs-lookup"><span data-stu-id="ff9d2-139">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ff9d2-140">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ff9d2-140">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ff9d2-141">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="ff9d2-141">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




