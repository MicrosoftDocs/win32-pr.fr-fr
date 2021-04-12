---
description: La fonction EnumForms énumère les formulaires pris en charge par l’imprimante spécifiée.
ms.assetid: b13b515a-c764-4a80-ab85-95fb4abb2a6b
title: EnumForms, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumForms
- EnumFormsA
- EnumFormsW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 18cd9ad6f8e0491700d5618e29a0a629e8045366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319097"
---
# <a name="enumforms-function"></a><span data-ttu-id="d6fa7-103">EnumForms fonction)</span><span class="sxs-lookup"><span data-stu-id="d6fa7-103">EnumForms function</span></span>

<span data-ttu-id="d6fa7-104">La fonction **EnumForms** énumère les formulaires pris en charge par l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-104">The **EnumForms** function enumerates the forms supported by the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6fa7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6fa7-105">Syntax</span></span>


```C++
BOOL EnumForms(
  _In_  HANDLE  hPrinter,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded,
  _Out_ LPDWORD pcReturned
);
```



## <a name="parameters"></a><span data-ttu-id="d6fa7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6fa7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6fa7-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-108">Handle vers l’imprimante pour laquelle les formulaires doivent être énumérés.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-108">Handle to the printer for which the forms should be enumerated.</span></span> <span data-ttu-id="d6fa7-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d6fa7-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-111">Spécifie la version de la structure vers laquelle *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-111">Specifies the version of the structure to which *pForm* points.</span></span> <span data-ttu-id="d6fa7-112">Cette valeur doit être 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d6fa7-113">*pForm* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-113">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-114">Pointeur vers une ou plusieurs structures d' [**informations de formulaire \_ \_ 1**](form-info-1.md) ou vers une ou plusieurs structures d' [**informations de formulaire \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="d6fa7-114">Pointer to one or more [**FORM\_INFO\_1**](form-info-1.md) structures or to one or more [**FORM\_INFO\_2**](form-info-2.md) structures.</span></span> <span data-ttu-id="d6fa7-115">Toutes les structures ont le même niveau.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-115">All the structures will have the same level.</span></span>

</dd> <dt>

<span data-ttu-id="d6fa7-116">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-116">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-117">Spécifie la taille, en octets, de la mémoire tampon vers laquelle *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-117">Specifies the size, in bytes, of the buffer to which *pForm* points.</span></span>

</dd> <dt>

<span data-ttu-id="d6fa7-118">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-118">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-119">Pointeur vers une variable qui reçoit le nombre d’octets copiés dans le tableau vers lequel *pForm* pointe (si l’opération réussit) ou le nombre d’octets requis (en cas d’échec, car *cbBuf* est trop petit).</span><span class="sxs-lookup"><span data-stu-id="d6fa7-119">Pointer to a variable that receives the number of bytes copied to the array to which *pForm* points (if the operation succeeds) or the number of bytes required (if it fails because *cbBuf* is too small).</span></span>

</dd> <dt>

<span data-ttu-id="d6fa7-120">*pcReturned* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-120">*pcReturned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6fa7-121">Pointeur vers une variable qui reçoit le nombre de structures copiées dans le tableau vers lequel *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-121">Pointer to a variable that receives the number of structures copied into the array to which *pForm* points.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6fa7-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6fa7-122">Return value</span></span>

<span data-ttu-id="d6fa7-123">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d6fa7-124">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6fa7-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d6fa7-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6fa7-126">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d6fa7-127">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d6fa7-128">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d6fa7-129">Si l’appelant est distant et que le *niveau* est 2, la **valeur StringType** des structures d' [**informations de formulaire \_ \_ 2**](form-info-2.md) retournées est toujours la **chaîne \_ LANGPAIR**.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) structures will always be **STRING\_LANGPAIR**.</span></span>

<span data-ttu-id="d6fa7-130">Dans Windows Vista, les données de formulaire retournées par **EnumForms** sont récupérées à partir d’un cache local lorsque *hPrinter* fait référence à un serveur d’impression distant ou à une imprimante hébergée par un serveur d’impression et qu’il existe au moins une connexion ouverte à une imprimante sur le serveur d’impression distant.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-130">In Windows Vista, the form data returned by **EnumForms** is retrieved from a local cache when *hPrinter* refers to a remote print server or a printer hosted by a print server and there is at least one open connection to a printer on the remote print server.</span></span> <span data-ttu-id="d6fa7-131">Dans toutes les autres configurations, les données du formulaire sont interrogées à partir du serveur d’impression distant.</span><span class="sxs-lookup"><span data-stu-id="d6fa7-131">In all other configurations, the form data is queried from the remote print server.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6fa7-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6fa7-132">Requirements</span></span>



| <span data-ttu-id="d6fa7-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6fa7-133">Requirement</span></span> | <span data-ttu-id="d6fa7-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6fa7-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6fa7-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6fa7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d6fa7-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6fa7-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6fa7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d6fa7-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6fa7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6fa7-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6fa7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6fa7-140"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6fa7-140"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d6fa7-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6fa7-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6fa7-142"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6fa7-142"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d6fa7-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d6fa7-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6fa7-144"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d6fa7-144"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d6fa7-145">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d6fa7-145">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d6fa7-146">**EnumFormsW** (Unicode) et **EnumFormsA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d6fa7-146">**EnumFormsW** (Unicode) and **EnumFormsA** (ANSI)</span></span><br/>                                             |



## <a name="see-also"></a><span data-ttu-id="d6fa7-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6fa7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6fa7-148">Impression</span><span class="sxs-lookup"><span data-stu-id="d6fa7-148">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d6fa7-149">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d6fa7-149">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d6fa7-150">**AddPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6fa7-150">**AddPrinter**</span></span>](addprinter.md)
</dt> <dt>

[<span data-ttu-id="d6fa7-151">**Informations de formulaire \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="d6fa7-151">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="d6fa7-152">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6fa7-152">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




