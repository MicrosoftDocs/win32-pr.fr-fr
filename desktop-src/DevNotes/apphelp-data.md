---
description: Contient des informations sur les données AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Structure APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514323"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="f4ea2-103">\_Structure de données APPHELP</span><span class="sxs-lookup"><span data-stu-id="f4ea2-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="f4ea2-104">Contient des informations sur les données AppHelp.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ea2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4ea2-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="f4ea2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f4ea2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4ea2-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-108">Ce paramètre peut prendre l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f4ea2-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ DÉSACTIVER le \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DÉSACTIVER les \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ noui** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annulation de APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ DÉSACTIVER \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DÉSACTIVER la \_ couche** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="f4ea2-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ DÉSACTIVER le \_ pilote** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="f4ea2-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="f4ea2-116">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-117">Ce paramètre peut être APPTYPE \_ None (0).</span><span class="sxs-lookup"><span data-stu-id="f4ea2-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-118">**dwHTMLHelpID**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-119">Identificateur d’aide HTML.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-120">**szAppName**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-121">Nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-122">**trExe**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-123">[**TAGREF**](tagref.md) du fichier exécutable correspondant.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-125">URL du lien AppHelp online.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-126">**szLink**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-127">Texte de lien pour **szURL**.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-128">**szAppTitle**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-129">Titre du message AppHelp.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-130">**szContact**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-131">Informations de contact du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-132">**szDetails**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-133">Message AppHelp détaillé.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-134">**dwData**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-135">Données définies par l’utilisateur et gérées par l’application.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="f4ea2-136">**bSPEntry**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="f4ea2-137">Ce membre a la **valeur true** si cette entrée figure dans la base de données Service Pack et la **valeur false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f4ea2-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f4ea2-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4ea2-138">Requirements</span></span>



| <span data-ttu-id="f4ea2-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4ea2-139">Requirement</span></span> | <span data-ttu-id="f4ea2-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4ea2-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f4ea2-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ea2-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ea2-142">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ea2-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f4ea2-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ea2-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ea2-144">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f4ea2-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f4ea2-145">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4ea2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ea2-146">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="f4ea2-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




