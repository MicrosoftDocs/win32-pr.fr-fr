---
description: Spécifie l’index de clé à utiliser pour chiffrer le trafic sans fil. Cette valeur est utilisée uniquement lorsque KeyType est défini sur &\# 0034 ; networkKey&\# 0034 ;.
ms.assetid: 5629605d-4c23-4318-8f09-939e13302552
title: KeyIndex (Security), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- keyIndex
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 43bb802d46abb3c4684b63206377d3464078e2c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104115822"
---
# <a name="keyindex-security-element"></a><span data-ttu-id="da70d-104">KeyIndex (Security), élément</span><span class="sxs-lookup"><span data-stu-id="da70d-104">keyIndex (security) Element</span></span>

<span data-ttu-id="da70d-105">L’élément KeyIndex (Security) spécifie l’index de clé à utiliser pour chiffrer le trafic sans fil.</span><span class="sxs-lookup"><span data-stu-id="da70d-105">The keyIndex (security) element specifies which key index should be used to encrypt wireless traffic.</span></span> <span data-ttu-id="da70d-106">Cette valeur est utilisée uniquement lorsque [**KeyType**](wlan-profileschema-keytype-sharedkey-element.md) est défini sur « networkKey ».</span><span class="sxs-lookup"><span data-stu-id="da70d-106">This is only used when [**keyType**](wlan-profileschema-keytype-sharedkey-element.md) is set to "networkKey".</span></span>

``` syntax
<xs:element name="keyIndex"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="0"
             />
            <xs:maxInclusive
                value="3"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="da70d-107">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="da70d-107">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="da70d-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="da70d-108">Requirements</span></span>



| <span data-ttu-id="da70d-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="da70d-109">Requirement</span></span> | <span data-ttu-id="da70d-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="da70d-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="da70d-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da70d-111">Minimum supported client</span></span><br/> | <span data-ttu-id="da70d-112">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da70d-112">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="da70d-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="da70d-113">Minimum supported server</span></span><br/> | <span data-ttu-id="da70d-114">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="da70d-114">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="da70d-115">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="da70d-115">Redistributable</span></span><br/>          | <span data-ttu-id="da70d-116">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="da70d-116">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="da70d-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da70d-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="da70d-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="da70d-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="da70d-119">**caution**</span><span class="sxs-lookup"><span data-stu-id="da70d-119">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="da70d-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="da70d-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="da70d-121">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="da70d-121">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




