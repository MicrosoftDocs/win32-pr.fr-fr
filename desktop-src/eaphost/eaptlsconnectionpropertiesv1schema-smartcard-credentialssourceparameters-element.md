---
title: Élément SmartCard (CredentialsSourceParameters)
description: Indique que le protocole EAP-TLS doit lire le certificat à partir de la carte à puce.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Élément SmartCard EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512817"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="23afd-104">Élément SmartCard (CredentialsSourceParameters)</span><span class="sxs-lookup"><span data-stu-id="23afd-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="23afd-105">L’élément **Smartcard (CredentialsSourceParameters)** indique que le protocole EAP-TLS doit lire le certificat à partir de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="23afd-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="23afd-106">L’élément de **carte à puce** est défini par le type complexe [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="23afd-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="23afd-107">Notes</span><span class="sxs-lookup"><span data-stu-id="23afd-107">Remarks</span></span>

<span data-ttu-id="23afd-108">Les éléments [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) et **Smartcard** ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="23afd-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="23afd-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="23afd-109">Requirements</span></span>



| <span data-ttu-id="23afd-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="23afd-110">Requirement</span></span> | <span data-ttu-id="23afd-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="23afd-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="23afd-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23afd-112">Minimum supported client</span></span><br/> | <span data-ttu-id="23afd-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23afd-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="23afd-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="23afd-114">Minimum supported server</span></span><br/> | <span data-ttu-id="23afd-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="23afd-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23afd-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="23afd-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="23afd-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="23afd-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="23afd-118">**CredentialsSourceParameters**</span><span class="sxs-lookup"><span data-stu-id="23afd-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="23afd-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="23afd-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="23afd-120">**CredentialsSource (EapType)**</span><span class="sxs-lookup"><span data-stu-id="23afd-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="23afd-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="23afd-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="23afd-122">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="23afd-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="23afd-123">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="23afd-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="23afd-124">Éléments de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="23afd-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





