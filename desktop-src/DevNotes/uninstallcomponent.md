---
description: Supprime un package d’exception.
ms.assetid: d590d0f8-c9b2-4973-999b-99bbf94d4928
title: UninstallComponent fonction)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UninstallComponent
api_type:
- DllExport
api_location:
- Msoobci.dll
ms.openlocfilehash: a541f51b030c9be7a26d573794e4df3a7cfc6f47
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537359"
---
# <a name="uninstallcomponent-function"></a><span data-ttu-id="83cd0-103">UninstallComponent fonction)</span><span class="sxs-lookup"><span data-stu-id="83cd0-103">UninstallComponent function</span></span>

<span data-ttu-id="83cd0-104">Supprime un package d’exception.</span><span class="sxs-lookup"><span data-stu-id="83cd0-104">Removes an exception package.</span></span>

## <a name="syntax"></a><span data-ttu-id="83cd0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83cd0-105">Syntax</span></span>


```C++
void UninstallComponent(
  _In_opt_ const GUID  *CompGuid,
  _In_           DWORD Flags,
  _In_opt_       INT   VerMajor,
  _In_opt_       INT   VerMinor,
  _In_opt_       INT   VerBuild,
  _In_opt_       INT   VerQFE
);
```



## <a name="parameters"></a><span data-ttu-id="83cd0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83cd0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83cd0-107">*CompGuid* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-107">*CompGuid* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-108">GUID du composant d’exception en cours de désinstallation.</span><span class="sxs-lookup"><span data-stu-id="83cd0-108">The GUID of the exception component being uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="83cd0-109">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-109">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-110">Indicateurs utilisés pour contrôler les comportements d’installation.</span><span class="sxs-lookup"><span data-stu-id="83cd0-110">The flags used to control installation behaviors.</span></span> <span data-ttu-id="83cd0-111">Ce paramètre peut être une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="83cd0-111">This parameter can be a combination of the following values.</span></span>



| <span data-ttu-id="83cd0-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="83cd0-112">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="83cd0-113">Signification</span><span class="sxs-lookup"><span data-stu-id="83cd0-113">Meaning</span></span>                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="COMP_FLAGS_NOUI"></span><span id="comp_flags_noui"></span><dl> <span data-ttu-id="83cd0-114"><dt>**\_indicateurs COMP \_ noui**</dt></span><span class="sxs-lookup"><span data-stu-id="83cd0-114"><dt>**COMP\_FLAGS\_NOUI**</dt></span></span> </dl>                                          | <span data-ttu-id="83cd0-115">Supprime toute l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="83cd0-115">Suppresses all UI.</span></span><br/>                                                                |
| <span id="COMP_FLAGS_UPDATE_DLLCACHE"></span><span id="comp_flags_update_dllcache"></span><dl> <span data-ttu-id="83cd0-116"><dt>**\_ \_ mise à jour dllcache des indicateurs COMP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="83cd0-116"><dt>**COMP\_FLAGS\_UPDATE\_DLLCACHE**</dt></span></span> </dl>        | <span data-ttu-id="83cd0-117">Force la mise à jour du répertoire DLLCACHE lorsqu’un fichier système est mis à jour.</span><span class="sxs-lookup"><span data-stu-id="83cd0-117">Forces the DLLCACHE directory to be updated when a system file is updated.</span></span><br/>        |
| <span id="COMP_FLAGS_USE_SVCPACK_CACHE"></span><span id="comp_flags_use_svcpack_cache"></span><dl> <span data-ttu-id="83cd0-118"><dt>**les \_ indicateurs COMP \_ utilisent le \_ \_ cache SVCPACK**</dt></span><span class="sxs-lookup"><span data-stu-id="83cd0-118"><dt>**COMP\_FLAGS\_USE\_SVCPACK\_CACHE**</dt></span></span> </dl> | <span data-ttu-id="83cd0-119">Utilise les fichiers mis en cache par une installation de Windows Service Pack pour remplacer les fichiers sauvegardés.</span><span class="sxs-lookup"><span data-stu-id="83cd0-119">Uses files cached by a Windows service pack install to supersede files backed up.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="83cd0-120">*VerMajor* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-120">*VerMajor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-121">Version principale du composant d’exception à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="83cd0-121">The major version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="83cd0-122">*Vermine* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-122">*VerMinor* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-123">Version mineure du composant d’exception à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="83cd0-123">The minor version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="83cd0-124">*VerBuild* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-124">*VerBuild* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-125">Version de build du composant d’exception à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="83cd0-125">The build version of the Exception component to be uninstalled.</span></span>

</dd> <dt>

<span data-ttu-id="83cd0-126">*VerQFE* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="83cd0-126">*VerQFE* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="83cd0-127">Révision du correctif logiciel du composant d’exception à désinstaller.</span><span class="sxs-lookup"><span data-stu-id="83cd0-127">The hotfix revision of the Exception component to be uninstalled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83cd0-128">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="83cd0-128">Return value</span></span>

<span data-ttu-id="83cd0-129">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="83cd0-129">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="83cd0-130">Notes</span><span class="sxs-lookup"><span data-stu-id="83cd0-130">Remarks</span></span>

<span data-ttu-id="83cd0-131">Les packages d’exception sont des fichiers système Windows qui sont publiés en dehors d’une version de package complète de Windows et qui mettent à jour les fichiers du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="83cd0-131">Exception packages are Windows system files that are released outside of a full package Windows release and that update operating-system files.</span></span> <span data-ttu-id="83cd0-132">Les packages d’exception sont créés uniquement par des équipes de système d’exploitation qui ont reçu l’autorisation de mettre à jour les fichiers système Windows.</span><span class="sxs-lookup"><span data-stu-id="83cd0-132">Exception packages are authored only by operating-system teams that have been granted authorization to update Windows system files.</span></span>

<span data-ttu-id="83cd0-133">Pour installer et désinstaller des fichiers qui ne sont pas protégés par la protection des fichiers Windows, utilisez les fonctions documentées dans les [fonctions d’installation générales](https://msdn.microsoft.com/library/ms794585.aspx).</span><span class="sxs-lookup"><span data-stu-id="83cd0-133">To install and uninstall files that are not protected by Windows File Protection, use the functions documented in [General Setup Functions](https://msdn.microsoft.com/library/ms794585.aspx).</span></span> <span data-ttu-id="83cd0-134">Pour installer des pilotes de périphérique, les fournisseurs doivent utiliser les fonctions documentées dans [fonctions d’installation des appareils](https://msdn.microsoft.com/library/ms792954.aspx) et [fonctions PNP Configuration Manager](https://msdn.microsoft.com/library/ms790838.aspx).</span><span class="sxs-lookup"><span data-stu-id="83cd0-134">To install device drivers, venders should use functions documented in [Device Installation Functions](https://msdn.microsoft.com/library/ms792954.aspx) and [PnP Configuration Manager Functions](https://msdn.microsoft.com/library/ms790838.aspx).</span></span>

<span data-ttu-id="83cd0-135">Cette fonction n’a pas de bibliothèque d’importation ou de fichier d’en-tête associé ; vous devez l’appeler à l’aide des fonctions [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="83cd0-135">This function has no associated import library or header file; you must call it by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="83cd0-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83cd0-136">Requirements</span></span>



| <span data-ttu-id="83cd0-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83cd0-137">Requirement</span></span> | <span data-ttu-id="83cd0-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="83cd0-138">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83cd0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="83cd0-139">DLL</span></span><br/> | <dl> <span data-ttu-id="83cd0-140"><dt>Msoobci.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83cd0-140"><dt>Msoobci.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83cd0-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83cd0-141">See also</span></span>

<dl> <span data-ttu-id="83cd0-142"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="83cd0-142"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="83cd0-143">**InstallComponentW**</span><span class="sxs-lookup"><span data-stu-id="83cd0-143">**InstallComponentW**</span></span>](installcomponentw.md)
</dt> </dl>

 

 
