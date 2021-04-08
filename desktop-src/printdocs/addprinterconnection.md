---
description: La fonction AddPrinterConnection ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel.
ms.assetid: 6decf89a-1411-4e7e-aa20-60e7068658c2
title: AddPrinterConnection, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection
- AddPrinterConnectionA
- AddPrinterConnectionW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: dae1f823f89b69526218ab4c027642fb54e3cea5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866565"
---
# <a name="addprinterconnection-function"></a><span data-ttu-id="505b2-103">AddPrinterConnection fonction)</span><span class="sxs-lookup"><span data-stu-id="505b2-103">AddPrinterConnection function</span></span>

<span data-ttu-id="505b2-104">La fonction **AddPrinterConnection** ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel.</span><span class="sxs-lookup"><span data-stu-id="505b2-104">The **AddPrinterConnection** function adds a connection to the specified printer for the current user.</span></span>

## <a name="syntax"></a><span data-ttu-id="505b2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="505b2-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection(
  _In_ LPTSTR pName
);
```



## <a name="parameters"></a><span data-ttu-id="505b2-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="505b2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="505b2-107">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="505b2-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="505b2-108">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom d’une imprimante à laquelle l’utilisateur actuel souhaite établir une connexion.</span><span class="sxs-lookup"><span data-stu-id="505b2-108">A pointer to a null-terminated string that specifies the name of a printer to which the current user wishes to establish a connection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="505b2-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="505b2-109">Return value</span></span>

<span data-ttu-id="505b2-110">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="505b2-110">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="505b2-111">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="505b2-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="505b2-112">Notes</span><span class="sxs-lookup"><span data-stu-id="505b2-112">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="505b2-113">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="505b2-113">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="505b2-114">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="505b2-114">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="505b2-115">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="505b2-115">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="505b2-116">Lorsque Windows établit une connexion à une imprimante, il peut être nécessaire de copier les fichiers du pilote d’imprimante sur le serveur auquel l’imprimante est attachée.</span><span class="sxs-lookup"><span data-stu-id="505b2-116">When Windows makes a connection to a printer, it may need to copy printer driver files to the server to which the printer is attached.</span></span> <span data-ttu-id="505b2-117">Si l’utilisateur n’a pas l’autorisation de copier les fichiers vers l’emplacement approprié, la fonction **AddPrinterConnection** échoue et [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="505b2-117">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection** function fails, and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="505b2-118">Une connexion d’imprimante établie par l’appel de **AddPrinterConnection** est énumérée lorsque [**EnumPrinters**](enumprinters.md) est appelé avec *dwType* défini sur la connexion d’enum d’imprimante \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="505b2-118">A printer connection established by calling **AddPrinterConnection** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

## <a name="requirements"></a><span data-ttu-id="505b2-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="505b2-119">Requirements</span></span>



| <span data-ttu-id="505b2-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="505b2-120">Requirement</span></span> | <span data-ttu-id="505b2-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="505b2-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="505b2-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="505b2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="505b2-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="505b2-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="505b2-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="505b2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="505b2-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="505b2-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="505b2-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="505b2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="505b2-127"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="505b2-127"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="505b2-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="505b2-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="505b2-129"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="505b2-129"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="505b2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="505b2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="505b2-131"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="505b2-131"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="505b2-132">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="505b2-132">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="505b2-133">**AddPrinterConnectionW** (Unicode) et **AddPrinterConnectionA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="505b2-133">**AddPrinterConnectionW** (Unicode) and **AddPrinterConnectionA** (ANSI)</span></span><br/>                       |



## <a name="see-also"></a><span data-ttu-id="505b2-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="505b2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="505b2-135">Impression</span><span class="sxs-lookup"><span data-stu-id="505b2-135">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="505b2-136">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="505b2-136">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="505b2-137">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="505b2-137">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="505b2-138">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="505b2-138">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> <dt>

[<span data-ttu-id="505b2-139">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="505b2-139">**EnumPrinters**</span></span>](enumprinters.md)
</dt> </dl>

 

