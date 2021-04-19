---
description: Installe un package d’exception.
ms.assetid: c4c3c01c-9aaf-42cd-a690-13e2113b15b3
title: InstallComponentW fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallComponentW
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: 4d262322be6084429f03d5725f61c0e0f7140871
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544469"
---
# <a name="installcomponentw-function"></a><span data-ttu-id="49a5e-103">InstallComponentW fonction)</span><span class="sxs-lookup"><span data-stu-id="49a5e-103">InstallComponentW function</span></span>

<span data-ttu-id="49a5e-104">Installe un package d’exception.</span><span class="sxs-lookup"><span data-stu-id="49a5e-104">Installs an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a5e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="49a5e-105">Syntax</span></span>


```C++
void InstallComponentW(
  _In_           LPCWSTR InfPath,
  _In_opt_ const GUID    *CompGuid,
  _In_           DWORD   Flags,
  _In_opt_       INT     VerMajor,
  _In_opt_       INT     VerMinor,
  _In_opt_       INT     VerBuild,
  _In_opt_       INT     VerQFE,
  _In_opt_       LPCWSTR Name
);
```



## <a name="parameters"></a><span data-ttu-id="49a5e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="49a5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49a5e-107">*InfPath* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-107">*InfPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-108">Chemin d’accès à l’exception INF à traiter.</span><span class="sxs-lookup"><span data-stu-id="49a5e-108">The path to the exception INF to process.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-109">*CompGuid* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-109">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-110">GUID du composant d’exception en cours d’installation.</span><span class="sxs-lookup"><span data-stu-id="49a5e-110">The GUID of the exception component being installed.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-112">Indicateurs utilisés pour contrôler les comportements d’installation.</span><span class="sxs-lookup"><span data-stu-id="49a5e-112">The flags used to control installation behaviors.</span></span> <span data-ttu-id="49a5e-113">Ce paramètre peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="49a5e-113">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="49a5e-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="49a5e-114">Value</span></span>                                                                                                                                                                                                                                                               | <span data-ttu-id="49a5e-115">Signification</span><span class="sxs-lookup"><span data-stu-id="49a5e-115">Meaning</span></span>                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_FORCE"></span><span id="comp_flags_force"></span><dl> <span data-ttu-id="49a5e-116"><dt>**COMP \_ INDICATEURS \_ force**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-116"><dt>**COMP\_FLAGS\_FORCE**</dt> <dt>0x00000020</dt></span></span> </dl>                             | <span data-ttu-id="49a5e-117">Ignore la vérification de la version sur les remplacements de fichiers.</span><span class="sxs-lookup"><span data-stu-id="49a5e-117">Skips the version check on file replacements.</span></span><br/>                                                                                                    |
| <span id="COMP_FLAGS_NEEDS_UNINSTALL"></span><span id="comp_flags_needs_uninstall"></span><dl> <span data-ttu-id="49a5e-118"><dt>**COMP \_ les indicateurs \_ doivent être \_ désinstallés**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-118"><dt>**COMP\_FLAGS\_NEEDS\_UNINSTALL**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="49a5e-119">Sauvegardez les fichiers qui sont mis à jour pour être utilisés par une désinstallation du composant.</span><span class="sxs-lookup"><span data-stu-id="49a5e-119">Back up files that are updated to be used by an uninstall of the component.</span></span><br/>                                                                      |
| <span id="COMP_FLAGS_NO_OVERWRITE"></span><span id="comp_flags_no_overwrite"></span><dl> <span data-ttu-id="49a5e-120"><dt>**COMP \_ INDICATEURS \_ sans \_ remplacement**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-120"><dt>**COMP\_FLAGS\_NO\_OVERWRITE**</dt> <dt></dt></span></span> </dl>                 | <span data-ttu-id="49a5e-121">Ignore la sauvegarde des fichiers si la version du composant d’exception est identique à celle d’un composant installé.</span><span class="sxs-lookup"><span data-stu-id="49a5e-121">Skips backing up files if the Exception component version is the same as an installed component.</span></span> <span data-ttu-id="49a5e-122">Cet indicateur est utilisé dans un scénario de réinstallation.</span><span class="sxs-lookup"><span data-stu-id="49a5e-122">This flag is used in a reinstallation scenario.</span></span><br/> |
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="49a5e-123"><dt>**COMP \_ INDICATEURS \_ noui**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-123"><dt>**COMP\_FLAGS\_NOUI**</dt> <dt>0x00000002</dt></span></span> </dl>                                | <span data-ttu-id="49a5e-124">Supprime toute l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="49a5e-124">Suppresses all UI.</span></span><br/>                                                                                                                               |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="49a5e-125"><dt>**COMP \_ INDICATEURS \_ Update \_ dllcache**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-125"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt> <dt></dt></span></span> </dl>        | <span data-ttu-id="49a5e-126">Force la mise à jour du répertoire DLLCACHE lorsqu’un fichier système est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="49a5e-126">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>                                                                       |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="49a5e-127"><dt>**COMP \_ les indicateurs \_ utilisent le \_ \_ cache SVCPACK**</dt><dt></dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-127"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt> <dt></dt></span></span> </dl> | <span data-ttu-id="49a5e-128">Utilise les fichiers mis en cache par une installation de Windows Service Pack pour remplacer les fichiers sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="49a5e-128">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/>                                                                |



 

</dd> <dt>

<span data-ttu-id="49a5e-129">*VerMajor* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-129">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-130">Version principale du composant d’exception.</span><span class="sxs-lookup"><span data-stu-id="49a5e-130">The major version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-131">*Vermine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-131">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-132">Version mineure du composant d’exception.</span><span class="sxs-lookup"><span data-stu-id="49a5e-132">The minor version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-133">*VerBuild* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-133">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-134">Version de build du composant d’exception.</span><span class="sxs-lookup"><span data-stu-id="49a5e-134">The build version of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-135">*VerQFE* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-135">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-136">Révision du correctif logiciel du composant d’exception.</span><span class="sxs-lookup"><span data-stu-id="49a5e-136">The hotfix revision of the Exception component.</span></span>

</dd> <dt>

<span data-ttu-id="49a5e-137">*Nom* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="49a5e-137">*Name* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="49a5e-138">Chaîne descriptive du composant affiché par la boîte de dialogue protection des fichiers Windows si le système d’exploitation détecte qu’un fichier protégé de protection de fichiers Windows est endommagé, falsifié ou endommagé.</span><span class="sxs-lookup"><span data-stu-id="49a5e-138">The descriptive string of the component shown by the Windows File Protection dialog box if the operating system detects that a Windows File Protection protect file is damaged, tampered with, or corrupted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49a5e-139">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="49a5e-139">Return value</span></span>

<span data-ttu-id="49a5e-140">Cette fonction retourne une valeur **HRESULT** (S \_ OK ou un code d’échec).</span><span class="sxs-lookup"><span data-stu-id="49a5e-140">This function returns an **HRESULT** value (S\_OK or a failure code).</span></span> <span data-ttu-id="49a5e-141">Un code d’échec peut être vérifié par rapport à une valeur de 0x20000100 pour déterminer si l’échec est dû à un redémarrage requis.</span><span class="sxs-lookup"><span data-stu-id="49a5e-141">A failure code can be checked against a value of 0x20000100 to determine whether the failure is because a reboot is required.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a5e-142">Notes</span><span class="sxs-lookup"><span data-stu-id="49a5e-142">Remarks</span></span>

<span data-ttu-id="49a5e-143">Les packages d’exception sont des fichiers système Windows qui sont publiés en dehors d’une version de package complète de Windows et qui mettent à jour les fichiers du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="49a5e-143">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="49a5e-144">Les packages d’exception sont créés uniquement par des équipes de système d’exploitation qui ont reçu l’autorisation de mettre à jour les fichiers système Windows.</span><span class="sxs-lookup"><span data-stu-id="49a5e-144">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="49a5e-145">Pour installer et désinstaller des fichiers qui ne sont pas protégés par la protection des fichiers Windows, utilisez les fonctions documentées dans les [fonctions d’installation générales](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="49a5e-145">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="49a5e-146">Pour installer des pilotes de périphérique, les fournisseurs doivent utiliser les fonctions documentées dans [fonctions d’installation des appareils](https://msdn.microsoft.com/library/ms792954.aspx) et [fonctions PNP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="49a5e-146">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="49a5e-147">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="49a5e-147">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a5e-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="49a5e-148">Requirements</span></span>



| <span data-ttu-id="49a5e-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="49a5e-149">Requirement</span></span> | <span data-ttu-id="49a5e-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="49a5e-150">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49a5e-151">DLL</span><span class="sxs-lookup"><span data-stu-id="49a5e-151">DLL</span></span><br/> | <dl> <span data-ttu-id="49a5e-152"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="49a5e-152"><dt>Msoobci.dll</dt></span></span> </dl> |



 

 
