---
description: La fonction GetForm récupère des informations sur un formulaire spécifié.
ms.assetid: 10b25748-6d7c-46ab-bd2c-9b6126a1d7d1
title: GetForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetForm
- GetFormA
- GetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 6b6ea9753e1b335936778e17562f6f26467b3083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106544939"
---
# <a name="getform-function"></a><span data-ttu-id="d6254-103">GetForm fonction)</span><span class="sxs-lookup"><span data-stu-id="d6254-103">GetForm function</span></span>

<span data-ttu-id="d6254-104">La fonction **GetForm** récupère des informations sur un formulaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="d6254-104">The **GetForm** function retrieves information about a specified form.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6254-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d6254-105">Syntax</span></span>


```C++
BOOL GetForm(
  _In_  HANDLE  hPrinter,
  _In_  LPTSTR  pFormName,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pForm,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a><span data-ttu-id="d6254-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d6254-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d6254-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6254-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-108">Handle vers l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d6254-108">A handle to the printer.</span></span> <span data-ttu-id="d6254-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d6254-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="d6254-110">*pFormName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6254-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire.</span><span class="sxs-lookup"><span data-stu-id="d6254-111">A pointer to a null-terminated string that specifies the name of the form.</span></span> <span data-ttu-id="d6254-112">Pour récupérer les noms des formulaires pris en charge par l’imprimante, appelez la fonction [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="d6254-112">To get the names of the forms supported by the printer, call the [**EnumForms**](enumforms.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d6254-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6254-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-114">Version de la structure vers laquelle *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="d6254-114">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="d6254-115">Cette valeur doit être 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="d6254-115">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="d6254-116">*pForm* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6254-116">*pForm* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-117">Pointeur vers un tableau d’octets qui reçoit la structure d' [**informations de \_ formulaire \_ 1**](form-info-1.md) ou [**d' \_ informations \_ de formulaire 2**](form-info-2.md) initialisée.</span><span class="sxs-lookup"><span data-stu-id="d6254-117">A pointer to an array of bytes that receives the initialized [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="d6254-118">*cbBuf* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d6254-118">*cbBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-119">Taille, en octets, du tableau *pForm* .</span><span class="sxs-lookup"><span data-stu-id="d6254-119">The size, in bytes, of the *pForm* array.</span></span>

</dd> <dt>

<span data-ttu-id="d6254-120">*pcbNeeded* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d6254-120">*pcbNeeded* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d6254-121">Pointeur vers une valeur qui spécifie le nombre d’octets copiés si la fonction est réussie ou le nombre d’octets requis si *cbBuf* est trop petit.</span><span class="sxs-lookup"><span data-stu-id="d6254-121">A pointer to a value that specifies the number of bytes copied if the function succeeds or the number of bytes required if *cbBuf* is too small.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d6254-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d6254-122">Return value</span></span>

<span data-ttu-id="d6254-123">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d6254-123">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d6254-124">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d6254-124">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d6254-125">Notes</span><span class="sxs-lookup"><span data-stu-id="d6254-125">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d6254-126">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d6254-126">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d6254-127">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d6254-127">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d6254-128">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d6254-128">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d6254-129">Si l’appelant est distant et que le *niveau* est 2, la valeur **StringType** des informations de [**formulaire \_ \_ 2**](form-info-2.md) retournées est toujours la chaîne \_ LANGPAIR.</span><span class="sxs-lookup"><span data-stu-id="d6254-129">If the caller is remote, and the *Level* is 2, the **StringType** value of the returned [**FORM\_INFO\_2**](form-info-2.md) will always be STRING\_LANGPAIR.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6254-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d6254-130">Requirements</span></span>



| <span data-ttu-id="d6254-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d6254-131">Requirement</span></span> | <span data-ttu-id="d6254-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="d6254-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6254-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6254-133">Minimum supported client</span></span><br/> | <span data-ttu-id="d6254-134">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6254-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d6254-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d6254-135">Minimum supported server</span></span><br/> | <span data-ttu-id="d6254-136">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d6254-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d6254-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="d6254-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6254-138"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6254-138"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d6254-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d6254-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="d6254-140"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d6254-140"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d6254-141">DLL</span><span class="sxs-lookup"><span data-stu-id="d6254-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d6254-142"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="d6254-142"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d6254-143">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="d6254-143">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d6254-144">**GetFormW** (Unicode) et **GetFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d6254-144">**GetFormW** (Unicode) and **GetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="d6254-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d6254-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6254-146">Impression</span><span class="sxs-lookup"><span data-stu-id="d6254-146">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d6254-147">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d6254-147">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d6254-148">**AddForm**</span><span class="sxs-lookup"><span data-stu-id="d6254-148">**AddForm**</span></span>](addform.md)
</dt> <dt>

[<span data-ttu-id="d6254-149">**DeleteForm**</span><span class="sxs-lookup"><span data-stu-id="d6254-149">**DeleteForm**</span></span>](deleteform.md)
</dt> <dt>

[<span data-ttu-id="d6254-150">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="d6254-150">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="d6254-151">**SetForm**</span><span class="sxs-lookup"><span data-stu-id="d6254-151">**SetForm**</span></span>](setform.md)
</dt> </dl>

 

 




