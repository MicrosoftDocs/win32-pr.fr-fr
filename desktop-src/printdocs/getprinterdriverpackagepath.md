---
description: Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.
ms.assetid: e88e984b-d2c0-43b4-8f70-b05ec202ab14
title: GetPrinterDriverPackagePath, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrinterDriverPackagePath
- GetPrinterDriverPackagePathA
- GetPrinterDriverPackagePathW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ea355782df6cce7910f92a46af3cde320536106e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529441"
---
# <a name="getprinterdriverpackagepath-function"></a><span data-ttu-id="c9979-103">GetPrinterDriverPackagePath fonction)</span><span class="sxs-lookup"><span data-stu-id="c9979-103">GetPrinterDriverPackagePath function</span></span>

<span data-ttu-id="c9979-104">Récupère le chemin d’accès au package de pilotes d’imprimante spécifié sur un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="c9979-104">Retrieves the path to the specified printer driver package on a print server.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9979-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9979-105">Syntax</span></span>


```C++
HRESULT GetPrinterDriverPackagePath(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszEnvironment,
  _In_    LPCTSTR pszLanguage,
  _In_    LPCTSTR pszPackageID,
  _Inout_ LPTSTR  pszDriverPackageCab,
  _In_    DWORD   cchDriverPackageCab,
  _Out_   LPDWORD pcchRequiredSize
);
```



## <a name="parameters"></a><span data-ttu-id="c9979-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9979-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9979-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9979-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-108">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="c9979-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="c9979-109">Utilisez la **valeur null** pour l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="c9979-109">Use **NULL** for the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-110">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9979-110">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-111">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="c9979-111">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="c9979-112">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9979-112">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-113">*pszLanguage* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9979-113">*pszLanguage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-114">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie la langue de l' [interface utilisateur multilingue](/windows/desktop/Intl/mui-resource-management) pour le pilote en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="c9979-114">A pointer to a constant, null-terminated string that specifies the [Multilingual User Interface](/windows/desktop/Intl/mui-resource-management) language for the driver being installed.</span></span> <span data-ttu-id="c9979-115">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9979-115">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-116">*pszPackageID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9979-116">*pszPackageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-117">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’ID du package de pilotes.</span><span class="sxs-lookup"><span data-stu-id="c9979-117">A pointer to a constant, null-terminated string that specifies the ID of the driver package.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-118">*pszDriverPackageCab* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="c9979-118">*pszDriverPackageCab* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-119">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le chemin d’accès au fichier CAB pour le package de pilotes.</span><span class="sxs-lookup"><span data-stu-id="c9979-119">A pointer to a null-terminated string that specifies the path to the cabinet file for the driver package.</span></span> <span data-ttu-id="c9979-120">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9979-120">This can be **NULL**.</span></span> <span data-ttu-id="c9979-121">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c9979-121">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-122">*cchDriverPackageCab* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9979-122">*cchDriverPackageCab* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-123">Taille, en caractères, de la mémoire tampon *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="c9979-123">The size, in characters, of the *pszDriverPackageCab* buffer.</span></span> <span data-ttu-id="c9979-124">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="c9979-124">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="c9979-125">*pcchRequiredSize* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9979-125">*pcchRequiredSize* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9979-126">Pointeur vers la taille requise de la mémoire tampon *pszDriverPackageCab* .</span><span class="sxs-lookup"><span data-stu-id="c9979-126">A pointer to the required size of the *pszDriverPackageCab* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9979-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9979-127">Return value</span></span>

<span data-ttu-id="c9979-128">Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="c9979-128">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="c9979-129">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="c9979-129">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c9979-130">Notes</span><span class="sxs-lookup"><span data-stu-id="c9979-130">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c9979-131">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="c9979-131">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="c9979-132">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="c9979-132">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="c9979-133">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="c9979-133">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="c9979-134">Pour obtenir une valeur pour *cchDriverPackageCab*, appelez la fonction avec **null** comme valeur de *pszDriverPackageCab*.</span><span class="sxs-lookup"><span data-stu-id="c9979-134">To obtain a value for *cchDriverPackageCab*, call the function with **NULL** as the value of *pszDriverPackageCab*.</span></span> <span data-ttu-id="c9979-135">Utilisez la valeur retournée dans *pcchRequiredSize* comme valeur de *cchDriverPackageCab* et appelez à nouveau la fonction.</span><span class="sxs-lookup"><span data-stu-id="c9979-135">Use the value returned in *pcchRequiredSize* as the value of *cchDriverPackageCab* and call the function again.</span></span>

<span data-ttu-id="c9979-136">Le *pszPackageID* est généralement obtenu à partir d’un appel à [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span><span class="sxs-lookup"><span data-stu-id="c9979-136">The *pszPackageID* is typically obtained from a call to [**GetCorePrinterDrivers**](getcoreprinterdrivers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c9979-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9979-137">Requirements</span></span>



| <span data-ttu-id="c9979-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9979-138">Requirement</span></span> | <span data-ttu-id="c9979-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9979-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9979-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9979-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c9979-141">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9979-141">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="c9979-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9979-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c9979-143">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9979-143">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c9979-144">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9979-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9979-145"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c9979-145"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="c9979-146">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c9979-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="c9979-147"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c9979-147"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="c9979-148">DLL</span><span class="sxs-lookup"><span data-stu-id="c9979-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9979-149"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9979-149"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="c9979-150">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="c9979-150">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="c9979-151">**GetPrinterDriverPackagePathW** (Unicode) et **GetPrinterDriverPackagePathA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="c9979-151">**GetPrinterDriverPackagePathW** (Unicode) and **GetPrinterDriverPackagePathA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c9979-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9979-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9979-153">Impression</span><span class="sxs-lookup"><span data-stu-id="c9979-153">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="c9979-154">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="c9979-154">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

