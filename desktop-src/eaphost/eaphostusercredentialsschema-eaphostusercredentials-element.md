---
title: Élément EapHostUserCredentials
description: Contient l’élément EapMethod, ainsi que les informations d’identification ou l’élément CredentialsBlob.
ms.assetid: 6d0d41c8-560c-4d42-83c9-865053aef47a
keywords:
- Élément EapHostUserCredentials EAPHost
topic_type:
- apiref
api_name:
- EapHostUserCredentials
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 690770091219e51b3ebb550a1a72e50f76b20542
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104872"
---
# <a name="eaphostusercredentials-element"></a><span data-ttu-id="a78c7-104">Élément EapHostUserCredentials</span><span class="sxs-lookup"><span data-stu-id="a78c7-104">EapHostUserCredentials Element</span></span>

<span data-ttu-id="a78c7-105">L’élément **EapHostUserCredentials** contient l’élément [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) , ainsi que les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) ou l’élément [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a78c7-105">The **EapHostUserCredentials** element contains the [**EapMethod**](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md) element, and [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) or [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) element.</span></span>

``` syntax
<xs:element name="EapHostUserCredentials">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="EapMethod"
                type="EapMethodType"
             />
            <xs:choice>
                <xs:element name="Credentials"
                    type="BaseEapMethodUserCredentials"
                 />
                <xs:element name="CredentialsBlob"
                    type="hexBinary"
                 />
            </xs:choice>
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="a78c7-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="a78c7-106">Child elements</span></span>



| <span data-ttu-id="a78c7-107">Élément</span><span class="sxs-lookup"><span data-stu-id="a78c7-107">Element</span></span>                                                                                                | <span data-ttu-id="a78c7-108">Type</span><span class="sxs-lookup"><span data-stu-id="a78c7-108">Type</span></span>                                                                                                                | <span data-ttu-id="a78c7-109">Description</span><span class="sxs-lookup"><span data-stu-id="a78c7-109">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a78c7-110">**Informations d’identification**</span><span class="sxs-lookup"><span data-stu-id="a78c7-110">**Credentials**</span></span>](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md)         | [<span data-ttu-id="a78c7-111">**BaseEapMethodUserCredentials**</span><span class="sxs-lookup"><span data-stu-id="a78c7-111">**BaseEapMethodUserCredentials**</span></span>](baseeapmethodusercredentialsschema-baseeapmethodusercredentials-complextype.md) | <span data-ttu-id="a78c7-112">Est utilisé lorsque la configuration de la méthode est au format texte XML au lieu d’un objet BLOB binaire.</span><span class="sxs-lookup"><span data-stu-id="a78c7-112">Is used when the method configuration is in XML text form instead of a binary BLOB.</span></span><br/>   |
| [<span data-ttu-id="a78c7-113">**CredentialsBlob**</span><span class="sxs-lookup"><span data-stu-id="a78c7-113">**CredentialsBlob**</span></span>](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) | <span data-ttu-id="a78c7-114">hexBinary</span><span class="sxs-lookup"><span data-stu-id="a78c7-114">hexBinary</span></span>                                                                                                           | <span data-ttu-id="a78c7-115">Est utilisé lorsque la configuration de la méthode est un objet BLOB binaire au lieu du format texte XML.</span><span class="sxs-lookup"><span data-stu-id="a78c7-115">Is used when the method configuration is a binary BLOB instead of in XML text format.</span></span><br/> |
| [<span data-ttu-id="a78c7-116">**EapMethod**</span><span class="sxs-lookup"><span data-stu-id="a78c7-116">**EapMethod**</span></span>](eaphostusercredentialsschema-eapmethod-eaphostusercredentials-element.md)             | [<span data-ttu-id="a78c7-117">**EapMethodType**</span><span class="sxs-lookup"><span data-stu-id="a78c7-117">**EapMethodType**</span></span>](eapcommonschema-eapmethodtype-complextype.md)                                                  | <span data-ttu-id="a78c7-118">Identifie la méthode référencée.</span><span class="sxs-lookup"><span data-stu-id="a78c7-118">Identifies the method being referred to.</span></span> <br/>                                             |



## <a name="remarks"></a><span data-ttu-id="a78c7-119">Notes</span><span class="sxs-lookup"><span data-stu-id="a78c7-119">Remarks</span></span>

<span data-ttu-id="a78c7-120">Les [**informations d’identification**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) et les éléments [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) ne peuvent pas être utilisés simultanément.</span><span class="sxs-lookup"><span data-stu-id="a78c7-120">The [**Credentials**](eaphostusercredentialsschema-credentials-eaphostusercredentials-element.md) and [**CredentialsBlob**](eaphostusercredentialsschema-credentialsblob-eaphostusercredentials-element.md) elements cannot be both be used simultaneously.</span></span>

<span data-ttu-id="a78c7-121">Il existe un point d’extension pour d’autres espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="a78c7-121">There is an extension point for other namespaces.</span></span>

<span data-ttu-id="a78c7-122">L’élément **processContents** active les futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="a78c7-122">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="a78c7-123">L’élément **processContents** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a78c7-123">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="a78c7-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a78c7-124">Requirements</span></span>



| <span data-ttu-id="a78c7-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a78c7-125">Requirement</span></span> | <span data-ttu-id="a78c7-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="a78c7-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a78c7-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78c7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a78c7-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a78c7-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a78c7-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a78c7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a78c7-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a78c7-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a78c7-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a78c7-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a78c7-132">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="a78c7-132">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="a78c7-133">Schéma eaphostusercredentials</span><span class="sxs-lookup"><span data-stu-id="a78c7-133">eaphostusercredentials Schema</span></span>](eaphostusercredentialsschema-schema.md)
</dt> </dl>

 

 





