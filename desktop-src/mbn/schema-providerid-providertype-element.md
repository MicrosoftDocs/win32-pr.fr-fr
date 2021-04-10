---
description: Spécifie l’ID du fournisseur du réseau cellulaire.
ms.assetid: 5528dfec-eb1b-4af3-8d7d-03b458e5ae75
title: ProviderID (providerType), élément
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ProviderID
api_type:
- Schema
ms.openlocfilehash: 750e6c3f4397f710bb1ccbcea0286be68a89e145
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201535"
---
# <a name="providerid-providertype-element"></a><span data-ttu-id="05af7-103">ProviderID (providerType), élément</span><span class="sxs-lookup"><span data-stu-id="05af7-103">ProviderID (providerType) Element</span></span>

<span data-ttu-id="05af7-104">L’élément **ProviderID (ProviderType)** spécifie l’ID du fournisseur du réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="05af7-104">The **ProviderID (providerType)** element specifies the provider ID of the cellular network.</span></span>

<span data-ttu-id="05af7-105">L’élément est une séquence de chiffres avec un maximum de 6 chiffres.</span><span class="sxs-lookup"><span data-stu-id="05af7-105">The element is a sequence of digits with a maximum of 6 digits.</span></span>

<span data-ttu-id="05af7-106">Cet élément est obligatoire dans l’élément [**Provider**](schema-provider-dataroamingpartners-element.md) .</span><span class="sxs-lookup"><span data-stu-id="05af7-106">This element is required within the [**Provider**](schema-provider-dataroamingpartners-element.md) element.</span></span>

``` syntax
<xs:element name="ProviderID"
    type="providerType"
 />
```

<span data-ttu-id="05af7-107">L’élément **ProviderID** est défini par le type complexe [**ProviderType**](schema-providertype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="05af7-107">The **ProviderID** element is defined by the [**providerType**](schema-providertype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="05af7-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="05af7-108">Requirements</span></span>



| <span data-ttu-id="05af7-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="05af7-109">Requirement</span></span> | <span data-ttu-id="05af7-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="05af7-110">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="05af7-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-111">Minimum supported client</span></span><br/> | <span data-ttu-id="05af7-112">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="05af7-112">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="05af7-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-113">Minimum supported server</span></span><br/> | <span data-ttu-id="05af7-114">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="05af7-114">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="05af7-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="05af7-115">See also</span></span>

<dl> <dt>

<span data-ttu-id="05af7-116">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="05af7-116">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="05af7-117">**providerType**</span><span class="sxs-lookup"><span data-stu-id="05af7-117">**providerType**</span></span>](schema-providertype-complextype.md)
</dt> <dt>

<span data-ttu-id="05af7-118">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="05af7-118">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="05af7-119">**Fournisseur (DataRoamingPartners)**</span><span class="sxs-lookup"><span data-stu-id="05af7-119">**Provider (DataRoamingPartners)**</span></span>](schema-provider-dataroamingpartners-element.md)
</dt> </dl>

 

 




