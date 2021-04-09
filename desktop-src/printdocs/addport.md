---
description: La fonction AddPort ajoute le nom d’un port à la liste des ports pris en charge. La fonction AddPort est exportée par le moniteur de port.
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: AddPort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868345"
---
# <a name="addport-function"></a><span data-ttu-id="435ff-104">AddPort fonction)</span><span class="sxs-lookup"><span data-stu-id="435ff-104">AddPort function</span></span>

<span data-ttu-id="435ff-105">La fonction **addport** ajoute le nom d’un port à la liste des ports pris en charge.</span><span class="sxs-lookup"><span data-stu-id="435ff-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="435ff-106">La fonction **addport** est exportée par le moniteur de port.</span><span class="sxs-lookup"><span data-stu-id="435ff-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="435ff-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="435ff-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="435ff-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="435ff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="435ff-109">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435ff-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435ff-110">Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="435ff-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="435ff-111">Si ce paramètre a la **valeur null**, le port est local.</span><span class="sxs-lookup"><span data-stu-id="435ff-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="435ff-112">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435ff-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435ff-113">Handle de la fenêtre parente de la boîte de dialogue **addport** .</span><span class="sxs-lookup"><span data-stu-id="435ff-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="435ff-114">*pMonitorName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="435ff-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="435ff-115">Pointeur vers une chaîne se terminant par zéro qui spécifie l’analyse associée au port.</span><span class="sxs-lookup"><span data-stu-id="435ff-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="435ff-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="435ff-116">Return value</span></span>

<span data-ttu-id="435ff-117">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="435ff-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="435ff-118">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="435ff-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="435ff-119">Notes</span><span class="sxs-lookup"><span data-stu-id="435ff-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="435ff-120">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="435ff-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="435ff-121">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="435ff-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="435ff-122">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="435ff-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="435ff-123">La fonction **addport** parcourt le réseau pour rechercher les ports existants et affiche une boîte de dialogue pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="435ff-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="435ff-124">La fonction **addport** doit valider le nom de port entré par l’utilisateur en appelant [**EnumPorts**](enumports.md) pour s’assurer qu’il n’existe aucun nom en double.</span><span class="sxs-lookup"><span data-stu-id="435ff-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="435ff-125">L’appelant de la fonction **addport** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="435ff-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="435ff-126">Pour ajouter un port sans afficher de boîte de dialogue, appelez la fonction **XcvData** à la place de **addport**.</span><span class="sxs-lookup"><span data-stu-id="435ff-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="435ff-127">Pour plus d’informations sur **XcvData**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="435ff-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="435ff-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="435ff-128">Requirements</span></span>



| <span data-ttu-id="435ff-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="435ff-129">Requirement</span></span> | <span data-ttu-id="435ff-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="435ff-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="435ff-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435ff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="435ff-132">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435ff-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="435ff-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="435ff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="435ff-134">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="435ff-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="435ff-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="435ff-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="435ff-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="435ff-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="435ff-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="435ff-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="435ff-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="435ff-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="435ff-139">DLL</span><span class="sxs-lookup"><span data-stu-id="435ff-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="435ff-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="435ff-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="435ff-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="435ff-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="435ff-142">**AddPortW** (Unicode) et **AddPortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="435ff-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="435ff-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="435ff-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="435ff-144">Impression</span><span class="sxs-lookup"><span data-stu-id="435ff-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="435ff-145">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="435ff-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="435ff-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="435ff-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="435ff-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="435ff-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="435ff-148">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="435ff-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




