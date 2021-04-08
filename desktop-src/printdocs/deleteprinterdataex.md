---
description: La fonction DeletePrinterDataEx supprime une valeur spécifiée des données de configuration pour une imprimante.
ms.assetid: bcc9cdb3-0fbf-40b6-9de2-1479c3c0ff55
title: DeletePrinterDataEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterDataEx
- DeletePrinterDataExA
- DeletePrinterDataExW
api_type:
- DllExport
api_location:
- Winspool.drv
- Ext-MS-Win-printer-Winspool-l1-1-1.dll
- Ext-MS-Win-Printer-WinSpool-l1-1-2.dll
- Ext-MS-Win-Printer-WinSpool-L1-1-3.dll
ms.openlocfilehash: 07cf6262db0a1e3a3c4c098ee26e03b3fdad4002
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757389"
---
# <a name="deleteprinterdataex-function"></a><span data-ttu-id="6c0a9-103">DeletePrinterDataEx fonction)</span><span class="sxs-lookup"><span data-stu-id="6c0a9-103">DeletePrinterDataEx function</span></span>

<span data-ttu-id="6c0a9-104">La fonction **DeletePrinterDataEx** supprime une valeur spécifiée des données de configuration pour une imprimante.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-104">The **DeletePrinterDataEx** function deletes a specified value from the configuration data for a printer.</span></span> <span data-ttu-id="6c0a9-105">Les données de configuration d’une imprimante consistent en un ensemble de valeurs nommées et typées stockées dans une hiérarchie de clés de registre.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-105">A printer's configuration data consists of a set of named and typed values stored in a hierarchy of registry keys.</span></span> <span data-ttu-id="6c0a9-106">La fonction supprime une valeur spécifiée sous une clé spécifiée.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-106">The function deletes a specified value under a specified key.</span></span>

<span data-ttu-id="6c0a9-107">À l’instar de la fonction [**DeletePrinterData**](deleteprinterdata.md) , **DeletePrinterDataEx** peut supprimer des valeurs stockées par la fonction [**SetPrinterData**](setprinterdata.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0a9-107">Like the [**DeletePrinterData**](deleteprinterdata.md) function, **DeletePrinterDataEx** can delete values stored by the [**SetPrinterData**](setprinterdata.md) function.</span></span> <span data-ttu-id="6c0a9-108">En outre, **DeletePrinterDataEx** peut supprimer des valeurs stockées sous une clé spécifiée par la fonction [**SetPrinterDataEx**](setprinterdataex.md) .</span><span class="sxs-lookup"><span data-stu-id="6c0a9-108">In addition, **DeletePrinterDataEx** can delete values stored under a specified key by the [**SetPrinterDataEx**](setprinterdataex.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c0a9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c0a9-109">Syntax</span></span>


```C++
DWORD DeletePrinterDataEx(
  _In_ HANDLE  hPrinter,
  _In_ LPCTSTR pKeyName,
  _In_ LPCTSTR pValueName
);
```



## <a name="parameters"></a><span data-ttu-id="6c0a9-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c0a9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c0a9-111">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c0a9-111">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0a9-112">Handle vers l’imprimante pour laquelle la fonction supprime une valeur.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-112">A handle to the printer for which the function deletes a value.</span></span> <span data-ttu-id="6c0a9-113">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-113">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="6c0a9-114">*pKeyName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c0a9-114">*pKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0a9-115">Pointeur vers une chaîne se terminant par un caractère null qui spécifie la clé contenant la valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-115">A pointer to a null-terminated string that specifies the key containing the value to delete.</span></span> <span data-ttu-id="6c0a9-116">Utilisez la barre oblique inverse ( \\ ) comme séparateur pour spécifier un chemin d’accès qui a une ou plusieurs sous-clés.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-116">Use the backslash ( \\ ) character as a delimiter to specify a path that has one or more subkeys.</span></span>

<span data-ttu-id="6c0a9-117">Si *pKeyName* a la **valeur null** ou est une chaîne vide, **DELETEPRINTERDATAEX** retourne un paramètre d’erreur \_ non valide \_ .</span><span class="sxs-lookup"><span data-stu-id="6c0a9-117">If *pKeyName* is **NULL** or an empty string, **DeletePrinterDataEx** returns ERROR\_INVALID\_PARAMETER.</span></span>

</dd> <dt>

<span data-ttu-id="6c0a9-118">*pValueName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6c0a9-118">*pValueName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c0a9-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la valeur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-119">A pointer to a null-terminated string that specifies the name of the value to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c0a9-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6c0a9-120">Return value</span></span>

<span data-ttu-id="6c0a9-121">Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-121">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

<span data-ttu-id="6c0a9-122">Si la fonction échoue, la valeur de retour est un code d’erreur système.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-122">If the function fails, the return value is a system error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c0a9-123">Notes</span><span class="sxs-lookup"><span data-stu-id="6c0a9-123">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="6c0a9-124">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-124">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="6c0a9-125">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-125">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="6c0a9-126">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="6c0a9-126">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6c0a9-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6c0a9-127">Requirements</span></span>



| <span data-ttu-id="6c0a9-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6c0a9-128">Requirement</span></span> | <span data-ttu-id="6c0a9-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6c0a9-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c0a9-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c0a9-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6c0a9-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c0a9-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c0a9-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6c0a9-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6c0a9-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6c0a9-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c0a9-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="6c0a9-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c0a9-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c0a9-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="6c0a9-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6c0a9-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c0a9-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c0a9-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="6c0a9-138">DLL</span><span class="sxs-lookup"><span data-stu-id="6c0a9-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c0a9-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="6c0a9-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="6c0a9-140">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="6c0a9-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="6c0a9-141">**DeletePrinterDataExW** (Unicode) et **DeletePrinterDataExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="6c0a9-141">**DeletePrinterDataExW** (Unicode) and **DeletePrinterDataExA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="6c0a9-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6c0a9-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0a9-143">Impression</span><span class="sxs-lookup"><span data-stu-id="6c0a9-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-144">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="6c0a9-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-145">**DeletePrinterKey**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-145">**DeletePrinterKey**</span></span>](deleteprinterkey.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-146">**EnumPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-146">**EnumPrinterDataEx**</span></span>](enumprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-147">**EnumPrinterKey**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-147">**EnumPrinterKey**</span></span>](enumprinterkey.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-148">**GetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-148">**GetPrinterDataEx**</span></span>](getprinterdataex.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-149">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-149">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="6c0a9-150">**SetPrinterDataEx**</span><span class="sxs-lookup"><span data-stu-id="6c0a9-150">**SetPrinterDataEx**</span></span>](setprinterdataex.md)
</dt> </dl>

 

 




