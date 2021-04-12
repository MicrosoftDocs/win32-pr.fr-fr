---
description: La fonction DeletePrintProvidor supprime un fournisseur d’impression ajouté par la fonction AddPrintProvidor.
ms.assetid: b7104f9a-111c-4904-a355-063bb4cc81f1
title: DeletePrintProvidor, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrintProvidor
- DeletePrintProvidorA
- DeletePrintProvidorW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: e68e56f115bac8abb1d0999990f57067f791d76d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203710"
---
# <a name="deleteprintprovidor-function"></a><span data-ttu-id="e08e8-103">DeletePrintProvidor fonction)</span><span class="sxs-lookup"><span data-stu-id="e08e8-103">DeletePrintProvidor function</span></span>

<span data-ttu-id="e08e8-104">La fonction **DeletePrintProvidor** supprime un fournisseur d’impression ajouté par la fonction [**AddPrintProvidor**](addprintprovidor.md) .</span><span class="sxs-lookup"><span data-stu-id="e08e8-104">The **DeletePrintProvidor** function removes a print provider added by the [**AddPrintProvidor**](addprintprovidor.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="e08e8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e08e8-105">Syntax</span></span>


```C++
BOOL DeletePrintProvidor(
  _In_ LPTSTR pName,
  _In_ LPTSTR pEnvironment,
  _In_ LPTSTR pPrintProviderName
);
```



## <a name="parameters"></a><span data-ttu-id="e08e8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e08e8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e08e8-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e08e8-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08e8-108">Réservé doit avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="e08e8-108">Reserved; must be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e08e8-109">*pEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e08e8-109">*pEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08e8-110">Pointeur vers une chaîne se terminant par un caractère null qui spécifie l’environnement à partir duquel le fournisseur doit être supprimé (par exemple, Windows NT x86, Windows IA64 ou Windows x64).</span><span class="sxs-lookup"><span data-stu-id="e08e8-110">A pointer to a null-terminated string that specifies the environment from which the provider is to be removed (for example, Windows NT x86, Windows IA64, or Windows x64).</span></span> <span data-ttu-id="e08e8-111">Si ce paramètre a la **valeur null**, le fournisseur est supprimé de l’environnement actuel de l’application appelante et de l’ordinateur client (et non de l’application de destination et du serveur d’impression).</span><span class="sxs-lookup"><span data-stu-id="e08e8-111">If this parameter is **NULL**, the provider is removed from the current environment of the calling application and client machine (not of the destination application and print server).</span></span> <span data-ttu-id="e08e8-112">La valeur **null** est recommandée, car elle offre une portabilité maximale.</span><span class="sxs-lookup"><span data-stu-id="e08e8-112">**NULL** is the recommended value because it provides maximum portability.</span></span>

</dd> <dt>

<span data-ttu-id="e08e8-113">*pPrintProviderName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e08e8-113">*pPrintProviderName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e08e8-114">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du fournisseur à supprimer.</span><span class="sxs-lookup"><span data-stu-id="e08e8-114">A pointer to a null-terminated string that specifies the name of the provider to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e08e8-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e08e8-115">Return value</span></span>

<span data-ttu-id="e08e8-116">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="e08e8-116">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="e08e8-117">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="e08e8-117">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="e08e8-118">Notes</span><span class="sxs-lookup"><span data-stu-id="e08e8-118">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e08e8-119">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e08e8-119">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e08e8-120">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="e08e8-120">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e08e8-121">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="e08e8-121">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="e08e8-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e08e8-122">Requirements</span></span>



| <span data-ttu-id="e08e8-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e08e8-123">Requirement</span></span> | <span data-ttu-id="e08e8-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="e08e8-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e08e8-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e08e8-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e08e8-126">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e08e8-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e08e8-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e08e8-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e08e8-128">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e08e8-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e08e8-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="e08e8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e08e8-130"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e08e8-130"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e08e8-131">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e08e8-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="e08e8-132"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e08e8-132"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e08e8-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e08e8-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e08e8-134"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e08e8-134"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="e08e8-135">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="e08e8-135">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="e08e8-136">**DeletePrintProvidorW** (Unicode) et **DeletePrintProvidorA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="e08e8-136">**DeletePrintProvidorW** (Unicode) and **DeletePrintProvidorA** (ANSI)</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="e08e8-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e08e8-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e08e8-138">Impression</span><span class="sxs-lookup"><span data-stu-id="e08e8-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e08e8-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="e08e8-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e08e8-140">**AddPrintProvidor**</span><span class="sxs-lookup"><span data-stu-id="e08e8-140">**AddPrintProvidor**</span></span>](addprintprovidor.md)
</dt> </dl>

 

 




