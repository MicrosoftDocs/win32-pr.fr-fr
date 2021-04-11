---
title: Structure MPRESOURCE_INFO (MpClient. h)
description: Structure des informations sur les ressources.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Fonctionnalités d’environnement Windows héritées de la structure MPRESOURCE_INFO
- PMPRESOURCE_INFO des fonctionnalités d’environnement Windows héritées du pointeur de structure
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942396"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="77da7-105">\_Structure d’informations MPRESOURCE</span><span class="sxs-lookup"><span data-stu-id="77da7-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="77da7-106">Structure des informations sur les ressources.</span><span class="sxs-lookup"><span data-stu-id="77da7-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="77da7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77da7-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="77da7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="77da7-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="77da7-109">**Mode**</span><span class="sxs-lookup"><span data-stu-id="77da7-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="77da7-110">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="77da7-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="77da7-111">Identificateur de schéma de ressource tel que « file » ou « dir ».</span><span class="sxs-lookup"><span data-stu-id="77da7-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="77da7-112">**Chemin d’accès**</span><span class="sxs-lookup"><span data-stu-id="77da7-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="77da7-113">Type : **MP \_ MIDL \_ String** de type LPWStr</span><span class="sxs-lookup"><span data-stu-id="77da7-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="77da7-114">Chemin d’accès absolu de la ressource, basé sur le **schéma**.</span><span class="sxs-lookup"><span data-stu-id="77da7-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="77da7-115">**Classe**</span><span class="sxs-lookup"><span data-stu-id="77da7-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="77da7-116">Type : **MPRESOURCE, \_ classe**</span><span class="sxs-lookup"><span data-stu-id="77da7-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="77da7-117">Ce champ est défini lorsque la ressource est identifiée dans le cadre de la menace.</span><span class="sxs-lookup"><span data-stu-id="77da7-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="77da7-118">Elle spécifie la classe de ressource, principalement concrète et latente.</span><span class="sxs-lookup"><span data-stu-id="77da7-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="77da7-119">Il peut s’agir d’une combinaison de ces valeurs possibles :</span><span class="sxs-lookup"><span data-stu-id="77da7-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="77da7-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="77da7-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="77da7-121">Signification</span><span class="sxs-lookup"><span data-stu-id="77da7-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="77da7-122">Pack d’e <dt>**\_ Classe de ressources \_ \_ inconnue**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="77da7-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="77da7-123">Pack d’e <dt>**\_ Classe de ressources 0x0001 \_ \_ concrète**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77da7-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="77da7-124">S’exclut mutuellement avec la **\_ classe de ressource MP \_ \_ latente**.</span><span class="sxs-lookup"><span data-stu-id="77da7-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="77da7-125">Pack d’e <dt>**\_ Classe de ressource la0x0002 \_ \_ latente**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77da7-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="77da7-126">S’exclut mutuellement avec la **\_ classe de ressources MP \_ \_ concrète**.</span><span class="sxs-lookup"><span data-stu-id="77da7-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="77da7-127">Pack d’e <dt>**\_ \_Exemple de \_ \_ fichier de classe de ressources**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="77da7-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="77da7-128">Pack d’e <dt>**\_ 0x0100 \_ \_ partagé**</dt> de la classe de ressources <dt></dt></span><span class="sxs-lookup"><span data-stu-id="77da7-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77da7-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77da7-129">Requirements</span></span>



| <span data-ttu-id="77da7-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77da7-130">Requirement</span></span> | <span data-ttu-id="77da7-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="77da7-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77da7-132">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77da7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="77da7-133">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77da7-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="77da7-134">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77da7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="77da7-135">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="77da7-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77da7-136">En-tête</span><span class="sxs-lookup"><span data-stu-id="77da7-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="77da7-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="77da7-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





