---
description: La fonction FreePrinterNotifyInfo libère une mémoire tampon allouée par le système créée par la fonction FindNextPrinterChangeNotification.
ms.assetid: e50d4718-3682-486b-9d07-ddddd0b284dc
title: FreePrinterNotifyInfo, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreePrinterNotifyInfo
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 8d2cc22971c2645af250a9e92872b89959387163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534505"
---
# <a name="freeprinternotifyinfo-function"></a><span data-ttu-id="67c45-103">FreePrinterNotifyInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="67c45-103">FreePrinterNotifyInfo function</span></span>

<span data-ttu-id="67c45-104">La fonction **FreePrinterNotifyInfo** libère une mémoire tampon allouée par le système créée par la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="67c45-104">The **FreePrinterNotifyInfo** function frees a system-allocated buffer created by the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="67c45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67c45-105">Syntax</span></span>


```C++
BOOL FreePrinterNotifyInfo(
  _In_ PPRINTER_NOTIFY_INFO pPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="67c45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67c45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67c45-107">*pPrinterNotifyInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67c45-107">*pPrinterNotifyInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67c45-108">Pointeur vers une mémoire tampon d' [**\_ \_ informations de notification**](printer-notify-info.md) de l’imprimante retournée par un appel à la fonction [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="67c45-108">Pointer to a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) buffer returned from a call to the [**FindNextPrinterChangeNotification**](findnextprinterchangenotification.md) function.</span></span> <span data-ttu-id="67c45-109">**FreePrinterNotifyInfo** libère cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="67c45-109">**FreePrinterNotifyInfo** deallocates this buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67c45-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67c45-110">Return value</span></span>

<span data-ttu-id="67c45-111">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="67c45-111">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="67c45-112">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="67c45-112">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="67c45-113">Notes</span><span class="sxs-lookup"><span data-stu-id="67c45-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="67c45-114">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="67c45-114">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="67c45-115">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="67c45-115">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="67c45-116">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="67c45-116">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="67c45-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67c45-117">Requirements</span></span>



| <span data-ttu-id="67c45-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67c45-118">Requirement</span></span> | <span data-ttu-id="67c45-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="67c45-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67c45-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67c45-120">Minimum supported client</span></span><br/> | <span data-ttu-id="67c45-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67c45-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="67c45-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67c45-122">Minimum supported server</span></span><br/> | <span data-ttu-id="67c45-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67c45-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="67c45-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="67c45-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="67c45-125"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67c45-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="67c45-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="67c45-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="67c45-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="67c45-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="67c45-128">DLL</span><span class="sxs-lookup"><span data-stu-id="67c45-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67c45-129"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67c45-129"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="67c45-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67c45-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67c45-131">Impression</span><span class="sxs-lookup"><span data-stu-id="67c45-131">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="67c45-132">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="67c45-132">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="67c45-133">**FindNextPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="67c45-133">**FindNextPrinterChangeNotification**</span></span>](findnextprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="67c45-134">**\_informations de notification de l’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="67c45-134">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> </dl>

 

 




