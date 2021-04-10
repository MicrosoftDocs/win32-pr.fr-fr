---
title: Élément d’auteur d’EapMethodType
description: En savoir plus sur l’élément de reEapMethodTypement. L’élément de réutilisation (EapMethodType) fait référence à l’auteur de la méthode.
ms.assetid: 1eb16a50-25b8-4883-b9ff-fde329d8dd81
keywords:
- Élément d’auteur EAPHost
topic_type:
- apiref
api_name:
- AuthorId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1c9a756d8ad1fc88154d3d99d4304de6dd50166b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941374"
---
# <a name="authorid-eapmethodtype-element"></a><span data-ttu-id="32c50-105">Élément d’auteur d’EapMethodType</span><span class="sxs-lookup"><span data-stu-id="32c50-105">AuthorId (EapMethodType) Element</span></span>

<span data-ttu-id="32c50-106">L’élément de réutilisation **(EapMethodType)** fait référence à l’auteur de la méthode.</span><span class="sxs-lookup"><span data-stu-id="32c50-106">The **AuthorId (EapMethodType)** element refers to the method author.</span></span>

<span data-ttu-id="32c50-107">L’identificateur d’auteur est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="32c50-107">The AuthorId is a unique number issued by the Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="AuthorId"
    type="unsignedInt"
 />
```

<span data-ttu-id="32c50-108">L’élément d’un élément d' **auteur** est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="32c50-108">The **AuthorId** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="32c50-109">Notes</span><span class="sxs-lookup"><span data-stu-id="32c50-109">Remarks</span></span>

<span data-ttu-id="32c50-110">Il n’est pas **nécessaire que les** éléments de réfaut de réfaut et [**ID**](eapcommonschema-vendorid-eapmethodtype-element.md) de données soient identiques pour une méthode particulière.</span><span class="sxs-lookup"><span data-stu-id="32c50-110">The **AuthorId** and [**VendorId**](eapcommonschema-vendorid-eapmethodtype-element.md) elements do not need to be the same for a particular method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32c50-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32c50-111">Requirements</span></span>



| <span data-ttu-id="32c50-112">Role</span><span class="sxs-lookup"><span data-stu-id="32c50-112">Role</span></span> | <span data-ttu-id="32c50-113">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="32c50-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="32c50-114">Client</span><span class="sxs-lookup"><span data-stu-id="32c50-114">Client</span></span><br/> | <span data-ttu-id="32c50-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32c50-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="32c50-116">Serveur</span><span class="sxs-lookup"><span data-stu-id="32c50-116">Server</span></span><br/> | <span data-ttu-id="32c50-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="32c50-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32c50-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32c50-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="32c50-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="32c50-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="32c50-120">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="32c50-120">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="32c50-121">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="32c50-121">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="32c50-122">Schéma eapcommon</span><span class="sxs-lookup"><span data-stu-id="32c50-122">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





