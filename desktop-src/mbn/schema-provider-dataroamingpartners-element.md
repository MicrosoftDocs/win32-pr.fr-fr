---
description: Identifie le nom et l’ID de fournisseur d’un réseau cellulaire.
ms.assetid: 007ecad9-23a3-4352-b3e2-c22d0f3f449d
title: Élément Provider (DataRoamingPartners)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Provider
api_type:
- Schema
ms.openlocfilehash: b5b36c973bf44175b90e25fd2a141fed3624d8b5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112894"
---
# <a name="provider-dataroamingpartners-element"></a><span data-ttu-id="87bf2-103">Élément Provider (DataRoamingPartners)</span><span class="sxs-lookup"><span data-stu-id="87bf2-103">Provider (DataRoamingPartners) Element</span></span>

<span data-ttu-id="87bf2-104">L’élément **Provider (DataRoamingPartners)** identifie le nom et l’ID de fournisseur d’un réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="87bf2-104">The **Provider (DataRoamingPartners)** element identifies the name and provider ID for a cellular network.</span></span>

<span data-ttu-id="87bf2-105">Cet élément possède les éléments enfants suivants.</span><span class="sxs-lookup"><span data-stu-id="87bf2-105">This element has the following child elements.</span></span>

-   [<span data-ttu-id="87bf2-106">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="87bf2-106">**ProviderID**</span></span>](schema-providerid-providertype-element.md)
-   [<span data-ttu-id="87bf2-107">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="87bf2-107">**ProviderName**</span></span>](schema-providername-providertype-element.md)

<span data-ttu-id="87bf2-108">Cet élément peut être défini plusieurs fois dans l’élément [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="87bf2-108">This element can be defined multiple times within the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span> <span data-ttu-id="87bf2-109">Elle doit être définie au moins une fois.</span><span class="sxs-lookup"><span data-stu-id="87bf2-109">It must be defined at least once.</span></span>

``` syntax
<xs:element name="Provider"
    type="providerType"
 />
```

<span data-ttu-id="87bf2-110">L’élément **Provider** est défini par l’élément [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="87bf2-110">The **Provider** element is defined by the [**DataRoamingPartners**](schema-dataroamingpartners-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="87bf2-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="87bf2-111">Requirements</span></span>



| <span data-ttu-id="87bf2-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="87bf2-112">Requirement</span></span> | <span data-ttu-id="87bf2-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="87bf2-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="87bf2-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87bf2-114">Minimum supported client</span></span><br/> | <span data-ttu-id="87bf2-115">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="87bf2-115">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="87bf2-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="87bf2-116">Minimum supported server</span></span><br/> | <span data-ttu-id="87bf2-117">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="87bf2-117">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="87bf2-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="87bf2-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="87bf2-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="87bf2-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="87bf2-120">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="87bf2-120">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="87bf2-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="87bf2-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="87bf2-122">**DataRoamingPartners (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="87bf2-122">**DataRoamingPartners (MBNProfile)**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)
</dt> </dl>

 

 




