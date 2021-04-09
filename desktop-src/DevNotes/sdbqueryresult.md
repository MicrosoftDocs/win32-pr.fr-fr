---
description: Contient les résultats de l’interrogation de la base de données de shims pour un exécutable correspondant.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: SDBQUERYRESULT, structure
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103950530"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="d9317-103">SDBQUERYRESULT, structure</span><span class="sxs-lookup"><span data-stu-id="d9317-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="d9317-104">Contient les résultats de l’interrogation de la base de données de shims pour un exécutable correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9317-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9317-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d9317-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="d9317-106">Membres</span><span class="sxs-lookup"><span data-stu-id="d9317-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d9317-107">**atrExes**</span><span class="sxs-lookup"><span data-stu-id="d9317-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-108">Valeurs **TAGREF** des fichiers exécutables correspondants.</span><span class="sxs-lookup"><span data-stu-id="d9317-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="d9317-109">Notez que **sdb \_ Max \_ exe** est défini sur 16.</span><span class="sxs-lookup"><span data-stu-id="d9317-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-110">**adwExeFlags**</span><span class="sxs-lookup"><span data-stu-id="d9317-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-111">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9317-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d9317-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d9317-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d9317-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d9317-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="d9317-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d9317-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d9317-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d9317-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d9317-119">**atrLayers**</span><span class="sxs-lookup"><span data-stu-id="d9317-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-120">Valeurs **TAGREF** des couches correspondantes.</span><span class="sxs-lookup"><span data-stu-id="d9317-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="d9317-121">Notez que **le \_ nombre maximal de \_ couches sdb** est défini sur 8.</span><span class="sxs-lookup"><span data-stu-id="d9317-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-122">**dwLayerFlags**</span><span class="sxs-lookup"><span data-stu-id="d9317-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-123">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9317-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d9317-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d9317-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d9317-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d9317-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="d9317-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d9317-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d9317-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d9317-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d9317-131">**trApphelp**</span><span class="sxs-lookup"><span data-stu-id="d9317-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-132">Valeur **TAGREF** du message AppHelp du fichier exécutable correspondant.</span><span class="sxs-lookup"><span data-stu-id="d9317-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-133">**dwExeCount**</span><span class="sxs-lookup"><span data-stu-id="d9317-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-134">Nombre d’éléments dans **atrExes**.</span><span class="sxs-lookup"><span data-stu-id="d9317-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-135">**dwLayerCount**</span><span class="sxs-lookup"><span data-stu-id="d9317-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-136">Nombre d’éléments dans **atrLayers**.</span><span class="sxs-lookup"><span data-stu-id="d9317-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-137">**Guidid ne**</span><span class="sxs-lookup"><span data-stu-id="d9317-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-138">GUID du dernier fichier exécutable.</span><span class="sxs-lookup"><span data-stu-id="d9317-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="d9317-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-140">Ce paramètre peut être une ou plusieurs des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="d9317-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="d9317-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="d9317-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="d9317-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="d9317-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="d9317-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="d9317-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="d9317-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="d9317-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="d9317-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="d9317-148">**dwCustomSDBMap**</span><span class="sxs-lookup"><span data-stu-id="d9317-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-149">Mappage des bases de données de shims personnalisées.</span><span class="sxs-lookup"><span data-stu-id="d9317-149">A map of the custom shim databases.</span></span> <span data-ttu-id="d9317-150">Les bits correspondants sont définis si **rgGuidDB** est valide.</span><span class="sxs-lookup"><span data-stu-id="d9317-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="d9317-151">**rgGuidDB**</span><span class="sxs-lookup"><span data-stu-id="d9317-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="d9317-152">GUID des bases de données de shims.</span><span class="sxs-lookup"><span data-stu-id="d9317-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="d9317-153">Notez que **sdb \_ Max \_ SDBS** est défini sur 16.</span><span class="sxs-lookup"><span data-stu-id="d9317-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d9317-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d9317-154">Requirements</span></span>



| <span data-ttu-id="d9317-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d9317-155">Requirement</span></span> | <span data-ttu-id="d9317-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="d9317-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="d9317-157">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9317-157">Minimum supported client</span></span><br/> | <span data-ttu-id="d9317-158">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9317-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="d9317-159">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d9317-159">Minimum supported server</span></span><br/> | <span data-ttu-id="d9317-160">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d9317-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9317-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d9317-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9317-162">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="d9317-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




