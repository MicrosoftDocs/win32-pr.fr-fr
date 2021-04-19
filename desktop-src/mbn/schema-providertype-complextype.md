---
description: Spécifie des informations sur un réseau cellulaire.
ms.assetid: 52d07b64-7939-4f1c-9793-be07af098053
title: Type complexe providerType (haut débit mobile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- providerType
api_type:
- Schema
ms.openlocfilehash: 1520425cf6ec1bc246f26f2db2d75f79f45a3dae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545789"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="74c17-103">Type complexe providerType</span><span class="sxs-lookup"><span data-stu-id="74c17-103">providerType Complex Type</span></span>

<span data-ttu-id="74c17-104">Le type complexe **ProviderType** spécifie des informations sur un réseau cellulaire.</span><span class="sxs-lookup"><span data-stu-id="74c17-104">The **providerType** complex type specifies information about a cellular network.</span></span>

``` syntax
<xs:complexType name="providerType">
    <xs:sequence>
        <xs:element name="ProviderID"
            type="providerIdType"
         />
        <xs:element name="ProviderName"
            type="providerNameType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="74c17-105">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="74c17-105">Child elements</span></span>



| <span data-ttu-id="74c17-106">Élément</span><span class="sxs-lookup"><span data-stu-id="74c17-106">Element</span></span>                                                          | <span data-ttu-id="74c17-107">Type</span><span class="sxs-lookup"><span data-stu-id="74c17-107">Type</span></span>                                                           | <span data-ttu-id="74c17-108">Description</span><span class="sxs-lookup"><span data-stu-id="74c17-108">Description</span></span>               |
|------------------------------------------------------------------|----------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="74c17-109">**ProviderID**</span><span class="sxs-lookup"><span data-stu-id="74c17-109">**ProviderID**</span></span>](schema-providerid-providertype-element.md)     | [<span data-ttu-id="74c17-110">**providerIdType**</span><span class="sxs-lookup"><span data-stu-id="74c17-110">**providerIdType**</span></span>](schema-provideridtype-simpletype.md)     | <span data-ttu-id="74c17-111">ID du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="74c17-111">Provider ID.</span></span><br/>   |
| [<span data-ttu-id="74c17-112">**ProviderName**</span><span class="sxs-lookup"><span data-stu-id="74c17-112">**ProviderName**</span></span>](schema-providername-providertype-element.md) | [<span data-ttu-id="74c17-113">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="74c17-113">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="74c17-114">Nom du fournisseur.</span><span class="sxs-lookup"><span data-stu-id="74c17-114">Provider name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="74c17-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74c17-115">Requirements</span></span>



| <span data-ttu-id="74c17-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74c17-116">Requirement</span></span> | <span data-ttu-id="74c17-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="74c17-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="74c17-118">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c17-118">Minimum supported client</span></span><br/> | <span data-ttu-id="74c17-119">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="74c17-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="74c17-120">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c17-120">Minimum supported server</span></span><br/> | <span data-ttu-id="74c17-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="74c17-121">None supported</span></span><br/>                         |



 

 




