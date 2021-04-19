---
description: Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel et spécifie les détails de connexion.
ms.assetid: 5ae98157-5978-449e-beb1-4787110925fa
title: AddPrinterConnection2, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterConnection2
- AddPrinterConnection2W
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: b24d5ddb25a43fae8576a042c4be6da8fd7cfef7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106520543"
---
# <a name="addprinterconnection2-function"></a><span data-ttu-id="ab574-103">AddPrinterConnection2 fonction)</span><span class="sxs-lookup"><span data-stu-id="ab574-103">AddPrinterConnection2 function</span></span>

<span data-ttu-id="ab574-104">Ajoute une connexion à l’imprimante spécifiée pour l’utilisateur actuel et spécifie les détails de connexion.</span><span class="sxs-lookup"><span data-stu-id="ab574-104">Adds a connection to the specified printer for the current user and specifies connection details.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab574-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ab574-105">Syntax</span></span>


```C++
BOOL AddPrinterConnection2(
  _In_ HWND    hWnd,
  _In_ LPCTSTR pszName,
       DWORD   dwLevel,
  _In_ PVOID   pConnectionInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ab574-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ab574-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab574-107">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab574-107">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab574-108">Handle de la fenêtre parente dans laquelle la boîte de dialogue s’affiche si le système d’impression doit télécharger un pilote d’imprimante à partir du serveur d’impression pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="ab574-108">A handle to the parent window in which the dialog box will be displayed if the print system must download a printer driver from the print server for this connection.</span></span>

</dd> <dt>

<span data-ttu-id="ab574-109">*pszName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab574-109">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab574-110">Pointeur vers une chaîne constante se terminant par un caractère null qui spécifie le nom de l’imprimante à laquelle l’utilisateur actuel souhaite se connecter.</span><span class="sxs-lookup"><span data-stu-id="ab574-110">A pointer to a constant null-terminated string specifying the name of the printer to which the current user wishes to connect.</span></span>

</dd> <dt>

<span data-ttu-id="ab574-111">*dwLevel*</span><span class="sxs-lookup"><span data-stu-id="ab574-111">*dwLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="ab574-112">Version de la structure vers laquelle pointe *pConnectionInfo*.</span><span class="sxs-lookup"><span data-stu-id="ab574-112">The version of the structure pointed to by *pConnectionInfo*.</span></span> <span data-ttu-id="ab574-113">Actuellement, seul le niveau 1 est défini, de sorte que la valeur de *dwLevel* doit être 1.</span><span class="sxs-lookup"><span data-stu-id="ab574-113">Currently, only level 1 is defined so the value of *dwLevel* must be 1.</span></span>

</dd> <dt>

<span data-ttu-id="ab574-114">*pConnectionInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ab574-114">*pConnectionInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab574-115">Pointeur vers une structure [**d' \_ informations de connexion d’imprimante \_ \_ 1**](printer-connection-info-1.md) .</span><span class="sxs-lookup"><span data-stu-id="ab574-115">A pointer to a [**PRINTER\_CONNECTION\_INFO\_1**](printer-connection-info-1.md) structure.</span></span> <span data-ttu-id="ab574-116">Pour plus d’informations sur ce paramètre, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ab574-116">See the Remarks section for more about this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab574-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ab574-117">Return value</span></span>

<span data-ttu-id="ab574-118">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ab574-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="ab574-119">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ab574-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="ab574-120">Pour obtenir des informations d’erreur étendues, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="ab574-120">For extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="ab574-121">Notes</span><span class="sxs-lookup"><span data-stu-id="ab574-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ab574-122">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="ab574-122">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="ab574-123">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="ab574-123">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="ab574-124">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="ab574-124">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="ab574-125">Lorsque Windows Vista établit une connexion à une imprimante, il peut être nécessaire de copier les fichiers du pilote d’imprimante à partir du serveur auquel l’imprimante est attachée.</span><span class="sxs-lookup"><span data-stu-id="ab574-125">When Windows Vista makes a connection to a printer, it may need to copy printer driver files from the server to which the printer is attached.</span></span> <span data-ttu-id="ab574-126">Si l’utilisateur n’a pas l’autorisation de copier les fichiers vers l’emplacement approprié, la fonction **AddPrinterConnection2** échoue et [**GETLASTERROR**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) retourne l’erreur \_ accès \_ refusé.</span><span class="sxs-lookup"><span data-stu-id="ab574-126">If the user does not have permission to copy files to the appropriate location, the **AddPrinterConnection2** function fails and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_ACCESS\_DENIED.</span></span>

<span data-ttu-id="ab574-127">Si les fichiers de pilote d’imprimante doivent être copiés à partir du serveur d’impression mais ne peuvent pas être copiés en mode silencieux en raison des stratégies de groupe en vigueur et de la connexion à l’imprimante, \_ \_ aucune \_ interface utilisateur n’est définie dans *pConnectionInfo->dwFlags*, aucune boîte de dialogue ne s’affiche et l’appel échoue.</span><span class="sxs-lookup"><span data-stu-id="ab574-127">If the printer driver files must be copied from the print server but cannot be copied silently due to the group policies that are in effect and PRINTER\_CONNECTION\_NO\_UI is set in *pConnectionInfo->dwFlags*, no dialog boxes will be displayed and the call will fail.</span></span>

<span data-ttu-id="ab574-128">Si le pilote d’imprimante locale peut être utilisé pour afficher les travaux d’impression pour cette imprimante et que la version du pilote local ne doit pas correspondre à la version du pilote d’imprimante sur le serveur, définissez \_ incompatibilité de connexion d’imprimante \_ dans *PConnectionInfo->dwFlags* et affectez le pointeur à une variable de chaîne qui contient le chemin d’accès au pilote d’imprimante locale pour *pConnectionInfo->pszDriverName*.</span><span class="sxs-lookup"><span data-stu-id="ab574-128">If the local printer driver can be used to render print jobs for this printer and the version of the local driver must not match the version of the printer driver on the server, set PRINTER\_CONNECTION\_MISMATCH in *pConnectionInfo->dwFlags* and assign the pointer to a string variable that contains the path to the local printer driver to *pConnectionInfo->pszDriverName*.</span></span>

<span data-ttu-id="ab574-129">Une connexion d’imprimante établie par l’appel de **AddPrinterConnection2** est énumérée lorsque [**EnumPrinters**](enumprinters.md) est appelé avec *dwType* défini sur la \_ connexion d’enum d’imprimante \_ .</span><span class="sxs-lookup"><span data-stu-id="ab574-129">A printer connection that is established by calling **AddPrinterConnection2** will be enumerated when [**EnumPrinters**](enumprinters.md) is called with *dwType* set to PRINTER\_ENUM\_CONNECTION.</span></span>

<span data-ttu-id="ab574-130">La version ANSI de cette fonction, **AddPrinterConnection2A**, n’est pas prise en charge et retourne une **erreur \_ non \_ prise en charge**.</span><span class="sxs-lookup"><span data-stu-id="ab574-130">The ANSI version of this function, **AddPrinterConnection2A**, is not supported and returns **ERROR\_NOT\_SUPPORTED**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab574-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ab574-131">Requirements</span></span>



| <span data-ttu-id="ab574-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ab574-132">Requirement</span></span> | <span data-ttu-id="ab574-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="ab574-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab574-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab574-134">Minimum supported client</span></span><br/> | <span data-ttu-id="ab574-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab574-135">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="ab574-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ab574-136">Minimum supported server</span></span><br/> | <span data-ttu-id="ab574-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ab574-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ab574-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="ab574-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab574-139"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab574-139"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="ab574-140">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ab574-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab574-141"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab574-141"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="ab574-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ab574-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab574-143"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="ab574-143"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="ab574-144">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="ab574-144">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="ab574-145">**AddPrinterConnection2W** (Unicode)</span><span class="sxs-lookup"><span data-stu-id="ab574-145">**AddPrinterConnection2W** (Unicode)</span></span><br/>                                                           |



## <a name="see-also"></a><span data-ttu-id="ab574-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ab574-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab574-147">Impression</span><span class="sxs-lookup"><span data-stu-id="ab574-147">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="ab574-148">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="ab574-148">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="ab574-149">**ConnectToPrinterDlg**</span><span class="sxs-lookup"><span data-stu-id="ab574-149">**ConnectToPrinterDlg**</span></span>](connecttoprinterdlg.md)
</dt> <dt>

[<span data-ttu-id="ab574-150">**EnumPrinters**</span><span class="sxs-lookup"><span data-stu-id="ab574-150">**EnumPrinters**</span></span>](enumprinters.md)
</dt> <dt>

[<span data-ttu-id="ab574-151">**DeletePrinterConnection**</span><span class="sxs-lookup"><span data-stu-id="ab574-151">**DeletePrinterConnection**</span></span>](deleteprinterconnection.md)
</dt> </dl>

 

