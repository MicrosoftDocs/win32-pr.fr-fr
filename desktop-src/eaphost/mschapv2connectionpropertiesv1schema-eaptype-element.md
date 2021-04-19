---
title: Élément EapType (mschapv2connectionpropertiesv1schema)
description: Est un type dérivé de l’élément EapType du schéma baseeapconnectionpropertiesv1. Il s’agit du premier élément qui apparaît dans l’élément config du schéma EapHostConfig.
ms.assetid: dbd63387-f8ed-4308-903f-7a555f3410f7
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
ms.openlocfilehash: 3e9b7db3d3e3ab1ba90427a65a5544b87939ca88
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106537937"
---
# <a name="eaptype-element-mschapv2connectionpropertiesv1schema"></a><span data-ttu-id="cb556-105">Élément EapType (mschapv2connectionpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="cb556-105">EapType Element (mschapv2connectionpropertiesv1schema)</span></span>

<span data-ttu-id="cb556-106">L’élément **EapType** est un type dérivé de l’élément [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) du schéma [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="cb556-106">The **EapType** element is a derived type of the [EapType](baseeapconnectionpropertiesv1schema-eaptype-element.md) element from the [baseeapconnectionpropertiesv1](baseeapconnectionpropertiesv1schema-schema.md) schema.</span></span> <span data-ttu-id="cb556-107">Il s’agit du premier élément qui apparaît à l’intérieur de l’élément config du schéma [EapHostConfig](eaphostconfigschema-elements.md)</span><span class="sxs-lookup"><span data-stu-id="cb556-107">This is the top element that appears inside the Config element of the [EapHostConfig](eaphostconfigschema-elements.md) schema</span></span>

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
                    <xs:element name="UseWinLogonCredentials"
                        type="boolean"
                        default="true"
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

## <a name="child-elements"></a><span data-ttu-id="cb556-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="cb556-108">Child elements</span></span>



| <span data-ttu-id="cb556-109">Élément</span><span class="sxs-lookup"><span data-stu-id="cb556-109">Element</span></span>                                                                                                       | <span data-ttu-id="cb556-110">Type</span><span class="sxs-lookup"><span data-stu-id="cb556-110">Type</span></span>    | <span data-ttu-id="cb556-111">Description</span><span class="sxs-lookup"><span data-stu-id="cb556-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb556-112">**UseWinLogonCredentials**</span><span class="sxs-lookup"><span data-stu-id="cb556-112">**UseWinLogonCredentials**</span></span>](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) | <span data-ttu-id="cb556-113">boolean</span><span class="sxs-lookup"><span data-stu-id="cb556-113">boolean</span></span> | <span data-ttu-id="cb556-114">Contrôle l’utilisation des informations d’identification winlogin.</span><span class="sxs-lookup"><span data-stu-id="cb556-114">Controls use of the winlogin credentials.</span></span> <span data-ttu-id="cb556-115">Si la valeur est TRUE, EAP MS-CHAPv2 obtient les informations d’identification de Winlogon.</span><span class="sxs-lookup"><span data-stu-id="cb556-115">If TRUE, then EAP MS-CHAPv2 obtains credentials from winlogon.</span></span> <span data-ttu-id="cb556-116">Si la valeur est FALSe, EAP MS-CHAPv2 obtient les informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb556-116">If FALSE, then EAP MS-CHAPv2 obtains credentials from the user.</span></span> <br/> <span data-ttu-id="cb556-117">L’élément [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="cb556-117">The [**UseWinLogonCredentials (EapType)**](mschapv2connectionpropertiesv1schema-usewinlogoncredentials-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="cb556-118">Notes</span><span class="sxs-lookup"><span data-stu-id="cb556-118">Remarks</span></span>

<span data-ttu-id="cb556-119">L’élément **processContents** active les futures améliorations du schéma.</span><span class="sxs-lookup"><span data-stu-id="cb556-119">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="cb556-120">L’élément **processContents** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="cb556-120">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb556-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cb556-121">Requirements</span></span>



| <span data-ttu-id="cb556-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cb556-122">Requirement</span></span> | <span data-ttu-id="cb556-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cb556-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cb556-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb556-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb556-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb556-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cb556-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cb556-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb556-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cb556-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cb556-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cb556-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb556-129">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="cb556-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cb556-130">Schéma mschapv2connectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cb556-130">mschapv2connectionpropertiesv1 Schema</span></span>](mschapv2connectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





