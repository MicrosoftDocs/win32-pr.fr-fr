---
description: Charge un pilote d’imprimante dans le magasin de pilotes des serveurs d’impression afin qu’il puisse être installé en appelant InstallPrinterDriverFromPackage.
ms.assetid: dd3b3a3b-8ded-44ae-85dd-e630bc62e898
title: UploadPrinterDriverPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UploadPrinterDriverPackage
- UploadPrinterDriverPackageA
- UploadPrinterDriverPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f616c4f731d3a416806f499a513f48466263f441
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210085"
---
# <a name="uploadprinterdriverpackage-function"></a><span data-ttu-id="4a697-103">UploadPrinterDriverPackage fonction)</span><span class="sxs-lookup"><span data-stu-id="4a697-103">UploadPrinterDriverPackage function</span></span>

<span data-ttu-id="4a697-104">Charge un pilote d’imprimante sur le magasin de pilotes du serveur d’impression afin qu’il puisse être installé en appelant [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span><span class="sxs-lookup"><span data-stu-id="4a697-104">Uploads a printer driver to the print server's driver store so that it can be installed by calling [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="4a697-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4a697-105">Syntax</span></span>


```C++
HRESULT UploadPrinterDriverPackage(
  _In_    LPCTSTR pszServer,
  _In_    LPCTSTR pszInfPath,
  _In_    LPCTSTR pszEnvironment,
  _In_    DWORD   dwFlags,
  _In_    HWND    hwnd,
  _Out_   LPTSTR  pszDestInfPath,
  _Inout_ PULONG  pcchDestInfPath
);
```



## <a name="parameters"></a><span data-ttu-id="4a697-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4a697-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a697-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a697-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-108">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="4a697-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="4a697-109">Utilisez la **valeur null** si le serveur est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="4a697-109">Use **NULL** if the server is the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="4a697-110">*pszInfPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a697-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-111">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès source au fichier. inf du pilote.</span><span class="sxs-lookup"><span data-stu-id="4a697-111">A pointer to a constant ,null-terminated string that specifies the source path to the driver's .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="4a697-112">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a697-112">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-113">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur du serveur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="4a697-113">A pointer to a constant, null-terminated string that specifies the server's processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="4a697-114">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="4a697-114">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4a697-115">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a697-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-116">Il peut s’agir de l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="4a697-116">This can be any of the following values:</span></span>



| <span data-ttu-id="4a697-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a697-117">Value</span></span>                                                                                                                                                                                     | <span data-ttu-id="4a697-118">Signification</span><span class="sxs-lookup"><span data-stu-id="4a697-118">Meaning</span></span>                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UPDP_SILENT_UPLOAD"></span><span id="updp_silent_upload"></span><dl> <span data-ttu-id="4a697-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-119"><dt>**UPDP_SILENT_UPLOAD**</dt></span></span> </dl>             | <span data-ttu-id="4a697-120">L’interface utilisateur ne sera pas affichée pendant le téléchargement.</span><span class="sxs-lookup"><span data-stu-id="4a697-120">The UI will not be shown during the upload.</span></span><br/>                                                                                                             |
| <span id="UPDP_UPLOAD_ALWAYS"></span><span id="updp_upload_always"></span><dl> <span data-ttu-id="4a697-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-121"><dt>**UPDP_UPLOAD_ALWAYS**</dt></span></span> </dl>             | <span data-ttu-id="4a697-122">Les fichiers sont téléchargés même si le package est déjà dans le magasin de pilotes du serveur.</span><span class="sxs-lookup"><span data-stu-id="4a697-122">The files will be uploaded even if the package is already in the server's driver store.</span></span><br/>                                                                 |
| <span id="UPDP_CHECK_DRIVERSTORE"></span><span id="updp_check_driverstore"></span><dl> <span data-ttu-id="4a697-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-123"><dt>**UPDP_CHECK_DRIVERSTORE**</dt></span></span> </dl> | <span data-ttu-id="4a697-124">Le magasin de pilotes du serveur sera vérifié avant le chargement pour voir si le package existe déjà.</span><span class="sxs-lookup"><span data-stu-id="4a697-124">The server's driver store will be checked before upload to see if the package is already there.</span></span> <span data-ttu-id="4a697-125">Ce paramètre est ignoré si UPDP_UPLOAD_ALWAYS est défini.</span><span class="sxs-lookup"><span data-stu-id="4a697-125">This setting is ignored if UPDP_UPLOAD_ALWAYS is set.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="4a697-126">*HWND* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4a697-126">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-127">Handle de l’interface utilisateur de copie.</span><span class="sxs-lookup"><span data-stu-id="4a697-127">A handle to the copying user interface.</span></span>

</dd> <dt>

<span data-ttu-id="4a697-128">*pszDestInfPath* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4a697-128">*pszDestInfPath* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-129">Pointeur vers le chemin d’accès de destination, dans le magasin de pilotes, dans lequel le fichier. inf du pilote a été copié.</span><span class="sxs-lookup"><span data-stu-id="4a697-129">A pointer to the destination path, in the driver store, to which the driver's .inf file was copied.</span></span>

</dd> <dt>

<span data-ttu-id="4a697-130">*pcchDestInfPath* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4a697-130">*pcchDestInfPath* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4a697-131">En entrée, spécifie la taille, en caractères, de la mémoire tampon *pszDestInfPath* .</span><span class="sxs-lookup"><span data-stu-id="4a697-131">On input, specifies the size, in characters, of the *pszDestInfPath* buffer.</span></span> <span data-ttu-id="4a697-132">Lors de la sortie, reçoit la taille, en caractères, de la chaîne de chemin d’accès, y compris le caractère null de fin.</span><span class="sxs-lookup"><span data-stu-id="4a697-132">On output, receives the size, in characters, of the path string, including the terminating null character.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a697-133">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4a697-133">Return value</span></span>

<span data-ttu-id="4a697-134">Si l’opération a échoué, la valeur de retour est S_OK ; sinon, le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="4a697-134">If the operation succeeds, the return value is S_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="4a697-135">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="4a697-135">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4a697-136">Notes</span><span class="sxs-lookup"><span data-stu-id="4a697-136">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4a697-137">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="4a697-137">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4a697-138">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="4a697-138">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4a697-139">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="4a697-139">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4a697-140">Le magasin de pilotes est généralement% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="4a697-140">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="4a697-141">Un seul package à la fois peut être téléchargé.</span><span class="sxs-lookup"><span data-stu-id="4a697-141">Only one package at a time can be uploaded.</span></span> <span data-ttu-id="4a697-142">Si un package dépend d’autres, il doit être téléchargé séparément.</span><span class="sxs-lookup"><span data-stu-id="4a697-142">If a package is dependent on others, they must be uploaded separately.</span></span>

<span data-ttu-id="4a697-143">Seuls les packages de pilotes signés peuvent être téléchargés.</span><span class="sxs-lookup"><span data-stu-id="4a697-143">Only signed driver packages can be uploaded.</span></span>

## <a name="requirements"></a><span data-ttu-id="4a697-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4a697-144">Requirements</span></span>



| <span data-ttu-id="4a697-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4a697-145">Requirement</span></span> | <span data-ttu-id="4a697-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a697-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a697-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a697-147">Minimum supported client</span></span><br/> | <span data-ttu-id="4a697-148">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a697-148">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="4a697-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4a697-149">Minimum supported server</span></span><br/> | <span data-ttu-id="4a697-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4a697-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4a697-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="4a697-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a697-152"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-152"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4a697-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="4a697-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="4a697-154"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-154"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4a697-155">DLL</span><span class="sxs-lookup"><span data-stu-id="4a697-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4a697-156"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a697-156"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4a697-157">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="4a697-157">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4a697-158">**UploadPrinterDriverPackageW** (Unicode) et **UploadPrinterDriverPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="4a697-158">**UploadPrinterDriverPackageW** (Unicode) and **UploadPrinterDriverPackageA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="4a697-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4a697-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a697-160">Impression</span><span class="sxs-lookup"><span data-stu-id="4a697-160">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4a697-161">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="4a697-161">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

