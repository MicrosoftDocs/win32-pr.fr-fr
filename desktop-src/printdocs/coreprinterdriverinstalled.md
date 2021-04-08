---
description: La fonction CorePrinterDriverInstalled indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.
ms.assetid: fb859aca-bb7b-495d-bd38-16ffa084c240
title: CorePrinterDriverInstalled, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CorePrinterDriverInstalled
- CorePrinterDriverInstalledA
- CorePrinterDriverInstalledW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 2e4f7033e5ca15a892a208621049c2f500873d73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034886"
---
# <a name="coreprinterdriverinstalled-function"></a><span data-ttu-id="54d45-103">CorePrinterDriverInstalled fonction)</span><span class="sxs-lookup"><span data-stu-id="54d45-103">CorePrinterDriverInstalled function</span></span>

<span data-ttu-id="54d45-104">La fonction **CorePrinterDriverInstalled** indique si un pilote d’imprimante principal avec un GUID, une date et une version spécifiés est installé.</span><span class="sxs-lookup"><span data-stu-id="54d45-104">The **CorePrinterDriverInstalled** function reports whether a core printer driver with a specified GUID, date, and version is installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="54d45-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54d45-105">Syntax</span></span>


```C++
HRESULT CorePrinterDriverInstalled(
  _In_  LPCTSTR   pszServer,
  _In_  LPCTSTR   pszEnvironment,
  _In_  GUID      CoreDriverGUID,
  _In_  FILETIME  ftDriverDate,
  _In_  DWORDLONG dwlDriverVersion,
  _Out_ BOOL      *pbDriverInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="54d45-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="54d45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54d45-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54d45-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-108">Pointeur vers une constante, chaîne terminée par le caractère null qui spécifie le nom du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="54d45-108">Pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="54d45-109">Utilisez la **valeur null** pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="54d45-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="54d45-110">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54d45-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-111">Pointeur vers une chaîne constante, terminée par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="54d45-111">Pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="54d45-112">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="54d45-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="54d45-113">*CoreDriverGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54d45-113">*CoreDriverGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-114">GUID du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="54d45-114">The GUID of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="54d45-115">*ftDriverDate* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54d45-115">*ftDriverDate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-116">Date du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="54d45-116">The date of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="54d45-117">*dwlDriverVersion* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="54d45-117">*dwlDriverVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-118">Version du pilote d’imprimante principal.</span><span class="sxs-lookup"><span data-stu-id="54d45-118">The version of the core printer driver.</span></span>

</dd> <dt>

<span data-ttu-id="54d45-119">*pbDriverInstalled* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="54d45-119">*pbDriverInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="54d45-120">Pointeur vers **true** si le pilote, ou une version plus récente, est installé ; sinon, **false** .</span><span class="sxs-lookup"><span data-stu-id="54d45-120">A pointer to **TRUE** if the driver, or a newer version, is installed, **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54d45-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="54d45-121">Return value</span></span>

<span data-ttu-id="54d45-122">Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="54d45-122">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="54d45-123">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="54d45-123">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54d45-124">Notes</span><span class="sxs-lookup"><span data-stu-id="54d45-124">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="54d45-125">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="54d45-125">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="54d45-126">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="54d45-126">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="54d45-127">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="54d45-127">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="54d45-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54d45-128">Requirements</span></span>



| <span data-ttu-id="54d45-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54d45-129">Requirement</span></span> | <span data-ttu-id="54d45-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="54d45-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="54d45-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d45-131">Minimum supported client</span></span><br/> | <span data-ttu-id="54d45-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d45-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="54d45-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54d45-133">Minimum supported server</span></span><br/> | <span data-ttu-id="54d45-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54d45-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="54d45-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="54d45-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="54d45-136"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="54d45-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="54d45-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="54d45-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="54d45-138"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54d45-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="54d45-139">DLL</span><span class="sxs-lookup"><span data-stu-id="54d45-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54d45-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54d45-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="54d45-141">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="54d45-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="54d45-142">**CorePrinterDriverInstalledW** (Unicode) et **CorePrinterDriverInstalledA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="54d45-142">**CorePrinterDriverInstalledW** (Unicode) and **CorePrinterDriverInstalledA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="54d45-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54d45-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54d45-144">Impression</span><span class="sxs-lookup"><span data-stu-id="54d45-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="54d45-145">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="54d45-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

