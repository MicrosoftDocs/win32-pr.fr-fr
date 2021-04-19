---
description: La structure EXPERTENUMINFO fournit des informations sur l’expert.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: EXPERTENUMINFO, structure (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517448"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="ba15f-103">EXPERTENUMINFO, structure</span><span class="sxs-lookup"><span data-stu-id="ba15f-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="ba15f-104">La structure **EXPERTENUMINFO** fournit des informations sur l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="ba15f-105">Moniteur réseau alloue de la mémoire pour la structure et la transmet à l’expert lorsqu’il appelle la fonction d' [**expert d’inscription**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="ba15f-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="ba15f-106">Lorsque l’expert reçoit la structure, il doit remplir toutes les informations que Moniteur réseau demandes.</span><span class="sxs-lookup"><span data-stu-id="ba15f-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba15f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba15f-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="ba15f-108">Membres</span><span class="sxs-lookup"><span data-stu-id="ba15f-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ba15f-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="ba15f-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-110">Nom de l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-111">**szVendor**</span><span class="sxs-lookup"><span data-stu-id="ba15f-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-112">Nom du fournisseur qui crée l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="ba15f-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-114">Description de l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-114">Description of the expert.</span></span> <span data-ttu-id="ba15f-115">La valeur du membre **szDescription** peut être **null**.</span><span class="sxs-lookup"><span data-stu-id="ba15f-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="ba15f-116">Si le nom est trop long, il est tronqué dans la configuration de la visionneuse par défaut.</span><span class="sxs-lookup"><span data-stu-id="ba15f-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-117">**Version**</span><span class="sxs-lookup"><span data-stu-id="ba15f-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-118">La valeur doit être égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="ba15f-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-119">**Indicateurs**</span><span class="sxs-lookup"><span data-stu-id="ba15f-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-120">Les indicateurs suivants décrivent l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="ba15f-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba15f-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="ba15f-122">Signification</span><span class="sxs-lookup"><span data-stu-id="ba15f-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="ba15f-123"><dt>**\_indicateur d’énumération expert \_ \_ configurable**</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="ba15f-124">L’expert prend en charge les appels à la méthode [**configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="ba15f-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="ba15f-125"><dt>**\_visionneuse d’indicateurs d’énumération d’experts \_ \_ \_ privée**</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="ba15f-126">L’expert requiert un observateur d’événements privé (non partagé).</span><span class="sxs-lookup"><span data-stu-id="ba15f-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="ba15f-127"><dt>**\_ \_ visionneuse d’indicateur d’enum d' \_ expert \_**</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="ba15f-128">L’expert n’envoie pas de notifications d’événements.</span><span class="sxs-lookup"><span data-stu-id="ba15f-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="ba15f-129"><dt>**\_indicateur d’énumération expert \_ \_ ajouter \_ \_ à \_ RMC \_ en \_ Résumé**</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="ba15f-130">Quand le focus se trouve dans le volet Résumé, l’expert s’affiche dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba15f-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="ba15f-131"><dt>**\_indicateur d’énumération \_ d’experts \_ ajouter \_ \_ à \_ RMC \_ en \_ détail**</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="ba15f-132">Quand le focus se trouve dans le volet d’informations, l’expert s’affiche dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="ba15f-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="ba15f-133">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="ba15f-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-134">Handle vers l’expert.</span><span class="sxs-lookup"><span data-stu-id="ba15f-134">Handle to the expert.</span></span> <span data-ttu-id="ba15f-135">Lorsque la structure **EXPERTENUMINFO** est utilisée pour inscrire un expert, le paramètre est ignoré.</span><span class="sxs-lookup"><span data-stu-id="ba15f-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="ba15f-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-137">Membre privé ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ba15f-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-138">**hModule**</span><span class="sxs-lookup"><span data-stu-id="ba15f-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-139">Membre privé ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ba15f-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-140">**pRegisterProc**</span><span class="sxs-lookup"><span data-stu-id="ba15f-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-141">Membre privé ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ba15f-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-142">**pConfigProc**</span><span class="sxs-lookup"><span data-stu-id="ba15f-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-143">Membre privé ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ba15f-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="ba15f-144">**pRunProc**</span><span class="sxs-lookup"><span data-stu-id="ba15f-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="ba15f-145">Membre privé ; n’utilisez pas.</span><span class="sxs-lookup"><span data-stu-id="ba15f-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ba15f-146">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba15f-146">Requirements</span></span>



| <span data-ttu-id="ba15f-147">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba15f-147">Requirement</span></span> | <span data-ttu-id="ba15f-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba15f-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ba15f-149">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba15f-149">Minimum supported client</span></span><br/> | <span data-ttu-id="ba15f-150">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba15f-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ba15f-151">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ba15f-151">Minimum supported server</span></span><br/> | <span data-ttu-id="ba15f-152">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ba15f-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ba15f-153">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba15f-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba15f-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba15f-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




