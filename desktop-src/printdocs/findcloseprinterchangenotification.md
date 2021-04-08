---
description: La fonction FindClosePrinterChangeNotification ferme un objet de notification de modification créé en appelant la fonction FindFirstPrinterChangeNotification.
ms.assetid: 2b4758f8-af0a-494b-8f1b-8ea6ee73c79b
title: FindClosePrinterChangeNotification, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindClosePrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8040944d5890aa521681827bef786201a35da039
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034466"
---
# <a name="findcloseprinterchangenotification-function"></a><span data-ttu-id="2afd4-103">FindClosePrinterChangeNotification fonction)</span><span class="sxs-lookup"><span data-stu-id="2afd4-103">FindClosePrinterChangeNotification function</span></span>

<span data-ttu-id="2afd4-104">La fonction **FindClosePrinterChangeNotification** ferme un objet de notification de modification créé en appelant la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2afd4-104">The **FindClosePrinterChangeNotification** function closes a change notification object created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="2afd4-105">L’imprimante ou le serveur d’impression associé à l’objet de notification de modification n’est plus analysé par cet objet.</span><span class="sxs-lookup"><span data-stu-id="2afd4-105">The printer or print server associated with the change notification object will no longer be monitored by that object.</span></span>

## <a name="syntax"></a><span data-ttu-id="2afd4-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2afd4-106">Syntax</span></span>


```C++
BOOL FindClosePrinterChangeNotification(
  _In_ HANDLE hChange
);
```



## <a name="parameters"></a><span data-ttu-id="2afd4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2afd4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2afd4-108">*hChange* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2afd4-108">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2afd4-109">Handle de l’objet de notification de modification à fermer.</span><span class="sxs-lookup"><span data-stu-id="2afd4-109">A handle to the change notification object to be closed.</span></span> <span data-ttu-id="2afd4-110">Il s’agit d’un handle créé en appelant la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="2afd4-110">This is a handle created by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2afd4-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2afd4-111">Return value</span></span>

<span data-ttu-id="2afd4-112">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="2afd4-112">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="2afd4-113">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="2afd4-113">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2afd4-114">Notes</span><span class="sxs-lookup"><span data-stu-id="2afd4-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2afd4-115">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2afd4-115">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="2afd4-116">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="2afd4-116">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="2afd4-117">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="2afd4-117">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="2afd4-118">Après l’appel de la fonction **FindClosePrinterChangeNotification** , vous ne pouvez pas utiliser le handle *hChange* dans les appels suivants à [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) ou [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span><span class="sxs-lookup"><span data-stu-id="2afd4-118">After calling the **FindClosePrinterChangeNotification** function, you cannot use the *hChange* handle in subsequent calls to either [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) or [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2afd4-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2afd4-119">Requirements</span></span>



| <span data-ttu-id="2afd4-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2afd4-120">Requirement</span></span> | <span data-ttu-id="2afd4-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2afd4-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2afd4-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afd4-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2afd4-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2afd4-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="2afd4-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2afd4-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2afd4-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2afd4-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="2afd4-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="2afd4-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="2afd4-127"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2afd4-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="2afd4-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="2afd4-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="2afd4-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2afd4-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="2afd4-130">DLL</span><span class="sxs-lookup"><span data-stu-id="2afd4-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2afd4-131"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2afd4-131"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="2afd4-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2afd4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2afd4-133">Impression</span><span class="sxs-lookup"><span data-stu-id="2afd4-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="2afd4-134">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="2afd4-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="2afd4-135">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2afd4-135">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="2afd4-136">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="2afd4-136">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> </dl>

 

 




