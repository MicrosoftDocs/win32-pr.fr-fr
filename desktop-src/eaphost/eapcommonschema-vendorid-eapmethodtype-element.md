---
title: Élément ID de l’élément (EapMethodType)
description: Fait référence au fournisseur qui a défini la méthode si l’élément de type (EapMethodType) est 254 (méthode EAP développée).
ms.assetid: 14992940-2fe5-4f85-91c0-1f61345ee90f
keywords:
- Élément ID de l’élément EAPHost
topic_type:
- apiref
api_name:
- VendorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9091cdbd7620baf6ec5dc893bd2100b2f04585ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508650"
---
# <a name="vendorid-eapmethodtype-element"></a><span data-ttu-id="f3db9-104">Élément ID de l’élément (EapMethodType)</span><span class="sxs-lookup"><span data-stu-id="f3db9-104">VendorId (EapMethodType) Element</span></span>

<span data-ttu-id="f3db9-105">L’élément **ID de fournisseur (EapMethodType)** fait référence au fournisseur qui a défini la méthode si l’élément de [**type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) est 254 (méthode EAP développée).</span><span class="sxs-lookup"><span data-stu-id="f3db9-105">The **VendorId (EapMethodType)** element refers to the vendor who defined the method if the [**Type (EapMethodType)**](eapcommonschema-type-eapmethodtype-element.md) element is 254 (an expanded EAP method).</span></span>

<span data-ttu-id="f3db9-106">Le **ID** de l’argument est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f3db9-106">The **VendorId** is optional.</span></span> <span data-ttu-id="f3db9-107">S’il est utilisé, le **ID** de certificat est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="f3db9-107">If used, the **VendorId** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="f3db9-108">L’élément **ID** de type est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="f3db9-108">The **VendorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3db9-109">Notes</span><span class="sxs-lookup"><span data-stu-id="f3db9-109">Remarks</span></span>

<span data-ttu-id="f3db9-110">Il n’est pas [**nécessaire que les**](eapcommonschema-authorid-eapmethodtype-element.md) éléments de réfaut de réfaut et **ID** de données soient identiques pour une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="f3db9-110">The [**AuthorId**](eapcommonschema-authorid-eapmethodtype-element.md) and **VendorId** elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3db9-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f3db9-111">Requirements</span></span>



| <span data-ttu-id="f3db9-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f3db9-112">Requirement</span></span> | <span data-ttu-id="f3db9-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="f3db9-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f3db9-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3db9-114">Minimum supported client</span></span><br/> | <span data-ttu-id="f3db9-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3db9-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f3db9-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f3db9-116">Minimum supported server</span></span><br/> | <span data-ttu-id="f3db9-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f3db9-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f3db9-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f3db9-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f3db9-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f3db9-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f3db9-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="f3db9-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="f3db9-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="f3db9-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f3db9-122">Schéma eapcommon</span><span class="sxs-lookup"><span data-stu-id="f3db9-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





