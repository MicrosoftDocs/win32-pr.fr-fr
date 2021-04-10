---
title: Type complexe CertSelection
description: En savoir plus sur le type complexe CertSelection. Ce type détermine la façon dont l’utilisateur sélectionne un certificat.
ms.assetid: f5a37258-8ab0-4736-9721-6c2800769c74
keywords:
- CertSelection type complexe EAPHost
topic_type:
- apiref
api_name:
- CertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba22df8dca61696f214e495542319168183dd2bf
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316475"
---
# <a name="certselection-complex-type"></a><span data-ttu-id="b57a1-105">Type complexe CertSelection</span><span class="sxs-lookup"><span data-stu-id="b57a1-105">CertSelection Complex Type</span></span>

<span data-ttu-id="b57a1-106">Le type complexe **CertSelection** détermine la façon dont l’utilisateur sélectionne un certificat.</span><span class="sxs-lookup"><span data-stu-id="b57a1-106">The **CertSelection** complex type determines how the user selects a certificate.</span></span>

``` syntax
<xs:complexType name="CertSelection">
    <xs:sequence>
        <xs:element name="SimpleCertSelection"
            type="boolean"
            minOccurs="0"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="b57a1-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="b57a1-107">Child elements</span></span>



| <span data-ttu-id="b57a1-108">Élément</span><span class="sxs-lookup"><span data-stu-id="b57a1-108">Element</span></span>                                                                                                     | <span data-ttu-id="b57a1-109">Type</span><span class="sxs-lookup"><span data-stu-id="b57a1-109">Type</span></span>    | <span data-ttu-id="b57a1-110">Description</span><span class="sxs-lookup"><span data-stu-id="b57a1-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                      |
|-------------------------------------------------------------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57a1-111">**SimpleCertSelection**</span><span class="sxs-lookup"><span data-stu-id="b57a1-111">**SimpleCertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) | <span data-ttu-id="b57a1-112">boolean</span><span class="sxs-lookup"><span data-stu-id="b57a1-112">boolean</span></span> | <span data-ttu-id="b57a1-113">A la valeur TRUE par défaut.</span><span class="sxs-lookup"><span data-stu-id="b57a1-113">Is TRUE by default.</span></span> <span data-ttu-id="b57a1-114">Si [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) a la valeur true, EAP-TLS effectue une recherche de certificat simple sans liste déroulante pour la sélection des certificats.</span><span class="sxs-lookup"><span data-stu-id="b57a1-114">If [**SimpleCertSelection**](eaptlsconnectionpropertiesv1schema-simplecertselection-certselection-element.md) is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="b57a1-115">Si **SimpleCertSelection** a la valeur false, EAP-TLS illustre à l’utilisateur le certificat approprié à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="b57a1-115">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b57a1-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b57a1-116">Requirements</span></span>



| <span data-ttu-id="b57a1-117">Role</span><span class="sxs-lookup"><span data-stu-id="b57a1-117">Role</span></span> | <span data-ttu-id="b57a1-118">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="b57a1-118">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="b57a1-119">Client</span><span class="sxs-lookup"><span data-stu-id="b57a1-119">Client</span></span><br/> | <span data-ttu-id="b57a1-120">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b57a1-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b57a1-121">Serveur</span><span class="sxs-lookup"><span data-stu-id="b57a1-121">Server</span></span><br/> | <span data-ttu-id="b57a1-122">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b57a1-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b57a1-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b57a1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57a1-124">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="b57a1-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="b57a1-125">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b57a1-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="b57a1-126">Types complexes de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="b57a1-126">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





