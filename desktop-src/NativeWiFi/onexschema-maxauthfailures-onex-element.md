---
description: Spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.
ms.assetid: 191b6b03-8b27-4b35-8623-1ccec632f208
title: Élément maxAuthFailures (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxAuthFailures
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 31dae7a8805275254a1d398108128380b1aa2e54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104529031"
---
# <a name="maxauthfailures-onex-element"></a><span data-ttu-id="42fbb-103">Élément maxAuthFailures (OneX)</span><span class="sxs-lookup"><span data-stu-id="42fbb-103">maxAuthFailures (OneX) Element</span></span>

<span data-ttu-id="42fbb-104">L’élément maxAuthFailures (OneX) spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="42fbb-104">The maxAuthFailures (OneX) element specifies the maximum number of authentication failures allowed for a set of credentials.</span></span>

<span data-ttu-id="42fbb-105">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="42fbb-105">This element is optional.</span></span> <span data-ttu-id="42fbb-106">Quand maxAuthFailures n’est pas spécifié dans un profil, la valeur 1 est utilisée.</span><span class="sxs-lookup"><span data-stu-id="42fbb-106">When maxAuthFailures is not specified in a profile, a value of one is used.</span></span>

<span data-ttu-id="42fbb-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="42fbb-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxAuthFailures">
    <xs:simpleType>
        <xs:restriction
            base="integer"
        >
            <xs:enumeration
                value="1"
             />
            <xs:enumeration
                value="100"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="42fbb-108">L’élément **maxAuthFailures** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="42fbb-108">The **maxAuthFailures** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="42fbb-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42fbb-109">Requirements</span></span>



| <span data-ttu-id="42fbb-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42fbb-110">Requirement</span></span> | <span data-ttu-id="42fbb-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="42fbb-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="42fbb-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42fbb-112">Minimum supported client</span></span><br/> | <span data-ttu-id="42fbb-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42fbb-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="42fbb-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42fbb-114">Minimum supported server</span></span><br/> | <span data-ttu-id="42fbb-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42fbb-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="42fbb-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42fbb-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="42fbb-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="42fbb-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="42fbb-118">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="42fbb-118">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="42fbb-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="42fbb-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="42fbb-120">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="42fbb-120">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




