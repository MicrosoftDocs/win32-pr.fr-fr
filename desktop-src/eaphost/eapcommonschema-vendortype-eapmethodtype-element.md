---
title: Élément de EapMethodType ()
description: En savoir plus sur l’élément de la EapMethodType. Cet élément est le type défini par le fournisseur pour la méthode.
ms.assetid: baa43e60-05e2-43f9-bb38-896725be76b4
keywords:
- Élément de la façon EAPHost
topic_type:
- apiref
api_name:
- VendorType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29030672cea0deff59f7f3026dcac98d6ff1c178
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104463695"
---
# <a name="vendortype-eapmethodtype-element"></a><span data-ttu-id="a1b37-105">Élément de EapMethodType ()</span><span class="sxs-lookup"><span data-stu-id="a1b37-105">VendorType (EapMethodType) Element</span></span>

<span data-ttu-id="a1b37-106">L’élément type de fournisseur **(EapMethodType)** est le type défini par le fournisseur pour la méthode.</span><span class="sxs-lookup"><span data-stu-id="a1b37-106">The **VendorType (EapMethodType)** element is the vendor defined type for the method.</span></span>

<span data-ttu-id="a1b37-107">L' **élément** un élément de la est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a1b37-107">The **VendorType** element is optional.</span></span> <span data-ttu-id="a1b37-108">Si elle est utilisée, le **numéro de la** valeur est un numéro unique émis par l’IANA (Internet Assigned Numbers Authority).</span><span class="sxs-lookup"><span data-stu-id="a1b37-108">If used, the **VendorType** is a unique number issued by Internet Assigned Numbers Authority (IANA).</span></span>

``` syntax
<xs:element name="VendorType"
    type="unsignedInt"
 />
```

<span data-ttu-id="a1b37-109">L' **élément type** est défini par le type complexe [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a1b37-109">The **VendorType** element is defined by the [**EapMethodType**](eapcommonschema-eapmethodtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1b37-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a1b37-110">Requirements</span></span>



| <span data-ttu-id="a1b37-111">Role</span><span class="sxs-lookup"><span data-stu-id="a1b37-111">Role</span></span> | <span data-ttu-id="a1b37-112">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="a1b37-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="a1b37-113">Client</span><span class="sxs-lookup"><span data-stu-id="a1b37-113">Client</span></span><br/> | <span data-ttu-id="a1b37-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1b37-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a1b37-115">Serveur</span><span class="sxs-lookup"><span data-stu-id="a1b37-115">Server</span></span><br/> | <span data-ttu-id="a1b37-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a1b37-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a1b37-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a1b37-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="a1b37-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a1b37-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a1b37-119">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="a1b37-119">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)
</dt> <dt>

[<span data-ttu-id="a1b37-120">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="a1b37-120">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a1b37-121">Schéma eapcommon</span><span class="sxs-lookup"><span data-stu-id="a1b37-121">eapcommon Schema</span></span>](eapcommonschema-schema.md)
</dt> </dl>

 

 





