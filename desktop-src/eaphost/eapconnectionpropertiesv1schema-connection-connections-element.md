---
title: Élément Connection (Connections)
description: Définit chaque paramètre de configuration et l’associe à un nom. L’élément Connection est facultatif.
ms.assetid: 913263ab-0e0e-4213-947b-7bca9ba0697e
keywords:
- Élément de connexion EAPHost
topic_type:
- apiref
api_name:
- Connection
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5aabc29a7fe5122a7f7571750b97ebccb38158d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106536291"
---
# <a name="connection-connections-element"></a><span data-ttu-id="f1df8-105">Élément Connection (Connections)</span><span class="sxs-lookup"><span data-stu-id="f1df8-105">Connection (Connections) Element</span></span>

<span data-ttu-id="f1df8-106">L’élément **Connection (Connections)** définit chaque paramètre de configuration et l’associe à un nom.</span><span class="sxs-lookup"><span data-stu-id="f1df8-106">The **Connection (Connections)** element defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="f1df8-107">L’élément **Connection** est facultatif.</span><span class="sxs-lookup"><span data-stu-id="f1df8-107">The **Connection** element is optional.</span></span>

``` syntax
<xs:element name="Connection">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="string"
             />
            <xs:element
                maxOccurs="unbounded"
                ref="Eap"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="f1df8-108">L’élément **Connection** est défini par l’élément [**connections**](eapconnectionpropertiesv1schema-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f1df8-108">The **Connection** element is defined by the [**Connections**](eapconnectionpropertiesv1schema-connections-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="f1df8-109">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="f1df8-109">Child elements</span></span>



| <span data-ttu-id="f1df8-110">Élément</span><span class="sxs-lookup"><span data-stu-id="f1df8-110">Element</span></span>                                                                 | <span data-ttu-id="f1df8-111">Type</span><span class="sxs-lookup"><span data-stu-id="f1df8-111">Type</span></span>   | <span data-ttu-id="f1df8-112">Description</span><span class="sxs-lookup"><span data-stu-id="f1df8-112">Description</span></span>                                                                                                             |
|-------------------------------------------------------------------------|--------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f1df8-113">**EAP**</span><span class="sxs-lookup"><span data-stu-id="f1df8-113">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)          |        | <span data-ttu-id="f1df8-114">Identifie l’élément de configuration EAP.</span><span class="sxs-lookup"><span data-stu-id="f1df8-114">Identifies the EAP configuration element.</span></span><br/>                                                                    |
| [<span data-ttu-id="f1df8-115">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f1df8-115">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md) | <span data-ttu-id="f1df8-116">string</span><span class="sxs-lookup"><span data-stu-id="f1df8-116">string</span></span> | <span data-ttu-id="f1df8-117">Capture le nom de la connexion définie, en aidant à identifier plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="f1df8-117">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="f1df8-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1df8-118">Requirements</span></span>



| <span data-ttu-id="f1df8-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1df8-119">Requirement</span></span> | <span data-ttu-id="f1df8-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1df8-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f1df8-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1df8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f1df8-122">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1df8-122">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f1df8-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f1df8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f1df8-124">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f1df8-124">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f1df8-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1df8-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="f1df8-126">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f1df8-126">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f1df8-127">**Connexions**</span><span class="sxs-lookup"><span data-stu-id="f1df8-127">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

<span data-ttu-id="f1df8-128">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="f1df8-128">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f1df8-129">**Connexions**</span><span class="sxs-lookup"><span data-stu-id="f1df8-129">**Connections**</span></span>](eapconnectionpropertiesv1schema-connections-element.md)
</dt> <dt>

[<span data-ttu-id="f1df8-130">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="f1df8-130">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f1df8-131">Schéma eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f1df8-131">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





