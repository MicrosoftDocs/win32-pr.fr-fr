---
title: Élément SimpleCertSelection (CertSelection)
description: En savoir plus sur l’élément SimpleCertSelection (CertSelection). Cet élément détermine la façon dont l’utilisateur sélectionne un certificat.
ms.assetid: 28454877-fd07-4b47-9544-f2b4e91c6651
keywords:
- Élément SimpleCertSelection EAPHost
topic_type:
- apiref
api_name:
- SimpleCertSelection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 30af9872f7583232e91b037c5b8961e18c7ce863
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104031869"
---
# <a name="simplecertselection-certselection-element"></a><span data-ttu-id="c1da2-105">Élément SimpleCertSelection (CertSelection)</span><span class="sxs-lookup"><span data-stu-id="c1da2-105">SimpleCertSelection (CertSelection) Element</span></span>

<span data-ttu-id="c1da2-106">L’élément **SimpleCertSelection (CertSelection)** détermine la façon dont l’utilisateur sélectionne un certificat.</span><span class="sxs-lookup"><span data-stu-id="c1da2-106">The **SimpleCertSelection (CertSelection)** element determines how the user selects a certificate.</span></span>

``` syntax
<xs:element name="SimpleCertSelection"
    type="boolean"
 />
```

<span data-ttu-id="c1da2-107">L’élément **SimpleCertSelection** est défini par le type complexe [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1da2-107">The **SimpleCertSelection** element is defined by the [**CertSelection**](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="c1da2-108">Notes</span><span class="sxs-lookup"><span data-stu-id="c1da2-108">Remarks</span></span>

<span data-ttu-id="c1da2-109">**SimpleCertSelection** a la valeur true par défaut.</span><span class="sxs-lookup"><span data-stu-id="c1da2-109">**SimpleCertSelection** is TRUE by default.</span></span> <span data-ttu-id="c1da2-110">Si **SimpleCertSelection** a la valeur true, EAP-TLS effectue une recherche de certificat simple sans liste déroulante pour la sélection des certificats.</span><span class="sxs-lookup"><span data-stu-id="c1da2-110">If **SimpleCertSelection** is TRUE, EAP-TLS performs a simple certificate search without any drop-down lists for the selection of certificates.</span></span> <span data-ttu-id="c1da2-111">Si **SimpleCertSelection** a la valeur false, EAP-TLS illustre à l’utilisateur le certificat approprié à sélectionner.</span><span class="sxs-lookup"><span data-stu-id="c1da2-111">If **SimpleCertSelection** is FALSE, EAP-TLS illustrates to the user the suitable certificate to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="c1da2-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c1da2-112">Requirements</span></span>



| <span data-ttu-id="c1da2-113">Role</span><span class="sxs-lookup"><span data-stu-id="c1da2-113">Role</span></span> | <span data-ttu-id="c1da2-114">Système d’exploitation minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c1da2-114">Minimum supported OS</span></span> |
|------|----------------------|
| <span data-ttu-id="c1da2-115">Client</span><span class="sxs-lookup"><span data-stu-id="c1da2-115">Client</span></span><br/> | <span data-ttu-id="c1da2-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1da2-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c1da2-117">Serveur</span><span class="sxs-lookup"><span data-stu-id="c1da2-117">Server</span></span><br/> | <span data-ttu-id="c1da2-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c1da2-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c1da2-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c1da2-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="c1da2-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="c1da2-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c1da2-121">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="c1da2-121">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md)
</dt> <dt>

<span data-ttu-id="c1da2-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="c1da2-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c1da2-123">**CertificateStore (CredentialsSourceParameters)**</span><span class="sxs-lookup"><span data-stu-id="c1da2-123">**CertificateStore (CredentialsSourceParameters)**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md)
<span data-ttu-id="c1da2-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="c1da2-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="c1da2-125">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="c1da2-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="c1da2-126">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1da2-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="c1da2-127">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="c1da2-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





