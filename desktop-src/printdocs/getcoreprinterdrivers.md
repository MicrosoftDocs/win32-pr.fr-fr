---
description: Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.
ms.assetid: 98acad48-cd42-4d2b-be58-81c1366f6912
title: GetCorePrinterDrivers, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCorePrinterDrivers
- GetCorePrinterDriversA
- GetCorePrinterDriversW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 5bdebc3f4b716a21c56c9ec756ff56c02765d1a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319090"
---
# <a name="getcoreprinterdrivers-function"></a><span data-ttu-id="15e25-103">GetCorePrinterDrivers fonction)</span><span class="sxs-lookup"><span data-stu-id="15e25-103">GetCorePrinterDrivers function</span></span>

<span data-ttu-id="15e25-104">Récupère le GUID, la version et la date des pilotes d’imprimante principaux spécifiés et le chemin d’accès à leurs packages.</span><span class="sxs-lookup"><span data-stu-id="15e25-104">Retrieves GUID, version, and date of the specified core printer drivers and the path to their packages.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e25-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="15e25-105">Syntax</span></span>


```C++
HRESULT GetCorePrinterDrivers(
  _In_  LPCTSTR              pszServer,
  _In_  LPCTSTR              pszEnvironment,
  _In_  LPCTSTR              pszzCoreDriverDependencies,
  _In_  DWORD                cCorePrinterDrivers,
  _Out_ PCORE_PRINTER_DRIVER pCorePrinterDrivers
);
```



## <a name="parameters"></a><span data-ttu-id="15e25-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="15e25-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15e25-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15e25-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e25-108">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="15e25-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="15e25-109">Utilisez la **valeur null** pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="15e25-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="15e25-110">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15e25-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e25-111">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="15e25-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="15e25-112">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="15e25-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="15e25-113">*pszzCoreDriverDependencies* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15e25-113">*pszzCoreDriverDependencies* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e25-114">Pointeur vers une chaîne multiple se terminant par un caractère null qui spécifie les GUID des pilotes d’imprimante principaux.</span><span class="sxs-lookup"><span data-stu-id="15e25-114">A pointer to a null-terminated multi-string that specifies the GUIDs of the core printer drivers.</span></span>

</dd> <dt>

<span data-ttu-id="15e25-115">*cCorePrinterDrivers* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="15e25-115">*cCorePrinterDrivers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15e25-116">Nombre de chaînes dans *pszzCoreDriverDependencies*.</span><span class="sxs-lookup"><span data-stu-id="15e25-116">The number of strings in *pszzCoreDriverDependencies*.</span></span>

</dd> <dt>

<span data-ttu-id="15e25-117">*pCorePrinterDrivers* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="15e25-117">*pCorePrinterDrivers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="15e25-118">Pointeur vers un tableau d’une ou de plusieurs structures de [**\_ \_ pilote d’imprimante principale**](core-printer-driver.md) .</span><span class="sxs-lookup"><span data-stu-id="15e25-118">A pointer to an array of one or more [**CORE\_PRINTER\_DRIVER**](core-printer-driver.md) structures.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15e25-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="15e25-119">Return value</span></span>

<span data-ttu-id="15e25-120">Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="15e25-120">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="15e25-121">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="15e25-121">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="15e25-122">Notes</span><span class="sxs-lookup"><span data-stu-id="15e25-122">Remarks</span></span>

<span data-ttu-id="15e25-123">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="15e25-123">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="15e25-124">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="15e25-124">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="15e25-125">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="15e25-125">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e25-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="15e25-126">Requirements</span></span>



| <span data-ttu-id="15e25-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="15e25-127">Requirement</span></span> | <span data-ttu-id="15e25-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="15e25-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="15e25-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e25-129">Minimum supported client</span></span><br/> | <span data-ttu-id="15e25-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15e25-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="15e25-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="15e25-131">Minimum supported server</span></span><br/> | <span data-ttu-id="15e25-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="15e25-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="15e25-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="15e25-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="15e25-134"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="15e25-134"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="15e25-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="15e25-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="15e25-136"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="15e25-136"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="15e25-137">DLL</span><span class="sxs-lookup"><span data-stu-id="15e25-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15e25-138"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e25-138"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="15e25-139">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="15e25-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="15e25-140">**GetCorePrinterDriversW** (Unicode) et **GetCorePrinterDriversA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="15e25-140">**GetCorePrinterDriversW** (Unicode) and **GetCorePrinterDriversA** (ANSI)</span></span><br/>                     |



## <a name="see-also"></a><span data-ttu-id="15e25-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="15e25-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15e25-142">Impression</span><span class="sxs-lookup"><span data-stu-id="15e25-142">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="15e25-143">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="15e25-143">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

