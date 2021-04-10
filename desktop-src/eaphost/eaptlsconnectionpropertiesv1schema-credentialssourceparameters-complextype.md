---
title: Type complexe CredentialsSourceParameters
description: Définit l’élément requis pour spécifier la source du certificat à utiliser avec une authentification EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- CredentialsSourceParameters type complexe EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104869"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="2002a-104">Type complexe CredentialsSourceParameters</span><span class="sxs-lookup"><span data-stu-id="2002a-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="2002a-105">Le type complexe **CredentialsSourceParameters** définit l’élément requis pour spécifier la source du certificat à utiliser avec une authentification EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="2002a-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="2002a-106">Vous avez le choix entre l’élément de [**carte à puce**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ou l’élément [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2002a-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="2002a-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="2002a-107">Child elements</span></span>



| <span data-ttu-id="2002a-108">Élément</span><span class="sxs-lookup"><span data-stu-id="2002a-108">Element</span></span>                                                                                                             | <span data-ttu-id="2002a-109">Type</span><span class="sxs-lookup"><span data-stu-id="2002a-109">Type</span></span>                                                                                  | <span data-ttu-id="2002a-110">Description</span><span class="sxs-lookup"><span data-stu-id="2002a-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2002a-111">**nom_magasin_certificats**</span><span class="sxs-lookup"><span data-stu-id="2002a-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="2002a-112">**CertSelection**</span><span class="sxs-lookup"><span data-stu-id="2002a-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="2002a-113">Indique que le protocole EAP-TLS doit lire le certificat du magasin My de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="2002a-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="2002a-114">**Carte à puce**</span><span class="sxs-lookup"><span data-stu-id="2002a-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="2002a-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="2002a-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="2002a-116">Indique que le protocole EAP-TLS doit lire le certificat à partir de la carte à puce.</span><span class="sxs-lookup"><span data-stu-id="2002a-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="2002a-117">Notes</span><span class="sxs-lookup"><span data-stu-id="2002a-117">Remarks</span></span>

<span data-ttu-id="2002a-118">Les éléments [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) et [**Smartcard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="2002a-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="2002a-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2002a-119">Requirements</span></span>



| <span data-ttu-id="2002a-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2002a-120">Requirement</span></span> | <span data-ttu-id="2002a-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="2002a-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2002a-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2002a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2002a-123">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2002a-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2002a-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2002a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2002a-125">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2002a-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2002a-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2002a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2002a-127">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="2002a-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2002a-128">Schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2002a-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2002a-129">Types complexes de schéma eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2002a-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





