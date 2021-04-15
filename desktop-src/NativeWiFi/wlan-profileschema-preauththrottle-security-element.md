---
description: Spécifie le nombre de tentatives de pré-authentification pour essayer sur les points d’accès voisins.
ms.assetid: 7e89e962-7544-4efb-9e3c-c108bee22aea
title: Élément preAuthThrottle (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- preAuthThrottle
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 499401affb264238a065c0861f1230f23936206e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525755"
---
# <a name="preauththrottle-security-element"></a><span data-ttu-id="5cdfa-103">Élément preAuthThrottle (Security)</span><span class="sxs-lookup"><span data-stu-id="5cdfa-103">preAuthThrottle (security) Element</span></span>

<span data-ttu-id="5cdfa-104">L’élément preAuthThrottle (Security) spécifie le nombre de tentatives de pré-authentification pour essayer sur les points d’accès voisins.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-104">The preAuthThrottle (security) element specifies the number pre-authentication attempts to try on neighboring APs.</span></span> <span data-ttu-id="5cdfa-105">Cet élément est valide uniquement pour les réseaux définis par WPA2 avec [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) défini sur « activé ».</span><span class="sxs-lookup"><span data-stu-id="5cdfa-105">This element is valid only for WPA2-defined networks with [**PMKCacheMode**](wlan-profileschema-pmkcachemode-security-element.md) set to "enabled".</span></span> <span data-ttu-id="5cdfa-106">Si **PMKCacheMode** est activé et que cet élément est absent, le nombre de tentatives est défini par défaut sur 3.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-106">If **PMKCacheMode** is enabled, and this element is absent, the number of tries defaults to 3.</span></span>

<span data-ttu-id="5cdfa-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="5cdfa-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="preAuthThrottle"
    minOccurs="0"
>
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:minInclusive
                value="1"
             />
            <xs:maxInclusive
                value="16"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="5cdfa-108">L’élément est défini par l’élément de [**sécurité**](wlan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="5cdfa-108">The element is defined by the [**security**](wlan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="5cdfa-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5cdfa-109">Requirements</span></span>



| <span data-ttu-id="5cdfa-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5cdfa-110">Requirement</span></span> | <span data-ttu-id="5cdfa-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="5cdfa-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5cdfa-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cdfa-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5cdfa-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cdfa-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5cdfa-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5cdfa-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5cdfa-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5cdfa-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5cdfa-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5cdfa-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="5cdfa-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="5cdfa-118">**caution**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-118">**security**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="5cdfa-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="5cdfa-120">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="5cdfa-120">**security (MSM)**</span></span>](wlan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




