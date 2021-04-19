---
description: La fonction DeletePrinterConnection supprime une connexion à une imprimante qui a été établie par un appel à AddPrinterConnection ou ConnectToPrinterDlg.
ms.assetid: 7b056eea-fbd9-4a08-a2dc-7326caeec387
title: DeletePrinterConnection, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePrinterConnection
- DeletePrinterConnectionA
- DeletePrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c524e3bcc79efc2207839b3d3a95051e2eb8bae5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535554"
---
# <a name="deleteprinterconnection-function"></a><span data-ttu-id="dfc7d-103">DeletePrinterConnection fonction)</span><span class="sxs-lookup"><span data-stu-id="dfc7d-103">DeletePrinterConnection function</span></span>

<span data-ttu-id="dfc7d-104">La fonction **DeletePrinterConnection** supprime une connexion à une imprimante qui a été établie par un appel à [**AddPrinterConnection**](addprinterconnection.md) ou [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span><span class="sxs-lookup"><span data-stu-id="dfc7d-104">The **DeletePrinterConnection** function deletes a connection to a printer that was established by a call to [**AddPrinterConnection**](addprinterconnection.md) or [**ConnectToPrinterDlg**](connecttoprinterdlg.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="dfc7d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dfc7d-105">Syntax</span></span>


```C++
BOOL DeletePrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="dfc7d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dfc7d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dfc7d-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dfc7d-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dfc7d-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom de la connexion d’imprimante à supprimer.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-108">Pointer to a null-terminated string that specifies the name of the printer connection to delete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dfc7d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dfc7d-109">Return value</span></span>

<span data-ttu-id="dfc7d-110">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="dfc7d-111">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dfc7d-112">Notes</span><span class="sxs-lookup"><span data-stu-id="dfc7d-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="dfc7d-113">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="dfc7d-114">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="dfc7d-115">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="dfc7d-116">La fonction **DeletePrinterConnection** ne supprime pas les fichiers de pilote d’imprimante qui ont été copiés sur le serveur auquel l’imprimante est attachée.</span><span class="sxs-lookup"><span data-stu-id="dfc7d-116">The **DeletePrinterConnection** function does not delete any printer driver files that were copied to the server to which the printer is attached.</span></span>

## <a name="requirements"></a><span data-ttu-id="dfc7d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dfc7d-117">Requirements</span></span>



| <span data-ttu-id="dfc7d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dfc7d-118">Requirement</span></span> | <span data-ttu-id="dfc7d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="dfc7d-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfc7d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfc7d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="dfc7d-121">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfc7d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="dfc7d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dfc7d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="dfc7d-123">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dfc7d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="dfc7d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="dfc7d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="dfc7d-125"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7d-125"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="dfc7d-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="dfc7d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="dfc7d-127"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7d-127"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="dfc7d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dfc7d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dfc7d-129"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="dfc7d-129"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="dfc7d-130">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="dfc7d-130">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dfc7d-131">**DeletePrinterConnectionW** (Unicode) et **DeletePrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="dfc7d-131">**DeletePrinterConnectionW** (Unicode) and **DeletePrinterConnectionA** (ANSI)</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="dfc7d-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dfc7d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dfc7d-133">Impression</span><span class="sxs-lookup"><span data-stu-id="dfc7d-133">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="dfc7d-134">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="dfc7d-134">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="dfc7d-135">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="dfc7d-135">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="dfc7d-136">**AddPrinterConnection2**</span><span class="sxs-lookup"><span data-stu-id="dfc7d-136">**AddPrinterConnection2**</span></span>](addprinterconnection2.md)
</dt> <dt>

[<span data-ttu-id="dfc7d-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="dfc7d-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> </dl>

 

 




