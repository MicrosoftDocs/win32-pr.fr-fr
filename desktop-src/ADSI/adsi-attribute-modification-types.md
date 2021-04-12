---
title: Types de modification des attributs ADSI (IADs. h)
description: Utilisé avec le membre dwControlCode de la \_ \_ structure info attr ADS pour spécifier le type d’opération à effectuer lorsqu’un attribut est modifié à l’aide de la méthode IDirectoryObject SetObjectAttributes.
ms.assetid: e9a454c8-e067-4730-97f4-85c4f5889e05
ms.tgt_platform: multiple
keywords:
- types de modification d’attribut ADSI
topic_type:
- apiref
api_name:
- ADS_ATTR_CLEAR
- ADS_ATTR_UPDATE
- ADS_ATTR_APPEND
- ADS_ATTR_DELETE
api_location:
- Iads.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21a739241fd52a7d45d58a1b36bb7de838234d6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032572"
---
# <a name="adsi-attribute-modification-types"></a><span data-ttu-id="18ef0-104">Types de modification des attributs ADSI</span><span class="sxs-lookup"><span data-stu-id="18ef0-104">ADSI Attribute Modification Types</span></span>

<span data-ttu-id="18ef0-105">Les constantes suivantes sont utilisées avec le membre **dwControlCode** de la structure [**\_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) pour spécifier le type d’opération à effectuer lorsqu’un attribut est modifié à l’aide de la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="18ef0-105">The following constants are used with the **dwControlCode** member of [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure to specify the type of operation to be performed when an attribute is modified with the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="18ef0-106">Pour plus d’informations sur l’utilisation de ces valeurs, consultez [modification des attributs avec ADSI](modifying-attributes-with-adsi.md).</span><span class="sxs-lookup"><span data-stu-id="18ef0-106">For more information about using these values, see [Modifying Attributes with ADSI](modifying-attributes-with-adsi.md).</span></span>

<dl> <dt>

<span data-ttu-id="18ef0-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**\_attr- \_ effacer les annonces**</span><span class="sxs-lookup"><span data-stu-id="18ef0-107"><span id="ADS_ATTR_CLEAR"></span><span id="ads_attr_clear"></span>**ADS\_ATTR\_CLEAR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ef0-108">1</span><span class="sxs-lookup"><span data-stu-id="18ef0-108">1</span></span>
</dt> <dt>



<span data-ttu-id="18ef0-109">Entraîne la suppression de toutes les valeurs d’attribut d’un objet.</span><span class="sxs-lookup"><span data-stu-id="18ef0-109">Causes all attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ef0-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**\_ \_ mise à jour de l’attr ads**</span><span class="sxs-lookup"><span data-stu-id="18ef0-110"><span id="ADS_ATTR_UPDATE"></span><span id="ads_attr_update"></span>**ADS\_ATTR\_UPDATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ef0-111">2</span><span class="sxs-lookup"><span data-stu-id="18ef0-111">2</span></span>
</dt> <dt>



<span data-ttu-id="18ef0-112">Entraîne la mise à jour des valeurs d’attribut spécifiées.</span><span class="sxs-lookup"><span data-stu-id="18ef0-112">Causes the specified attribute values to be updated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ef0-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**\_Ajout d’attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="18ef0-113"><span id="ADS_ATTR_APPEND"></span><span id="ads_attr_append"></span>**ADS\_ATTR\_APPEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ef0-114">3</span><span class="sxs-lookup"><span data-stu-id="18ef0-114">3</span></span>
</dt> <dt>



<span data-ttu-id="18ef0-115">Entraîne l’ajout des valeurs d’attribut spécifiées aux valeurs d’attribut existantes.</span><span class="sxs-lookup"><span data-stu-id="18ef0-115">Causes the specified attribute values to be appended to the existing attribute values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="18ef0-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**suppression de l' \_ attr ADS \_**</span><span class="sxs-lookup"><span data-stu-id="18ef0-116"><span id="ADS_ATTR_DELETE"></span><span id="ads_attr_delete"></span>**ADS\_ATTR\_DELETE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="18ef0-117">4</span><span class="sxs-lookup"><span data-stu-id="18ef0-117">4</span></span>
</dt> <dt>



<span data-ttu-id="18ef0-118">Entraîne la suppression des valeurs d’attribut spécifiées d’un objet.</span><span class="sxs-lookup"><span data-stu-id="18ef0-118">Causes the specified attribute values to be removed from an object.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="18ef0-119">Notes</span><span class="sxs-lookup"><span data-stu-id="18ef0-119">Remarks</span></span>

<span data-ttu-id="18ef0-120">Ces constantes sont destinées à être utilisées avec la [**structure \_ \_ info attr ADS**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) dans la méthode [**IDirectoryObject :: SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) .</span><span class="sxs-lookup"><span data-stu-id="18ef0-120">These constants are intended to be used with the [**ADS\_ATTR\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_attr_info) structure in the [**IDirectoryObject::SetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes) method.</span></span> <span data-ttu-id="18ef0-121">Ces constantes ne doivent pas être confondues avec les membres de l’énumération enum de l' [**\_ opération de propriété \_ \_ ADS**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) , qui sont destinés à être utilisés avec la méthode [**IADs ::P Utex**](/windows/desktop/api/Iads/nf-iads-iads-putex) .</span><span class="sxs-lookup"><span data-stu-id="18ef0-121">These constants should not be confused with members of the [**ADS\_PROPERTY\_OPERATION\_ENUM**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) enumeration, which are intended to be used with the [**IADs::PutEx**](/windows/desktop/api/Iads/nf-iads-iads-putex) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="18ef0-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="18ef0-122">Requirements</span></span>



| <span data-ttu-id="18ef0-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="18ef0-123">Requirement</span></span> | <span data-ttu-id="18ef0-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="18ef0-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="18ef0-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ef0-125">Minimum supported client</span></span><br/> | <span data-ttu-id="18ef0-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18ef0-126">Windows Vista</span></span><br/>                                                          |
| <span data-ttu-id="18ef0-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="18ef0-127">Minimum supported server</span></span><br/> | <span data-ttu-id="18ef0-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="18ef0-128">Windows Server 2008</span></span><br/>                                                    |
| <span data-ttu-id="18ef0-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="18ef0-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="18ef0-130"><dt>IADs. h</dt></span><span class="sxs-lookup"><span data-stu-id="18ef0-130"><dt>Iads.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18ef0-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="18ef0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18ef0-132">**\_infos attr \_ ads**</span><span class="sxs-lookup"><span data-stu-id="18ef0-132">**ADS\_ATTR\_INFO**</span></span>](/windows/desktop/api/Iads/ns-iads-ads_attr_info)
</dt> <dt>

[<span data-ttu-id="18ef0-133">**IDirectoryObject::SetObjectAttributes**</span><span class="sxs-lookup"><span data-stu-id="18ef0-133">**IDirectoryObject::SetObjectAttributes**</span></span>](/windows/desktop/api/Iads/nf-iads-idirectoryobject-setobjectattributes)
</dt> <dt>

[<span data-ttu-id="18ef0-134">Modification d’attributs avec ADSI</span><span class="sxs-lookup"><span data-stu-id="18ef0-134">Modifying Attributes with ADSI</span></span>](modifying-attributes-with-adsi.md)
</dt> </dl>

 

 





