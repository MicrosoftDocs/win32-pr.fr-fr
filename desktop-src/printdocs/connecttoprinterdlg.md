---
description: La fonction ConnectToPrinterDlg affiche une boîte de dialogue qui permet aux utilisateurs de parcourir les imprimantes et de s’y connecter sur un réseau.
ms.assetid: 7cb9108b-8b65-4af3-88c8-a69771ed8e3f
title: ConnectToPrinterDlg, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConnectToPrinterDlg
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: 9af428533d111300d31f6529a0a030fc3b81ee7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521962"
---
# <a name="connecttoprinterdlg-function"></a><span data-ttu-id="e4ae5-103">ConnectToPrinterDlg fonction)</span><span class="sxs-lookup"><span data-stu-id="e4ae5-103">ConnectToPrinterDlg function</span></span>

<span data-ttu-id="e4ae5-104">La fonction **ConnectToPrinterDlg** affiche une boîte de dialogue qui permet aux utilisateurs de parcourir les imprimantes et de s’y connecter sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-104">The **ConnectToPrinterDlg** function displays a dialog box that lets users browse and connect to printers on a network.</span></span> <span data-ttu-id="e4ae5-105">Si l’utilisateur sélectionne une imprimante, la fonction tente de créer une connexion à celle-ci ; Si aucun pilote approprié n’est installé sur le serveur, l’utilisateur a la possibilité de créer une imprimante localement.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-105">If the user selects a printer, the function attempts to create a connection to it; if a suitable driver is not installed on the server, the user is given the option of creating a printer locally.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4ae5-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e4ae5-106">Syntax</span></span>


```C++
HANDLE ConnectToPrinterDlg(
  _In_ HWND  hwnd,
  _In_ DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="e4ae5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e4ae5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4ae5-108">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e4ae5-108">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ae5-109">Spécifie la fenêtre parente de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-109">Specifies the parent window of the dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="e4ae5-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="e4ae5-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4ae5-111">Ce paramètre est réservé et doit être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-111">This parameter is reserved and must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4ae5-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e4ae5-112">Return value</span></span>

<span data-ttu-id="e4ae5-113">Si la fonction s’exécute correctement et que l’utilisateur sélectionne une imprimante, la valeur de retour est un handle vers l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-113">If the function succeeds and the user selects a printer, the return value is a handle to the selected printer.</span></span>

<span data-ttu-id="e4ae5-114">Si la fonction échoue, ou si l’utilisateur annule la boîte de dialogue sans sélectionner d’imprimante, la valeur de retour est **null**.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-114">If the function fails, or the user cancels the dialog box without selecting a printer, the return value is **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4ae5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="e4ae5-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="e4ae5-116">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-116">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="e4ae5-117">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-117">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="e4ae5-118">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-118">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="e4ae5-119">La fonction **ConnectToPrinterDlg** tente de créer une connexion à l’imprimante sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-119">The **ConnectToPrinterDlg** function attempts to create a connection to the selected printer.</span></span> <span data-ttu-id="e4ae5-120">Toutefois, si le serveur sur lequel l’imprimante réside n’a pas de pilote approprié installé, la fonction offre à l’utilisateur la possibilité de créer une imprimante localement.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-120">However, if the server on which the printer resides does not have a suitable driver installed, the function offers the user the option of creating a printer locally.</span></span> <span data-ttu-id="e4ae5-121">Une application appelante peut déterminer si la fonction a créé une imprimante localement en appelant [**GetPrinter**](getprinter.md) avec une structure [**Printer \_ info \_ 2**](printer-info-2.md) , puis en examinant le membre des **attributs** de cette structure.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-121">A calling application can determine whether the function has created a printer locally by calling [**GetPrinter**](getprinter.md) with a [**PRINTER\_INFO\_2**](printer-info-2.md) structure, then examining that structure's **Attributes** member.</span></span>

<span data-ttu-id="e4ae5-122">Une application doit appeler [**DeletePrinter**](deleteprinter.md) pour supprimer une imprimante locale.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-122">An application should call [**DeletePrinter**](deleteprinter.md) to delete a local printer.</span></span> <span data-ttu-id="e4ae5-123">Une application doit appeler [**DeletePrinterConnection**](deleteprinterconnection.md) pour supprimer une connexion à une imprimante.</span><span class="sxs-lookup"><span data-stu-id="e4ae5-123">An application should call [**DeletePrinterConnection**](deleteprinterconnection.md) to delete a connection to a printer.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4ae5-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e4ae5-124">Requirements</span></span>



| <span data-ttu-id="e4ae5-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e4ae5-125">Requirement</span></span> | <span data-ttu-id="e4ae5-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e4ae5-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4ae5-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4ae5-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e4ae5-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4ae5-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e4ae5-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e4ae5-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e4ae5-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e4ae5-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e4ae5-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="e4ae5-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4ae5-132"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4ae5-132"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="e4ae5-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e4ae5-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="e4ae5-134"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e4ae5-134"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="e4ae5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="e4ae5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4ae5-136"><dt>WinSpool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="e4ae5-136"><dt>WinSpool.drv</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="e4ae5-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e4ae5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4ae5-138">Impression</span><span class="sxs-lookup"><span data-stu-id="e4ae5-138">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-139">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="e4ae5-139">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-140">**AddPrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-140">**AddPrinterConnection**</span></span>](addprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-141">**ClosePrinter**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-141">**ClosePrinter**</span></span>](closeprinter.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-142">**DeletePrinter**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-142">**DeletePrinter**</span></span>](deleteprinter.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-143">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-143">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-144">**GetPrinter**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-144">**GetPrinter**</span></span>](getprinter.md)
</dt> <dt>

[<span data-ttu-id="e4ae5-145">**\_Infos sur l’imprimante \_ 2**</span><span class="sxs-lookup"><span data-stu-id="e4ae5-145">**PRINTER\_INFO\_2**</span></span>](printer-info-2.md)
</dt> </dl>

 

 




