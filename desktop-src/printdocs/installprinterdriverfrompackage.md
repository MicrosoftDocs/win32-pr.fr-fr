---
description: Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes des serveurs d’impression.
ms.assetid: 5906d9c6-9fbf-4ec6-81ce-112a9ef6d7c0
title: InstallPrinterDriverFromPackage, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallPrinterDriverFromPackage
- InstallPrinterDriverFromPackageA
- InstallPrinterDriverFromPackageW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: f817f5e73537f6a71d8236ad9532acdf02a53552
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210468"
---
# <a name="installprinterdriverfrompackage-function"></a><span data-ttu-id="8a6bf-103">InstallPrinterDriverFromPackage fonction)</span><span class="sxs-lookup"><span data-stu-id="8a6bf-103">InstallPrinterDriverFromPackage function</span></span>

<span data-ttu-id="8a6bf-104">Installe un pilote d’imprimante à partir d’un package de pilotes qui se trouve dans le magasin de pilotes du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-104">Installs a printer driver from a driver package that is in the print server's driver store.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a6bf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8a6bf-105">Syntax</span></span>


```C++
HRESULT InstallPrinterDriverFromPackage(
  _In_ LPCTSTR pszServer,
  _In_ LPCTSTR pszInfPath,
  _In_ LPCTSTR pszDriverName,
  _In_ LPCTSTR pszEnvironment,
  _In_ DWORD   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8a6bf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8a6bf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a6bf-107">*pszServer* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-107">*pszServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6bf-108">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-108">A pointer to a constant, null-terminated string that specifies the name of the print server.</span></span> <span data-ttu-id="8a6bf-109">La **valeur null** correspond à l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-109">**NULL** means the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="8a6bf-110">*pszInfPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-110">*pszInfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6bf-111">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le chemin d’accès du magasin de pilotes au fichier. inf du pilote d’impression.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-111">A pointer to a constant, null-terminated string that specifies the driver store path to the print driver's .inf file.</span></span> <span data-ttu-id="8a6bf-112">**Null** signifie que le pilote se trouve dans un fichier INF fourni avec Windows.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-112">**NULL** means the driver is in an inf file that shipped with Windows.</span></span>

</dd> <dt>

<span data-ttu-id="8a6bf-113">*pszDriverName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-113">*pszDriverName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6bf-114">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie le nom du pilote.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-114">A pointer to a constant, null-terminated string that specifies the name of the driver.</span></span>

</dd> <dt>

<span data-ttu-id="8a6bf-115">*pszEnvironment* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-115">*pszEnvironment* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6bf-116">Pointeur vers une chaîne constante, se terminant par un caractère null qui spécifie l’architecture du processeur (par exemple, Windows NT x86).</span><span class="sxs-lookup"><span data-stu-id="8a6bf-116">A pointer to a constant, null-terminated string that specifies the processor architecture (for example, Windows NT x86).</span></span> <span data-ttu-id="8a6bf-117">Il peut s’agir de la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-117">This can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a6bf-118">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a6bf-119">Ce peut être uniquement 0 ou IPDFP \_ copier \_ tous les \_ fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-119">This can only be 0 or IPDFP\_COPY\_ALL\_FILES.</span></span> <span data-ttu-id="8a6bf-120">La valeur 0 signifie que le pilote d’imprimante doit être ajouté et que tous les fichiers du répertoire du pilote d’imprimante qui sont plus récents que les fichiers correspondants en cours d’utilisation doivent être copiés.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-120">A value of 0 means that the printer driver must be added and any files in the printer driver directory that are newer than corresponding files currently in use must be copied.</span></span> <span data-ttu-id="8a6bf-121">La valeur IPDFP \_ copier \_ tous les \_ fichiers signifie que le pilote d’imprimante et tous les fichiers du répertoire du pilote d’imprimante doivent être ajoutés.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-121">A value of IPDFP\_COPY\_ALL\_FILES means the printer driver and all the files in the printer driver directory must be added.</span></span> <span data-ttu-id="8a6bf-122">Les horodatages de fichier sont ignorés quand *dwFlags* a la valeur IPDFP \_ copier \_ tous les \_ fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-122">The file time stamps are ignored when *dwFlags* has a value of IPDFP\_COPY\_ALL\_FILES.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a6bf-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8a6bf-123">Return value</span></span>

<span data-ttu-id="8a6bf-124">Si l’opération a échoué, la valeur de retour est S \_ OK, sinon le **HRESULT** contient un code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-124">If the operation succeeds, the return value is S\_OK, otherwise the **HRESULT** will contain an error code.</span></span>

<span data-ttu-id="8a6bf-125">Pour plus d’informations sur les codes d’erreur COM, consultez [gestion des erreurs](../com/error-handling-in-com.md).</span><span class="sxs-lookup"><span data-stu-id="8a6bf-125">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8a6bf-126">Notes</span><span class="sxs-lookup"><span data-stu-id="8a6bf-126">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="8a6bf-127">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-127">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="8a6bf-128">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-128">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="8a6bf-129">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-129">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="8a6bf-130">Le magasin de pilotes est généralement% windir% \\ INF ou% windir% \\ system32 \\ DriverStore \\ FileRepository.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-130">The driver store is typically either %windir%\\inf or %windir%\\System32\\DriverStore\\FileRepository.</span></span>

<span data-ttu-id="8a6bf-131">**InstallPrinterDriverFromPackage** installe également d’autres fichiers dans le package, tels que les profils de couleurs et les processeurs d’impression.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-131">**InstallPrinterDriverFromPackage** also installs other files in the package, such as color profiles and print processors.</span></span>

<span data-ttu-id="8a6bf-132">Les utilisateurs doivent disposer de droits d’administration d’imprimante pour installer sur un ordinateur distant ou sur l’ordinateur local lorsque l’utilisateur est connecté avec les services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-132">Users must have printer administration rights to install either on a remote computer or on the local computer when the user is logged in with Terminal Services.</span></span>

<span data-ttu-id="8a6bf-133">Seuls les packages signés peuvent être installés sur un ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="8a6bf-133">Only signed packages can be installed on a remote computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a6bf-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8a6bf-134">Requirements</span></span>



| <span data-ttu-id="8a6bf-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8a6bf-135">Requirement</span></span> | <span data-ttu-id="8a6bf-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="8a6bf-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8a6bf-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a6bf-137">Minimum supported client</span></span><br/> | <span data-ttu-id="8a6bf-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="8a6bf-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8a6bf-139">Minimum supported server</span></span><br/> | <span data-ttu-id="8a6bf-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8a6bf-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="8a6bf-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="8a6bf-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="8a6bf-142"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8a6bf-142"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="8a6bf-143">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8a6bf-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="8a6bf-144"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8a6bf-144"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="8a6bf-145">DLL</span><span class="sxs-lookup"><span data-stu-id="8a6bf-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a6bf-146"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a6bf-146"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="8a6bf-147">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="8a6bf-147">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="8a6bf-148">**InstallPrinterDriverFromPackageW** (Unicode) et **InstallPrinterDriverFromPackageA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="8a6bf-148">**InstallPrinterDriverFromPackageW** (Unicode) and **InstallPrinterDriverFromPackageA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a6bf-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8a6bf-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a6bf-150">Impression</span><span class="sxs-lookup"><span data-stu-id="8a6bf-150">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="8a6bf-151">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="8a6bf-151">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

