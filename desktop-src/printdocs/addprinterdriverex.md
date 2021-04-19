---
description: La fonction AddPrinterDriverEx installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote.
ms.assetid: 472adb7d-39cc-4c76-b96c-610ff9d276ad
title: AddPrinterDriverEx, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPrinterDriverEx
- AddPrinterDriverExA
- AddPrinterDriverExW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: c431d710ddad7f723d063fd5bf046bae08b77b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518665"
---
# <a name="addprinterdriverex-function"></a><span data-ttu-id="59c3d-103">AddPrinterDriverEx fonction)</span><span class="sxs-lookup"><span data-stu-id="59c3d-103">AddPrinterDriverEx function</span></span>

<span data-ttu-id="59c3d-104">La fonction **AddPrinterDriverEx** installe un pilote d’imprimante local ou distant et lie les fichiers de configuration, de données et de pilote.</span><span class="sxs-lookup"><span data-stu-id="59c3d-104">The **AddPrinterDriverEx** function installs a local or remote printer driver and links the configuration, data, and driver files.</span></span> <span data-ttu-id="59c3d-105">Outre les fonctionnalités de [**AddPrinterDriver**](addprinterdriver.md), il offre également des options qui permettent une mise à niveau stricte, une rétrogradation stricte, la copie de fichiers récents uniquement et la copie de tous les fichiers (quels que soient les horodatages des fichiers).</span><span class="sxs-lookup"><span data-stu-id="59c3d-105">Besides having the capabilities of [**AddPrinterDriver**](addprinterdriver.md), it also has options that permit strict upgrade, strict downgrade, copying of newer files only, and copying of all files (regardless of file time stamps).</span></span>

> [!Note]  
> <span data-ttu-id="59c3d-106">L’installation d’un pilote d’imprimante sans package de pilotes n’est plus recommandée.</span><span class="sxs-lookup"><span data-stu-id="59c3d-106">Installing a printer driver without a driver package is no longer recommended.</span></span> <span data-ttu-id="59c3d-107">Utilisez [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="59c3d-107">Use [**InstallPrinterDriverFromPackage**](installprinterdriverfrompackage.md) instead.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="59c3d-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59c3d-108">Syntax</span></span>


```C++
BOOL AddPrinterDriverEx(
  _In_    LPTSTR pName,
  _In_    DWORD  Level,
  _Inout_ LPBYTE pDriverInfo,
  _In_    DWORD  dwFileCopyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="59c3d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59c3d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59c3d-110">*pname* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-110">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3d-111">Pointeur vers une chaîne se terminant par un caractère null qui spécifie le nom du serveur sur lequel le pilote doit être installé.</span><span class="sxs-lookup"><span data-stu-id="59c3d-111">A pointer to a null-terminated string that specifies the name of the server on which the driver should be installed.</span></span> <span data-ttu-id="59c3d-112">Si ce paramètre a la **valeur null**, la fonction installe le pilote sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="59c3d-112">If this parameter is **NULL**, the function installs the driver on the local computer.</span></span>

</dd> <dt>

<span data-ttu-id="59c3d-113">De *niveau* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-113">*Level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3d-114">Version de la structure vers laquelle *pDriverInfo* pointe.</span><span class="sxs-lookup"><span data-stu-id="59c3d-114">The version of the structure to which *pDriverInfo* points.</span></span> <span data-ttu-id="59c3d-115">Cette valeur peut être 2, 3, 4, 6 ou 8.</span><span class="sxs-lookup"><span data-stu-id="59c3d-115">This value can be 2, 3, 4, 6, or 8.</span></span>

</dd> <dt>

<span data-ttu-id="59c3d-116">*pDriverInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-116">*pDriverInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3d-117">Pointeur vers une structure contenant des informations sur le pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="59c3d-117">A pointer to a structure containing printer driver information.</span></span> <span data-ttu-id="59c3d-118">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="59c3d-118">It can be one of the following.</span></span>



| <span data-ttu-id="59c3d-119">Valeur de niveau</span><span class="sxs-lookup"><span data-stu-id="59c3d-119">Value of Level</span></span>                                                                                       | <span data-ttu-id="59c3d-120">\_Structure info \_ du pilote \*</span><span class="sxs-lookup"><span data-stu-id="59c3d-120">DRIVER\_INFO\_\* Structure</span></span>                          |
|------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="2"></span><dl> <span data-ttu-id="59c3d-121"><dt>**2**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-121"><dt>**2**</dt></span></span> </dl> | [<span data-ttu-id="59c3d-122">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="59c3d-122">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)<br/> |
| <span id="3"></span><dl> <span data-ttu-id="59c3d-123"><dt>**3**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-123"><dt>**3**</dt></span></span> </dl> | [<span data-ttu-id="59c3d-124">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="59c3d-124">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)<br/> |
| <span id="4"></span><dl> <span data-ttu-id="59c3d-125"><dt>**4**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-125"><dt>**4**</dt></span></span> </dl> | [<span data-ttu-id="59c3d-126">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="59c3d-126">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)<br/> |
| <span id="6"></span><dl> <span data-ttu-id="59c3d-127"><dt>**6**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-127"><dt>**6**</dt></span></span> </dl> | [<span data-ttu-id="59c3d-128">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="59c3d-128">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)<br/> |
| <span id="8"></span><dl> <span data-ttu-id="59c3d-129"><dt>**8**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-129"><dt>**8**</dt></span></span> </dl> | [<span data-ttu-id="59c3d-130">**\_Informations sur le pilote \_ 8**</span><span class="sxs-lookup"><span data-stu-id="59c3d-130">**DRIVER\_INFO\_8**</span></span>](driver-info-8.md)<br/> |



 

<span data-ttu-id="59c3d-131">Si le membre **pEnvironment** de la structure vers laquelle pointe *PDriverInfo* a la **valeur null**, la fonction utilise l’environnement actuel de l’appelant/du client, et non de l’environnement du serveur de destination/serveur.</span><span class="sxs-lookup"><span data-stu-id="59c3d-131">If the **pEnvironment** member of the structure pointed to by *pDriverInfo* is **NULL**, the function uses the current environment of the caller/client, not the environment of the destination/server.</span></span>

</dd> <dt>

<span data-ttu-id="59c3d-132">*dwFileCopyFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-132">*dwFileCopyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59c3d-133">Options de copie des fichiers de pilote.</span><span class="sxs-lookup"><span data-stu-id="59c3d-133">The options for copying the driver files.</span></span> <span data-ttu-id="59c3d-134">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="59c3d-134">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="59c3d-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c3d-135">Value</span></span>                                                                                                                                                                                         | <span data-ttu-id="59c3d-136">Signification</span><span class="sxs-lookup"><span data-stu-id="59c3d-136">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="APD_COPY_ALL_FILES"></span><span id="apd_copy_all_files"></span><dl> <span data-ttu-id="59c3d-137"><dt>**APD \_ copier \_ tous les \_ fichiers**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-137"><dt>**APD\_COPY\_ALL\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="59c3d-138">Ajoutez le pilote d’imprimante et copiez tous les fichiers dans le répertoire du pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="59c3d-138">Add the printer driver and copy all the files in the printer-driver directory.</span></span> <span data-ttu-id="59c3d-139">Les horodatages de fichier sont ignorés avec cette option.</span><span class="sxs-lookup"><span data-stu-id="59c3d-139">The file time stamps are ignored with this option.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="APD_COPY_FROM_DIRECTORY"></span><span id="apd_copy_from_directory"></span><dl> <span data-ttu-id="59c3d-140"><dt>**APD \_ copier \_ à partir de l' \_ Annuaire**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-140"><dt>**APD\_COPY\_FROM\_DIRECTORY**</dt></span></span> </dl> | <span data-ttu-id="59c3d-141">Ajoutez le pilote d’imprimante à l’aide des noms de fichiers complets spécifiés dans la structure [**\_ info \_ 6 du pilote**](driver-info-6.md) .</span><span class="sxs-lookup"><span data-stu-id="59c3d-141">Add the printer driver using the fully qualified file names specified in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure.</span></span> <span data-ttu-id="59c3d-142">Cet indicateur est associé à l’un des autres indicateurs de copie.</span><span class="sxs-lookup"><span data-stu-id="59c3d-142">This flag is ORed in conjunction with one of the other copy flags.</span></span> <span data-ttu-id="59c3d-143">Si cet indicateur est défini, **AddPrinterDriverEx** échoue si les fichiers n’existent pas là où ils sont spécifiés pour exister dans la structure **\_ information \_ 6 du pilote** .</span><span class="sxs-lookup"><span data-stu-id="59c3d-143">If this flag is set, **AddPrinterDriverEx** will fail if the files do not exist where they are specified to exist by the **DRIVER\_INFO\_6** structure.</span></span> <span data-ttu-id="59c3d-144">Les fichiers ne doivent pas être copiés dans le répertoire du pilote d’imprimante du système.</span><span class="sxs-lookup"><span data-stu-id="59c3d-144">The files do not need to be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="59c3d-145">Consultez les notes.</span><span class="sxs-lookup"><span data-stu-id="59c3d-145">See the Remarks.</span></span><br/> <span data-ttu-id="59c3d-146">**Windows 2000 :** Cet indicateur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="59c3d-146">**Windows 2000:** This flag is not supported.</span></span><br/> |
| <span id="APD_COPY_NEW_FILES"></span><span id="apd_copy_new_files"></span><dl> <span data-ttu-id="59c3d-147"><dt>**APD \_ copier les \_ nouveaux \_ fichiers**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-147"><dt>**APD\_COPY\_NEW\_FILES**</dt></span></span> </dl>                | <span data-ttu-id="59c3d-148">Ajoutez le pilote d’imprimante et copiez les fichiers du répertoire du pilote d’imprimante qui sont plus récents que les fichiers correspondants en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="59c3d-148">Add the printer driver and copy the files in the printer-driver directory that are newer than any corresponding files that are currently in use.</span></span> <span data-ttu-id="59c3d-149">Cet indicateur émule le comportement de [**AddPrinterDriver**](addprinterdriver.md).</span><span class="sxs-lookup"><span data-stu-id="59c3d-149">This flag emulates the behavior of [**AddPrinterDriver**](addprinterdriver.md).</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="APD_STRICT_DOWNGRADE"></span><span id="apd_strict_downgrade"></span><dl> <span data-ttu-id="59c3d-150"><dt>**\_rétrogradation stricte APD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-150"><dt>**APD\_STRICT\_DOWNGRADE**</dt></span></span> </dl>           | <span data-ttu-id="59c3d-151">Ajoutez le pilote d’imprimante uniquement si tous les fichiers du répertoire du pilote d’imprimante sont antérieurs aux fichiers correspondants en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="59c3d-151">Add the printer driver only if all the files in the printer-driver directory are older than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="APD_STRICT_UPGRADE"></span><span id="apd_strict_upgrade"></span><dl> <span data-ttu-id="59c3d-152"><dt>**\_ \_ mise à niveau STRICTe APD**</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-152"><dt>**APD\_STRICT\_UPGRADE**</dt></span></span> </dl>                 | <span data-ttu-id="59c3d-153">Ajoutez le pilote d’imprimante uniquement si tous les fichiers du répertoire du pilote d’imprimante sont plus récents que les fichiers correspondants en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="59c3d-153">Add the printer driver only if all the files in the printer-driver directory are newer than any corresponding files currently in use.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59c3d-154">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59c3d-154">Return value</span></span>

<span data-ttu-id="59c3d-155">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="59c3d-155">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="59c3d-156">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="59c3d-156">If the function fails, the return value is zero.</span></span>

<span data-ttu-id="59c3d-157">Si le pilote d’imprimante rencontre des problèmes de fonctionnement avec le système d’exploitation, **AddPrinterDriverEx** échoue avec l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="59c3d-157">If the printer driver is known to have problems working with the operating system, **AddPrinterDriverEx** will fail with one of the following error codes:</span></span>



| <span data-ttu-id="59c3d-158">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="59c3d-158">Error Code</span></span>                      | <span data-ttu-id="59c3d-159">Signification</span><span class="sxs-lookup"><span data-stu-id="59c3d-159">Meaning</span></span>                                                                                                                                                   |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c3d-160">ERREUR \_ de \_ pilote d’imprimante \_ bloquée</span><span class="sxs-lookup"><span data-stu-id="59c3d-160">ERROR\_PRINTER\_DRIVER\_BLOCKED</span></span> | <span data-ttu-id="59c3d-161">Le pilote ne fonctionne pas sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="59c3d-161">The driver does not work on the operating system.</span></span>                                                                                                         |
| <span data-ttu-id="59c3d-162">ERREUR \_ de \_ pilote d’imprimante \_</span><span class="sxs-lookup"><span data-stu-id="59c3d-162">ERROR\_PRINTER\_DRIVER\_WARNED</span></span>  | <span data-ttu-id="59c3d-163">Le pilote n’est pas fiable sur le système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="59c3d-163">The driver is unreliable on the operating system.</span></span> <span data-ttu-id="59c3d-164">Toutefois, si \_ le pilote d’installation APD \_ \_ est spécifié, le pilote est installé et aucun avertissement n’est fourni.</span><span class="sxs-lookup"><span data-stu-id="59c3d-164">However, if APD\_INSTALL\_WARNED\_DRIVER is specified, the driver is installed and no warning is given.</span></span> |



 

<span data-ttu-id="59c3d-165">Pour plus d'informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="59c3d-165">For more information, see the Remarks.</span></span>

## <a name="remarks"></a><span data-ttu-id="59c3d-166">Notes</span><span class="sxs-lookup"><span data-stu-id="59c3d-166">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="59c3d-167">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="59c3d-167">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="59c3d-168">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="59c3d-168">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="59c3d-169">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="59c3d-169">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="59c3d-170">L’appelant doit avoir le [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="59c3d-170">The caller must have the [SeLoadDriverPrivilege](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

<span data-ttu-id="59c3d-171">Avant d’appeler la fonction **AddPrinterDriverEx** , tous les fichiers requis par le pilote doivent être copiés dans le répertoire du pilote d’imprimante du système.</span><span class="sxs-lookup"><span data-stu-id="59c3d-171">Before calling the **AddPrinterDriverEx** function, all files required by the driver must be copied to the system's printer-driver directory.</span></span> <span data-ttu-id="59c3d-172">Pour récupérer le nom de ce répertoire, appelez la fonction [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="59c3d-172">To retrieve the name of this directory, call the [**GetPrinterDriverDirectory**](getprinterdriverdirectory.md) function.</span></span>

<span data-ttu-id="59c3d-173">Pour déterminer les pilotes d’imprimante actuellement installés, appelez la fonction [**EnumPrinterDrivers**](enumprinterdrivers.md) .</span><span class="sxs-lookup"><span data-stu-id="59c3d-173">To determine which printer drivers are currently installed, call the [**EnumPrinterDrivers**](enumprinterdrivers.md) function.</span></span>

<span data-ttu-id="59c3d-174">Si le pilote d’imprimante a été ajouté avec succès, la fonction appelle la fonction DrvDriverEvent (DRIVER \_ Event \_ Initialize, Level, Driver \_ info \_ \* , lParam) pour permettre au pilote d’effectuer les initialisations nécessaires pendant l’installation d’un pilote d’imprimante.</span><span class="sxs-lookup"><span data-stu-id="59c3d-174">If the printer driver has been successfully added, the function calls the DrvDriverEvent (DRIVER\_EVENT\_INITIALIZE, Level, DRIVER\_INFO\_\*, lparam ) function to allow the driver to perform any initializations required during the installation of a printer driver.</span></span> <span data-ttu-id="59c3d-175">Pour plus d’informations sur **DrvDriverEvent**, consultez le kit de développement de pilotes (DDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="59c3d-175">For more information about **DrvDriverEvent**, see the Microsoft Windows Driver Development Kit (DDK)</span></span>

<span data-ttu-id="59c3d-176">Le pilote ne doit pas utiliser un appel d’interface utilisateur lors de l’appel à **DrvDriverEvent**.</span><span class="sxs-lookup"><span data-stu-id="59c3d-176">The driver should not use a UI call during the call to **DrvDriverEvent**.</span></span> <span data-ttu-id="59c3d-177">Pour effectuer des tâches liées à l’interface utilisateur, le programme d’installation doit utiliser l’entrée VendorSetup dans le fichier. inf de l’imprimante ou, pour Plug-and-Play appareils, le programme d’installation peut utiliser un co-programme d’installation spécifique à l’appareil.</span><span class="sxs-lookup"><span data-stu-id="59c3d-177">To do UI-related jobs, the installer should either use the VendorSetup entry in the printer's .inf file or, for Plug and Play devices, the installer can use a device-specific co-installer.</span></span> <span data-ttu-id="59c3d-178">Pour plus d’informations sur VendorSetup, consultez le DDK.</span><span class="sxs-lookup"><span data-stu-id="59c3d-178">For more information about VendorSetup, see the DDK.</span></span>

<span data-ttu-id="59c3d-179">Les fichiers qui sont référencés dans la [**structure \_ info \_ 6 du pilote**](driver-info-6.md) doivent être locaux sur l’ordinateur à partir duquel l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="59c3d-179">The files that are referenced in the [**DRIVER\_INFO\_6**](driver-info-6.md) structure must be local to the machine from which the call is made.</span></span> <span data-ttu-id="59c3d-180">Un nom de fichier peut être un nom UNC tant que le nom UNC est l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="59c3d-180">A file name can be a UNC name as long as the UNC name is the local machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="59c3d-181">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59c3d-181">Requirements</span></span>



| <span data-ttu-id="59c3d-182">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59c3d-182">Requirement</span></span> | <span data-ttu-id="59c3d-183">Valeur</span><span class="sxs-lookup"><span data-stu-id="59c3d-183">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59c3d-184">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3d-184">Minimum supported client</span></span><br/> | <span data-ttu-id="59c3d-185">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="59c3d-186">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="59c3d-186">Minimum supported server</span></span><br/> | <span data-ttu-id="59c3d-187">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="59c3d-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="59c3d-188">En-tête</span><span class="sxs-lookup"><span data-stu-id="59c3d-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="59c3d-189"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-189"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="59c3d-190">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59c3d-190">Library</span></span><br/>                  | <dl> <span data-ttu-id="59c3d-191"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-191"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="59c3d-192">DLL</span><span class="sxs-lookup"><span data-stu-id="59c3d-192">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59c3d-193"><dt>Winspool. drv</dt></span><span class="sxs-lookup"><span data-stu-id="59c3d-193"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="59c3d-194">Noms Unicode et ANSI</span><span class="sxs-lookup"><span data-stu-id="59c3d-194">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="59c3d-195">**AddPrinterDriverExW** (Unicode) et **AddPrinterDriverExA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="59c3d-195">**AddPrinterDriverExW** (Unicode) and **AddPrinterDriverExA** (ANSI)</span></span><br/>                           |



## <a name="see-also"></a><span data-ttu-id="59c3d-196">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59c3d-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59c3d-197">Impression</span><span class="sxs-lookup"><span data-stu-id="59c3d-197">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="59c3d-198">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="59c3d-198">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="59c3d-199">**AddPrinterDriver**</span><span class="sxs-lookup"><span data-stu-id="59c3d-199">**AddPrinterDriver**</span></span>](addprinterdriver.md)
</dt> <dt>

[<span data-ttu-id="59c3d-200">**\_Informations sur le pilote \_ 2**</span><span class="sxs-lookup"><span data-stu-id="59c3d-200">**DRIVER\_INFO\_2**</span></span>](driver-info-2.md)
</dt> <dt>

[<span data-ttu-id="59c3d-201">**\_Informations sur le pilote \_ 3**</span><span class="sxs-lookup"><span data-stu-id="59c3d-201">**DRIVER\_INFO\_3**</span></span>](driver-info-3.md)
</dt> <dt>

[<span data-ttu-id="59c3d-202">**\_Informations sur le pilote \_ 4**</span><span class="sxs-lookup"><span data-stu-id="59c3d-202">**DRIVER\_INFO\_4**</span></span>](driver-info-4.md)
</dt> <dt>

[<span data-ttu-id="59c3d-203">**\_Informations sur le pilote \_ 6**</span><span class="sxs-lookup"><span data-stu-id="59c3d-203">**DRIVER\_INFO\_6**</span></span>](driver-info-6.md)
</dt> <dt>

[<span data-ttu-id="59c3d-204">**DeletePrinterDriverEx**</span><span class="sxs-lookup"><span data-stu-id="59c3d-204">**DeletePrinterDriverEx**</span></span>](deleteprinterdriverex.md)
</dt> <dt>

[<span data-ttu-id="59c3d-205">**EnumPrinterDrivers**</span><span class="sxs-lookup"><span data-stu-id="59c3d-205">**EnumPrinterDrivers**</span></span>](enumprinterdrivers.md)
</dt> <dt>

[<span data-ttu-id="59c3d-206">**GetPrinterDriverDirectory**</span><span class="sxs-lookup"><span data-stu-id="59c3d-206">**GetPrinterDriverDirectory**</span></span>](getprinterdriverdirectory.md)
</dt> </dl>

 

