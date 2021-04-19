---
description: La fonction AddForm ajoute un formulaire à la liste des formulaires disponibles qui peuvent être sélectionnés pour l’imprimante spécifiée.
ms.assetid: 17b59019-f93a-4b57-86fb-91c61aecbac4
title: AddForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddForm
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2de3ddbdc57a5a41bac048a94a8175cd124df4ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106525043"
---
# <a name="addform-function"></a><span data-ttu-id="c22c1-103">AddForm fonction)</span><span class="sxs-lookup"><span data-stu-id="c22c1-103">AddForm function</span></span>

<span data-ttu-id="c22c1-104">La fonction **AddForm** ajoute un formulaire à la liste des formulaires disponibles qui peuvent être sélectionnés pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="c22c1-104">The **AddForm** function adds a form to the list of available forms that can be selected for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="c22c1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c22c1-105">Syntax</span></span>


```C++
BOOL AddForm(
  _In_ HANDLE hPrinter,
  _In_ DWORD  Level,
  _In_ LPBYTE pForm
);
```



## <a name="parameters"></a><span data-ttu-id="c22c1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c22c1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c22c1-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c22c1-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22c1-108">Handle vers l’imprimante qui prend en charge l’impression avec le formulaire spécifié.</span><span class="sxs-lookup"><span data-stu-id="c22c1-108">A handle to the printer that supports printing with the specified form.</span></span> <span data-ttu-id="c22c1-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="c22c1-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="c22c1-110">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c22c1-110">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22c1-111">Niveau de la structure vers laquelle *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="c22c1-111">The level of the structure to which *pForm* points.</span></span> <span data-ttu-id="c22c1-112">Cette valeur doit être 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="c22c1-112">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="c22c1-113">*pForm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c22c1-113">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c22c1-114">Pointeur vers une structure [**d' \_ informations \_**](form-info-1.md) de formulaire 1 ou d' [**informations de formulaire \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="c22c1-114">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c22c1-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c22c1-115">Return value</span></span>

<span data-ttu-id="c22c1-116">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c22c1-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="c22c1-117">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="c22c1-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="c22c1-118">Notes</span><span class="sxs-lookup"><span data-stu-id="c22c1-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c22c1-119">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c22c1-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c22c1-120">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="c22c1-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c22c1-121">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="c22c1-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c22c1-122">Une application peut déterminer les formulaires disponibles pour une imprimante en appelant la fonction [**EnumForms**](enumforms.md) .</span><span class="sxs-lookup"><span data-stu-id="c22c1-122">An application can determine which forms are available for a printer by calling the [**EnumForms**](enumforms.md) function.</span></span>

<span data-ttu-id="c22c1-123">Si *pForm* pointe vers une [**information de formulaire \_ \_ 2**](form-info-2.md), **AddForm** échouera s’il existe déjà un formulaire portant le nom spécifié ou si la valeur *pKeyword* de la structure existe déjà.</span><span class="sxs-lookup"><span data-stu-id="c22c1-123">If *pForm* points to a [**FORM\_INFO\_2**](form-info-2.md), then **AddForm** will fail if either a form with the specified name already exists or the structure's *pKeyword* value already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c22c1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c22c1-124">Requirements</span></span>



| <span data-ttu-id="c22c1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c22c1-125">Requirement</span></span> | <span data-ttu-id="c22c1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="c22c1-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c22c1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c22c1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c22c1-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c22c1-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c22c1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c22c1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c22c1-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c22c1-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c22c1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="c22c1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="c22c1-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c22c1-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c22c1-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c22c1-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="c22c1-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c22c1-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c22c1-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c22c1-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c22c1-136"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c22c1-136"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="c22c1-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c22c1-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c22c1-138">Impression</span><span class="sxs-lookup"><span data-stu-id="c22c1-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c22c1-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c22c1-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="c22c1-140">**EnumForms**</span><span class="sxs-lookup"><span data-stu-id="c22c1-140">**EnumForms**</span></span>](enumforms.md)
</dt> <dt>

[<span data-ttu-id="c22c1-141">**Informations de formulaire \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="c22c1-141">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="c22c1-142">**Informations de formulaire \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="c22c1-142">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> <dt>

[<span data-ttu-id="c22c1-143">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="c22c1-143">**OpenPrinter**</span></span>](openprinter.md)
</dt> </dl>

 

 




