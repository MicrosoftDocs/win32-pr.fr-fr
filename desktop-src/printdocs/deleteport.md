---
description: La fonction DeletePort affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: DeletePort, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203711"
---
# <a name="deleteport-function"></a><span data-ttu-id="35ed4-103">DeletePort fonction)</span><span class="sxs-lookup"><span data-stu-id="35ed4-103">DeletePort function</span></span>

<span data-ttu-id="35ed4-104">La fonction **DeletePort** affiche une boîte de dialogue qui permet à l’utilisateur de supprimer un nom de port.</span><span class="sxs-lookup"><span data-stu-id="35ed4-104">The **DeletePort** function displays a dialog box that allows the user to delete a port name.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ed4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="35ed4-105">Syntax</span></span>


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a><span data-ttu-id="35ed4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="35ed4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ed4-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35ed4-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ed4-108">Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du serveur pour lequel le port doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="35ed4-108">A pointer to a zero-terminated string that specifies the name of the server for which the port should be deleted.</span></span> <span data-ttu-id="35ed4-109">Si ce paramètre a la **valeur null**, un port local est supprimé.</span><span class="sxs-lookup"><span data-stu-id="35ed4-109">If this parameter is **NULL**, a local port is deleted.</span></span>

</dd> <dt>

<span data-ttu-id="35ed4-110">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35ed4-110">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ed4-111">Handle de la fenêtre parente de la boîte de dialogue de suppression de port.</span><span class="sxs-lookup"><span data-stu-id="35ed4-111">A handle to the parent window of the port-deletion dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="35ed4-112">*pPortName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="35ed4-112">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35ed4-113">Pointeur vers une chaîne se terminant par zéro qui spécifie le nom du port qui doit être supprimé.</span><span class="sxs-lookup"><span data-stu-id="35ed4-113">A pointer to a zero-terminated string that specifies the name of the port that should be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ed4-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="35ed4-114">Return value</span></span>

<span data-ttu-id="35ed4-115">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="35ed4-115">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="35ed4-116">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="35ed4-116">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35ed4-117">Notes</span><span class="sxs-lookup"><span data-stu-id="35ed4-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="35ed4-118">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="35ed4-118">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="35ed4-119">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="35ed4-119">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="35ed4-120">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="35ed4-120">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="35ed4-121">Une application peut récupérer les noms des ports valides en appelant la fonction [**EnumPorts**](enumports.md) .</span><span class="sxs-lookup"><span data-stu-id="35ed4-121">An application can retrieve the names of valid ports by calling the [**EnumPorts**](enumports.md) function.</span></span>

<span data-ttu-id="35ed4-122">La fonction **DeletePort** renvoie une erreur si une imprimante est actuellement connectée au port spécifié.</span><span class="sxs-lookup"><span data-stu-id="35ed4-122">The **DeletePort** function returns an error if a printer is currently connected to the specified port.</span></span>

<span data-ttu-id="35ed4-123">L’appelant de la fonction **DeletePort** doit disposer d’un accès serveur \_ \_ administrer l’accès au serveur auquel le port est connecté.</span><span class="sxs-lookup"><span data-stu-id="35ed4-123">The caller of the **DeletePort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ed4-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="35ed4-124">Requirements</span></span>



| <span data-ttu-id="35ed4-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="35ed4-125">Requirement</span></span> | <span data-ttu-id="35ed4-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="35ed4-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ed4-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ed4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="35ed4-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ed4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="35ed4-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="35ed4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="35ed4-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="35ed4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="35ed4-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="35ed4-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="35ed4-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ed4-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="35ed4-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="35ed4-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="35ed4-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="35ed4-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="35ed4-135">DLL</span><span class="sxs-lookup"><span data-stu-id="35ed4-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35ed4-136"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="35ed4-136"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="35ed4-137">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="35ed4-137">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="35ed4-138">**DeletePortW** (Unicode) et **DeletePortA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="35ed4-138">**DeletePortW** (Unicode) and **DeletePortA** (ANSI)</span></span><br/>                                           |



## <a name="see-also"></a><span data-ttu-id="35ed4-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="35ed4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ed4-140">Impression</span><span class="sxs-lookup"><span data-stu-id="35ed4-140">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="35ed4-141">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="35ed4-141">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="35ed4-142">**AddPort**</span><span class="sxs-lookup"><span data-stu-id="35ed4-142">**AddPort**</span></span>](addport.md)
</dt> <dt>

[<span data-ttu-id="35ed4-143">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="35ed4-143">**EnumPorts**</span></span>](enumports.md)
</dt> </dl>

 

 




