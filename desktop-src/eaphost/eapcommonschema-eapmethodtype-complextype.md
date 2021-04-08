---
title: Type complexe EapMethodType
description: Définit les éléments qui identifient de manière unique un type de méthode EAP, un ID de type, un type de caractère et un ID d’auteur unique.
ms.assetid: 3ef96187-7376-438d-9d47-a87d5a6c9b8b
keywords:
- EapMethodType type complexe EAPHost
topic_type:
- apiref
api_name:
- EapMethodType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cea2448111266696398d1581aaecdbec2fb5859e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741844"
---
# <a name="eapmethodtype-complex-type"></a><span data-ttu-id="fa340-104">Type complexe EapMethodType</span><span class="sxs-lookup"><span data-stu-id="fa340-104">EapMethodType Complex Type</span></span>

<span data-ttu-id="fa340-105">Le type complexe **EapMethodType** définit les éléments qui identifient de façon unique une méthode EAP unique : type, [](eapcommonschema-vendortype-eapmethodtype-element.md)ID de [**type, type de type**](eapcommonschema-type-eapmethodtype-element.md)et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md)d' [**auteur**](eapcommonschema-authorid-eapmethodtype-element.md).</span><span class="sxs-lookup"><span data-stu-id="fa340-105">The **EapMethodType** complex type defines the elements that uniquely identify a single EAP method: [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md), [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md), and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md).</span></span>

<span data-ttu-id="fa340-106">Le [**type**](eapcommonschema-type-eapmethodtype-element.md) et l’ID d' [**auteur**](eapcommonschema-authorid-eapmethodtype-element.md) sont des éléments obligatoires, alors que les [**types de type**](eapcommonschema-vendortype-eapmethodtype-element.md) et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de l’élément sont requis uniquement lorsque l’élément de **type** est 254 (méthode EAP développée).</span><span class="sxs-lookup"><span data-stu-id="fa340-106">[**Type**](eapcommonschema-type-eapmethodtype-element.md) and [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) are mandatory elements, whereas [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) are required only when the **Type** element is 254 (an expanded EAP method).</span></span>

``` syntax
<xs:complexType name="EapMethodType">
    <xs:sequence>
        <xs:element name="Type"
            type="unsignedByte"
         />
        <xs:element name="VendorId"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="VendorType"
            type="unsignedInt"
            default="0"
            minOccurs="0"
         />
        <xs:element name="AuthorId"
            type="unsignedInt"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="fa340-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="fa340-107">Child elements</span></span>



| <span data-ttu-id="fa340-108">Élément</span><span class="sxs-lookup"><span data-stu-id="fa340-108">Element</span></span>                                                                | <span data-ttu-id="fa340-109">Type</span><span class="sxs-lookup"><span data-stu-id="fa340-109">Type</span></span>         | <span data-ttu-id="fa340-110">Description</span><span class="sxs-lookup"><span data-stu-id="fa340-110">Description</span></span>                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fa340-111">**Faut**</span><span class="sxs-lookup"><span data-stu-id="fa340-111">**AuthorId**</span></span>](eapcommonschema-authorid-eapmethodtype-element.md)     | <span data-ttu-id="fa340-112">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fa340-112">unsignedInt</span></span>  | <span data-ttu-id="fa340-113">Fait référence à l’auteur de la méthode.</span><span class="sxs-lookup"><span data-stu-id="fa340-113">Refers to the method author.</span></span> <br/>                                                                                                                                                                                                                 |
| [<span data-ttu-id="fa340-114">**Entrer**</span><span class="sxs-lookup"><span data-stu-id="fa340-114">**Type**</span></span>](eapcommonschema-type-eapmethodtype-element.md)             | <span data-ttu-id="fa340-115">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="fa340-115">unsignedByte</span></span> | <span data-ttu-id="fa340-116">Fait référence au type de méthode EAP.</span><span class="sxs-lookup"><span data-stu-id="fa340-116">Refers to the EAP method type.</span></span> <br/>                                                                                                                                                                                                               |
| [<span data-ttu-id="fa340-117">**VendorId**</span><span class="sxs-lookup"><span data-stu-id="fa340-117">**VendorId**</span></span>](eapcommonschema-vendorid-eapmethodtype-element.md)     | <span data-ttu-id="fa340-118">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fa340-118">unsignedInt</span></span>  | <span data-ttu-id="fa340-119">Fait référence au fournisseur qui a défini la méthode-si l’élément [**type**](eapcommonschema-type-eapmethodtype-element.md) est 254 (méthode EAP développée).</span><span class="sxs-lookup"><span data-stu-id="fa340-119">Refers to the vendor who defined the method - if the [**Type**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span> <span data-ttu-id="fa340-120">Le [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de l’argument est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fa340-120">The [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) is optional.</span></span> <br/> |
| [<span data-ttu-id="fa340-121">**#D3**</span><span class="sxs-lookup"><span data-stu-id="fa340-121">**VendorType**</span></span>](eapcommonschema-vendortype-eapmethodtype-element.md) | <span data-ttu-id="fa340-122">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="fa340-122">unsignedInt</span></span>  | <span data-ttu-id="fa340-123">Est le type défini par le fournisseur pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="fa340-123">Is the vendor defined type for the method.</span></span> <span data-ttu-id="fa340-124">Le [**module**](eapcommonschema-vendortype-eapmethodtype-element.md) de la est facultatif.</span><span class="sxs-lookup"><span data-stu-id="fa340-124">The [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) is optional.</span></span> <br/>                                                                                                           |



## <a name="remarks"></a><span data-ttu-id="fa340-125">Notes</span><span class="sxs-lookup"><span data-stu-id="fa340-125">Remarks</span></span>

<span data-ttu-id="fa340-126">Il n’est pas [**nécessaire que les**](eapcommonschema-authorid-eapmethodtype-element.md) éléments de réfaut de réfaut et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de données soient identiques pour une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="fa340-126">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

<span data-ttu-id="fa340-127">Les [**éléments de**](eapcommonschema-authorid-eapmethodtype-element.md)réfaut-réid, type, [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de [**certificat et**](eapcommonschema-vendortype-eapmethodtype-element.md) [**type**](eapcommonschema-type-eapmethodtype-element.md)d’élément sont chacun un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="fa340-127">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md), [**Type**](eapcommonschema-type-eapmethodtype-element.md), [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) and [**VendorType**](eapcommonschema-vendortype-eapmethodtype-element.md) elements are each a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

## <a name="requirements"></a><span data-ttu-id="fa340-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fa340-128">Requirements</span></span>



| <span data-ttu-id="fa340-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fa340-129">Requirement</span></span> | <span data-ttu-id="fa340-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="fa340-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fa340-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa340-131">Minimum supported client</span></span><br/> | <span data-ttu-id="fa340-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa340-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fa340-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fa340-133">Minimum supported server</span></span><br/> | <span data-ttu-id="fa340-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fa340-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fa340-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa340-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fa340-136">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="fa340-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="fa340-137">Schéma eapcommon</span><span class="sxs-lookup"><span data-stu-id="fa340-137">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





