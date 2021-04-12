---
description: Contient les paramètres globaux de la configuration automatique des réseaux câblés.
ms.assetid: 172cf15c-cd51-43d4-ae5d-f9460c2a40e2
title: Élément globalFlags (LANPolicy)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c9a244fbbc616e3092e2293fe187da1d7be0fa53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203765"
---
# <a name="globalflags-lanpolicy-element"></a><span data-ttu-id="6fda9-103">Élément globalFlags (LANPolicy)</span><span class="sxs-lookup"><span data-stu-id="6fda9-103">globalFlags (LANPolicy) Element</span></span>

<span data-ttu-id="6fda9-104">L’élément globalFlags (LANPolicy) contient les paramètres globaux de la configuration automatique des réseaux câblés.</span><span class="sxs-lookup"><span data-stu-id="6fda9-104">The globalFlags (LANPolicy) element contains the global settings for the automatic configuration of wired networks.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
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

<span data-ttu-id="6fda9-105">L’élément **globalFlags** est défini par l’élément [**LANPolicy**](lan-policyschema-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="6fda9-105">The **globalFlags** element is defined by the [**LANPolicy**](lan-policyschema-lanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6fda9-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="6fda9-106">Child elements</span></span>



| <span data-ttu-id="6fda9-107">Élément</span><span class="sxs-lookup"><span data-stu-id="6fda9-107">Element</span></span>                                                                           | <span data-ttu-id="6fda9-108">Type</span><span class="sxs-lookup"><span data-stu-id="6fda9-108">Type</span></span>    | <span data-ttu-id="6fda9-109">Description</span><span class="sxs-lookup"><span data-stu-id="6fda9-109">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6fda9-110">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="6fda9-110">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="6fda9-111">boolean</span><span class="sxs-lookup"><span data-stu-id="6fda9-111">boolean</span></span> | <span data-ttu-id="6fda9-112">Spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="6fda9-112">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6fda9-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6fda9-113">Requirements</span></span>



| <span data-ttu-id="6fda9-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6fda9-114">Requirement</span></span> | <span data-ttu-id="6fda9-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="6fda9-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6fda9-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fda9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6fda9-117">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fda9-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6fda9-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6fda9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6fda9-119">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6fda9-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6fda9-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6fda9-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="6fda9-121">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="6fda9-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6fda9-122">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="6fda9-122">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="6fda9-123">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="6fda9-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6fda9-124">**LANPolicy**</span><span class="sxs-lookup"><span data-stu-id="6fda9-124">**LANPolicy**</span></span>](lan-policyschema-lanpolicy-element.md)
</dt> </dl>

 

 




