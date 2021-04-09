---
title: CFSTR_DS_DISPLAY_SPEC_OPTIONS (DSClient. h)
description: Le \_ format de \_ presse-papiers des options de spécification de CFSTR DS affiche \_ \_ un HGLOBAL qui contient une structure DSDISPLAYSPECOPTIONS.
ms.assetid: 98e033e4-14fe-44ed-83d5-a97e00ecce4c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DS_DISPLAY_SPEC_OPTIONS
- CFSTR_DSDISPLAYSPECOPTIONS
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d81f3a229971be5ecfb9ec2c86e166af27f94e01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032705"
---
# <a name="cfstr_ds_display_spec_options"></a><span data-ttu-id="17039-103">CFSTR \_ DS \_ affichent les \_ Options des spécifications \_</span><span class="sxs-lookup"><span data-stu-id="17039-103">CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS</span></span>

<dl> <dt>

<span data-ttu-id="17039-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR \_ DS \_ affichent les \_ Options des spécifications \_**</span><span class="sxs-lookup"><span data-stu-id="17039-104"><span id="CFSTR_DS_DISPLAY_SPEC_OPTIONS"></span><span id="cfstr_ds_display_spec_options"></span>**CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="17039-105">"DsDisplaySpecOptions"</span><span class="sxs-lookup"><span data-stu-id="17039-105">"DsDisplaySpecOptions"</span></span>
</dt> <dt>



<span data-ttu-id="17039-106">Les utilisateurs et ordinateurs Active Directory, les Active Directory les sites et les services et les composants logiciels enfichables domaines et approbations Active Directory prennent en charge le format de presse-papiers **CFSTR \_ DS \_ Display \_ \_** .</span><span class="sxs-lookup"><span data-stu-id="17039-106">The Active Directory Users and Computers, the Active Directory Sites and Services, and the Active Directory Domains and Trusts snap-ins support the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span> <span data-ttu-id="17039-107">Le format de presse-papiers des **options de spécification de CFSTR \_ DS \_ \_ \_ affiche** un **HGLOBAL** qui contient une structure [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) .</span><span class="sxs-lookup"><span data-stu-id="17039-107">The **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format provides an **HGLOBAL** that contains a [**DSDISPLAYSPECOPTIONS**](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions) structure.</span></span> <span data-ttu-id="17039-108">Le **DSDISPLAYSPECOPTIONS** contient des données de configuration utilisables par l’extension.</span><span class="sxs-lookup"><span data-stu-id="17039-108">The **DSDISPLAYSPECOPTIONS** contains configuration data for use by the extension.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="17039-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR \_ DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="17039-109"><span id="CFSTR_DSDISPLAYSPECOPTIONS"></span><span id="cfstr_dsdisplayspecoptions"></span>**CFSTR\_DSDISPLAYSPECOPTIONS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="17039-110">Le format du presse-papiers **CFSTR \_ DSDISPLAYSPECOPTIONS** est identique au format du presse-papiers des **Options des spécifications d’affichage de CFSTR \_ \_ \_ \_ DS** .</span><span class="sxs-lookup"><span data-stu-id="17039-110">The **CFSTR\_DSDISPLAYSPECOPTIONS** clipboard format is identical to the **CFSTR\_DS\_DISPLAY\_SPEC\_OPTIONS** clipboard format.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="17039-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="17039-111">Requirements</span></span>



| <span data-ttu-id="17039-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="17039-112">Requirement</span></span> | <span data-ttu-id="17039-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="17039-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="17039-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17039-114">Minimum supported client</span></span><br/> | <span data-ttu-id="17039-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17039-115">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="17039-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="17039-116">Minimum supported server</span></span><br/> | <span data-ttu-id="17039-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17039-117">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="17039-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="17039-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="17039-119"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="17039-119"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17039-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="17039-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17039-121">**DSDISPLAYSPECOPTIONS**</span><span class="sxs-lookup"><span data-stu-id="17039-121">**DSDISPLAYSPECOPTIONS**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dsdisplayspecoptions)
</dt> </dl>

 

 





