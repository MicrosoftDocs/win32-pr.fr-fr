---
title: CFSTR_DSPROPERTYPAGEINFO (DSClient. h)
description: Le \_ format de presse-papiers CFSTR DSPROPERTYPAGEINFO fournit un HGLOBAL qui contient une structure DSPROPERTYPAGEINFO.
ms.assetid: 84ed1322-fee3-44ee-873e-57586261ff62
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSPROPERTYPAGEINFO
api_location:
- DSClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 259c9addbb3ee41c7b12cd7ea77eb8393b69daaf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032702"
---
# <a name="cfstr_dspropertypageinfo"></a><span data-ttu-id="efc6c-103">CFSTR \_ DSPROPERTYPAGEINFO</span><span class="sxs-lookup"><span data-stu-id="efc6c-103">CFSTR\_DSPROPERTYPAGEINFO</span></span>

<dl> <dt>

<span data-ttu-id="efc6c-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR \_ DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="efc6c-104"><span id="CFSTR_DSPROPERTYPAGEINFO"></span><span id="cfstr_dspropertypageinfo"></span>**CFSTR\_DSPROPERTYPAGEINFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="efc6c-105">"DsPropPageInfo"</span><span class="sxs-lookup"><span data-stu-id="efc6c-105">"DsPropPageInfo"</span></span>
</dt> <dt>



<span data-ttu-id="efc6c-106">Le format de presse-papiers **CFSTR \_ DSPROPERTYPAGEINFO** fournit un **HGLOBAL** qui contient une structure [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) .</span><span class="sxs-lookup"><span data-stu-id="efc6c-106">The **CFSTR\_DSPROPERTYPAGEINFO** clipboard format provides an **HGLOBAL** that contains a [**DSPROPERTYPAGEINFO**](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo) structure.</span></span> <span data-ttu-id="efc6c-107">La structure **DSPROPERTYPAGEINFO** contient la chaîne facultative que l’extension a ajoutée aux valeurs de paramètre **adminPropertySheet** et/ou **shellPropertySheet** lors de l’inscription de l’extension.</span><span class="sxs-lookup"><span data-stu-id="efc6c-107">The **DSPROPERTYPAGEINFO** structure contains the optional string that the extension added to the **adminPropertySheet** and/or **shellPropertySheet** parameter values when the extension was registered.</span></span> <span data-ttu-id="efc6c-108">Pour plus d’informations sur la façon dont cette chaîne est définie, consultez [inscription de l’objet com page de propriétés dans un spécificateur d’affichage](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="efc6c-108">For more information about how this string is set, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="efc6c-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="efc6c-109">Requirements</span></span>



| <span data-ttu-id="efc6c-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="efc6c-110">Requirement</span></span> | <span data-ttu-id="efc6c-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="efc6c-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="efc6c-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efc6c-112">Minimum supported client</span></span><br/> | <span data-ttu-id="efc6c-113">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="efc6c-113">Windows Vista</span></span><br/>                                                              |
| <span data-ttu-id="efc6c-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="efc6c-114">Minimum supported server</span></span><br/> | <span data-ttu-id="efc6c-115">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="efc6c-115">Windows Server 2008</span></span><br/>                                                        |
| <span data-ttu-id="efc6c-116">En-tête</span><span class="sxs-lookup"><span data-stu-id="efc6c-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="efc6c-117"><dt>DSClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="efc6c-117"><dt>DSClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="efc6c-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="efc6c-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="efc6c-119">**DSPROPERTYPAGEINFO**</span><span class="sxs-lookup"><span data-stu-id="efc6c-119">**DSPROPERTYPAGEINFO**</span></span>](/windows/desktop/api/Dsclient/ns-dsclient-dspropertypageinfo)
</dt> <dt>

[<span data-ttu-id="efc6c-120">Inscription de l’objet COM de la page de propriétés dans un spécificateur d’affichage</span><span class="sxs-lookup"><span data-stu-id="efc6c-120">Registering the Property Page COM Object in a Display Specifier</span></span>](registering-the-property-page-com-object-in-a-display-specifier.md)
</dt> </dl>

 

 





