---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Le \_ format de \_ presse-papiers de la liste de sélection DS CFSTR DSOP \_ \_ fournit un HGLOBAL qui contient une structure de liste de sélection des services d’annuaire \_ \_ . La structure de la liste de sélection des services \_ \_ d’annuaire contient des données sur les éléments sélectionnés dans la boîte de dialogue Sélecteur d’objets d’annuaire.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941967"
---
# <a name="cfstr_dsop_ds_selection_list"></a><span data-ttu-id="7ffd4-104">liste de sélection de CFSTR \_ DSOP \_ DS \_ \_</span><span class="sxs-lookup"><span data-stu-id="7ffd4-104">CFSTR\_DSOP\_DS\_SELECTION\_LIST</span></span>

<dl> <dt>

<span data-ttu-id="7ffd4-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**liste de sélection de CFSTR \_ DSOP \_ DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7ffd4-105"><span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**CFSTR\_DSOP\_DS\_SELECTION\_LIST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7ffd4-106">« \_ liste de sélection CFSTR DSOP \_ DS \_ \_ »</span><span class="sxs-lookup"><span data-stu-id="7ffd4-106">"CFSTR\_DSOP\_DS\_SELECTION\_LIST"</span></span>
</dt> <dt>



<span data-ttu-id="7ffd4-107">Le format de presse-papiers de la **\_ \_ \_ \_ liste de sélection DS CFSTR DSOP** est fourni par l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenu en appelant [**IDsObjectPicker :: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span><span class="sxs-lookup"><span data-stu-id="7ffd4-107">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format is provided by the [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtained by calling [**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog).</span></span> <span data-ttu-id="7ffd4-108">Le format de presse-papiers de la **\_ \_ \_ \_ liste de sélection DS CFSTR DSOP** fournit un **HGLOBAL** qui contient une structure de [**\_ \_ liste de sélection des services d’annuaire**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) .</span><span class="sxs-lookup"><span data-stu-id="7ffd4-108">The **CFSTR\_DSOP\_DS\_SELECTION\_LIST** clipboard format provides an **HGLOBAL** that contains a [**DS\_SELECTION\_LIST**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) structure.</span></span> <span data-ttu-id="7ffd4-109">La structure de la **\_ \_ liste de sélection des services** d’annuaire contient des données sur les éléments sélectionnés dans la boîte de dialogue Sélecteur d’objets d' [Annuaire](directory-object-picker.md) .</span><span class="sxs-lookup"><span data-stu-id="7ffd4-109">The **DS\_SELECTION\_LIST** structure contains data about the items selected in a [Directory Object Picker](directory-object-picker.md) dialog box.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7ffd4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7ffd4-110">Requirements</span></span>



| <span data-ttu-id="7ffd4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7ffd4-111">Requirement</span></span> | <span data-ttu-id="7ffd4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7ffd4-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7ffd4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ffd4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7ffd4-114">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7ffd4-114">Windows Vista</span></span><br/>                                                            |
| <span data-ttu-id="7ffd4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7ffd4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7ffd4-116">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ffd4-116">Windows Server 2008</span></span><br/>                                                      |
| <span data-ttu-id="7ffd4-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="7ffd4-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="7ffd4-118"><dt>Objsel. h</dt></span><span class="sxs-lookup"><span data-stu-id="7ffd4-118"><dt>Objsel.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ffd4-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ffd4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ffd4-120">**\_liste de sélection DS \_**</span><span class="sxs-lookup"><span data-stu-id="7ffd4-120">**DS\_SELECTION\_LIST**</span></span>](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[<span data-ttu-id="7ffd4-121">**IDsObjectPicker::InvokeDialog**</span><span class="sxs-lookup"><span data-stu-id="7ffd4-121">**IDsObjectPicker::InvokeDialog**</span></span>](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[<span data-ttu-id="7ffd4-122">Sélecteur d’objets d’annuaire</span><span class="sxs-lookup"><span data-stu-id="7ffd4-122">Directory Object Picker</span></span>](directory-object-picker.md)
</dt> </dl>

 

