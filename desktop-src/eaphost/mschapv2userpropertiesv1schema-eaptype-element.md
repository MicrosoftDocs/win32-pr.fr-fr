---
title: Élément EapType (mschapv2userpropertiesv1schema)
description: Cet élément est un type dérivé de l’élément EapType du schéma baseeapuserpropertiesv1. Pour mschapv2userpropertiesv1schema.
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
keywords:
- Élément EapType EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106530066"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="1a478-105">Élément EapType (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="1a478-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="1a478-106">L’élément **EapType** est un type dérivé de l’élément [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) du schéma [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1a478-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="1a478-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="1a478-107">Child elements</span></span>



| <span data-ttu-id="1a478-108">Élément</span><span class="sxs-lookup"><span data-stu-id="1a478-108">Element</span></span>                                                                           | <span data-ttu-id="1a478-109">Type</span><span class="sxs-lookup"><span data-stu-id="1a478-109">Type</span></span>   | <span data-ttu-id="1a478-110">Description</span><span class="sxs-lookup"><span data-stu-id="1a478-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1a478-111">**Nom d’utilisateur**</span><span class="sxs-lookup"><span data-stu-id="1a478-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="1a478-112">Identifie l’utilisateur authentifié.</span><span class="sxs-lookup"><span data-stu-id="1a478-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="1a478-113">Si cet élément n’est pas présent, le nom d’utilisateur est obtenu à partir de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="1a478-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="1a478-114">L’élément [**username**](mschapv2userpropertiesv1schema-username-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a478-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="1a478-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="1a478-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="1a478-116">string</span><span class="sxs-lookup"><span data-stu-id="1a478-116">string</span></span> | <span data-ttu-id="1a478-117">Identifie le domaine de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="1a478-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="1a478-118">Si cet élément n’est pas présent, c’est le domaine de Winlogon qui est utilisé.</span><span class="sxs-lookup"><span data-stu-id="1a478-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="1a478-119">L’élément [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a478-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="1a478-120">**De**</span><span class="sxs-lookup"><span data-stu-id="1a478-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="1a478-121">string</span><span class="sxs-lookup"><span data-stu-id="1a478-121">string</span></span> | <span data-ttu-id="1a478-122">Identifie le mot de passe de l’utilisateur ou de l’ordinateur en cours d’authentification.</span><span class="sxs-lookup"><span data-stu-id="1a478-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="1a478-123">Si cet élément n’est pas présent, le hachage de mot de passe est obtenu à partir de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="1a478-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="1a478-124">L’élément [**de mot de passe**](mschapv2userpropertiesv1schema-password-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a478-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1a478-125">Notes</span><span class="sxs-lookup"><span data-stu-id="1a478-125">Remarks</span></span>

<span data-ttu-id="1a478-126">L’élément **processContents** active les futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="1a478-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="1a478-127">L’élément **processContents** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="1a478-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a478-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1a478-128">Requirements</span></span>



| <span data-ttu-id="1a478-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1a478-129">Requirement</span></span> | <span data-ttu-id="1a478-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="1a478-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a478-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a478-131">Minimum supported client</span></span><br/> | <span data-ttu-id="1a478-132">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a478-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1a478-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1a478-133">Minimum supported server</span></span><br/> | <span data-ttu-id="1a478-134">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1a478-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a478-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1a478-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a478-136">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="1a478-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1a478-137">Schéma mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1a478-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





