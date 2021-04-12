---
description: La fonction SetForm définit les informations de formulaire pour l’imprimante spécifiée.
ms.assetid: 05d5d495-952c-4a1d-8694-1004d0c2bcf6
title: SetForm, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetForm
- SetFormA
- SetFormW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 93848afa0f36032bb972f8f4a7c6c3d5eb8c42ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319089"
---
# <a name="setform-function"></a><span data-ttu-id="b615f-103">SetForm fonction)</span><span class="sxs-lookup"><span data-stu-id="b615f-103">SetForm function</span></span>

<span data-ttu-id="b615f-104">La fonction **SetForm** définit les informations de formulaire pour l’imprimante spécifiée.</span><span class="sxs-lookup"><span data-stu-id="b615f-104">The **SetForm** function sets the form information for the specified printer.</span></span>

## <a name="syntax"></a><span data-ttu-id="b615f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b615f-105">Syntax</span></span>


```C++
BOOL SetForm(
  _In_ HANDLE hPrinter,
  _In_ LPTSTR pFormName,
  _In_ DWORD  Level,
  _In_ LPTSTR pForm
);
```



## <a name="parameters"></a><span data-ttu-id="b615f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b615f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b615f-107">*hPrinter* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b615f-107">*hPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b615f-108">Handle vers l’imprimante pour laquelle les informations de formulaire sont définies.</span><span class="sxs-lookup"><span data-stu-id="b615f-108">A handle to the printer for which the form information is set.</span></span> <span data-ttu-id="b615f-109">Utilisez la fonction [**OpenPrinter**](openprinter.md) ou [**AddPrinter**](addprinter.md) pour récupérer un handle d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="b615f-109">Use the [**OpenPrinter**](openprinter.md) or [**AddPrinter**](addprinter.md) function to retrieve a printer handle.</span></span>

</dd> <dt>

<span data-ttu-id="b615f-110">*pFormName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b615f-110">*pFormName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b615f-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du formulaire pour lequel les informations de formulaire sont définies.</span><span class="sxs-lookup"><span data-stu-id="b615f-111">A pointer to a null-terminated string that specifies the form name for which the form information is set.</span></span>

</dd> <dt>

<span data-ttu-id="b615f-112">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b615f-112">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b615f-113">Version de la structure vers laquelle *pForm* pointe.</span><span class="sxs-lookup"><span data-stu-id="b615f-113">The version of the structure to which *pForm* points.</span></span> <span data-ttu-id="b615f-114">Cette valeur doit être 1 ou 2.</span><span class="sxs-lookup"><span data-stu-id="b615f-114">This value must be 1 or 2.</span></span>

</dd> <dt>

<span data-ttu-id="b615f-115">*pForm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b615f-115">*pForm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b615f-116">Pointeur vers une structure [**d' \_ informations \_**](form-info-1.md) de formulaire 1 ou d' [**informations de formulaire \_ \_ 2**](form-info-2.md) .</span><span class="sxs-lookup"><span data-stu-id="b615f-116">A pointer to a [**FORM\_INFO\_1**](form-info-1.md) or [**FORM\_INFO\_2**](form-info-2.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b615f-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b615f-117">Return value</span></span>

<span data-ttu-id="b615f-118">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="b615f-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="b615f-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="b615f-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="b615f-120">Notes</span><span class="sxs-lookup"><span data-stu-id="b615f-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b615f-121">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="b615f-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="b615f-122">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="b615f-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="b615f-123">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="b615f-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="b615f-124">**SetForm** peut être appelé plusieurs fois pour une [**information de formulaire existante \_ \_ 2**](form-info-2.md), chaque appel ajoutant des paires de valeurs **pDisplayName** et **wLangId** supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="b615f-124">**SetForm** can be called multiple times for an existing [**FORM\_INFO\_2**](form-info-2.md), each call adding additional pairs of **pDisplayName** and **wLangId** values.</span></span> <span data-ttu-id="b615f-125">Toutes les versions linguistiques du formulaire obtiendront les valeurs **Size** et **ImageableArea** des **informations de \_ formulaire \_ 2** dans l’appel le plus récent à **SetForm**.</span><span class="sxs-lookup"><span data-stu-id="b615f-125">All languages versions of the form will get the **Size** and **ImageableArea** values of the **FORM\_INFO\_2** in the most recent call to **SetForm**.</span></span>

<span data-ttu-id="b615f-126">Si l’appelant est distant et que le *niveau* est 2, la valeur **StringType** des [**informations de formulaire \_ \_ 2**](form-info-2.md) ne peut pas être de type chaîne \_ MUIDLL.</span><span class="sxs-lookup"><span data-stu-id="b615f-126">If the caller is remote and the *Level* is 2, the **StringType** value of the [**FORM\_INFO\_2**](form-info-2.md) cannot be STRING\_MUIDLL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b615f-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b615f-127">Requirements</span></span>



| <span data-ttu-id="b615f-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b615f-128">Requirement</span></span> | <span data-ttu-id="b615f-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="b615f-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b615f-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b615f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="b615f-131">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b615f-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="b615f-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b615f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="b615f-133">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b615f-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="b615f-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="b615f-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="b615f-135"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b615f-135"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="b615f-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b615f-136">Library</span></span><br/>                  | <dl> <span data-ttu-id="b615f-137"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b615f-137"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b615f-138">DLL</span><span class="sxs-lookup"><span data-stu-id="b615f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b615f-139"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="b615f-139"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="b615f-140">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="b615f-140">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="b615f-141">**SetFormW** (Unicode) et **SetFormA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="b615f-141">**SetFormW** (Unicode) and **SetFormA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="b615f-142">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b615f-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b615f-143">Impression</span><span class="sxs-lookup"><span data-stu-id="b615f-143">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="b615f-144">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="b615f-144">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="b615f-145">**GetForm**</span><span class="sxs-lookup"><span data-stu-id="b615f-145">**GetForm**</span></span>](getform.md)
</dt> <dt>

[<span data-ttu-id="b615f-146">**OpenPrinter**</span><span class="sxs-lookup"><span data-stu-id="b615f-146">**OpenPrinter**</span></span>](openprinter.md)
</dt> <dt>

[<span data-ttu-id="b615f-147">**Informations de formulaire \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="b615f-147">**FORM\_INFO\_1**</span></span>](form-info-1.md)
</dt> <dt>

[<span data-ttu-id="b615f-148">**Informations de formulaire \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="b615f-148">**FORM\_INFO\_2**</span></span>](form-info-2.md)
</dt> </dl>

 

 




