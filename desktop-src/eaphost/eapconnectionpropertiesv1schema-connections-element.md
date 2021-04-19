---
title: Élément connections
description: En savoir plus sur l’élément Connections. Cet élément collecte et contient zéro ou plusieurs éléments de connexion.
ms.assetid: 2c199338-892f-4d8c-bf33-4a19f362de3e
keywords:
- Connections, élément EAPHost
topic_type:
- apiref
api_name:
- Connections
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6cdb23c9f1a6130e2fe77061286e8a0657c3e2f5
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "106518037"
---
# <a name="connections-element"></a><span data-ttu-id="94ddc-105">Élément connections</span><span class="sxs-lookup"><span data-stu-id="94ddc-105">Connections Element</span></span>

<span data-ttu-id="94ddc-106">L’élément **connections** collecte et contient zéro ou plusieurs éléments de [**connexion**](eapconnectionpropertiesv1schema-connection-connections-element.md) .</span><span class="sxs-lookup"><span data-stu-id="94ddc-106">The **Connections** element collects and contains zero or more [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) elements.</span></span>

``` syntax
<xs:element name="Connections">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Connection"
                minOccurs="0"
                maxOccurs="unbounded"
            >
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
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="94ddc-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="94ddc-107">Child elements</span></span>



| <span data-ttu-id="94ddc-108">Élément</span><span class="sxs-lookup"><span data-stu-id="94ddc-108">Element</span></span>                                                                              | <span data-ttu-id="94ddc-109">Type</span><span class="sxs-lookup"><span data-stu-id="94ddc-109">Type</span></span>   | <span data-ttu-id="94ddc-110">Description</span><span class="sxs-lookup"><span data-stu-id="94ddc-110">Description</span></span>                                                                                                                                                                                |
|--------------------------------------------------------------------------------------|--------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94ddc-111">**EAP**</span><span class="sxs-lookup"><span data-stu-id="94ddc-111">**Eap**</span></span>](baseeapconnectionpropertiesv1schema-eap-element.md)                       |        | <span data-ttu-id="94ddc-112">Identifie l’élément de configuration EAP.</span><span class="sxs-lookup"><span data-stu-id="94ddc-112">Identifies the EAP configuration element.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="94ddc-113">**Égard**</span><span class="sxs-lookup"><span data-stu-id="94ddc-113">**Connection**</span></span>](eapconnectionpropertiesv1schema-connection-connections-element.md) |        | <span data-ttu-id="94ddc-114">Définit chaque paramètre de configuration et l’associe à un nom.</span><span class="sxs-lookup"><span data-stu-id="94ddc-114">Defines each configuration setting and associates it with a name.</span></span> <span data-ttu-id="94ddc-115">L’élément [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) est facultatif.</span><span class="sxs-lookup"><span data-stu-id="94ddc-115">The [**Connection**](eapconnectionpropertiesv1schema-connection-connections-element.md) element is optional.</span></span><br/> |
| [<span data-ttu-id="94ddc-116">**Nom**</span><span class="sxs-lookup"><span data-stu-id="94ddc-116">**Name**</span></span>](eapconnectionpropertiesv1schema-name-connection-element.md)              | <span data-ttu-id="94ddc-117">string</span><span class="sxs-lookup"><span data-stu-id="94ddc-117">string</span></span> | <span data-ttu-id="94ddc-118">Capture le nom de la connexion définie, en aidant à identifier plusieurs connexions.</span><span class="sxs-lookup"><span data-stu-id="94ddc-118">Captures the name of the connection being defined, assisting in the identification of multiple connections.</span></span><br/>                                                                     |



## <a name="remarks"></a><span data-ttu-id="94ddc-119">Notes</span><span class="sxs-lookup"><span data-stu-id="94ddc-119">Remarks</span></span>

<span data-ttu-id="94ddc-120">L’élément **connections** n’est pas utilisé avec les méthodes héritées via les API EAPHost.</span><span class="sxs-lookup"><span data-stu-id="94ddc-120">The **Connections** element is not used with legacy methods via the EAPHost APIs.</span></span>

## <a name="requirements"></a><span data-ttu-id="94ddc-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="94ddc-121">Requirements</span></span>



| <span data-ttu-id="94ddc-122">Role</span><span class="sxs-lookup"><span data-stu-id="94ddc-122">Role</span></span> | <span data-ttu-id="94ddc-123">Version minimale du système d’exploitation prise en charge</span><span class="sxs-lookup"><span data-stu-id="94ddc-123">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="94ddc-124">Client</span><span class="sxs-lookup"><span data-stu-id="94ddc-124">Client</span></span><br/> | <span data-ttu-id="94ddc-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ddc-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="94ddc-126">Serveur</span><span class="sxs-lookup"><span data-stu-id="94ddc-126">Server</span></span><br/> | <span data-ttu-id="94ddc-127">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="94ddc-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94ddc-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="94ddc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ddc-129">EAPHost et schéma hérité</span><span class="sxs-lookup"><span data-stu-id="94ddc-129">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="94ddc-130">Schéma eapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="94ddc-130">eapconnectionpropertiesv1 Schema</span></span>](eapconnectionpropertiesv1schema-schema.md)
</dt> </dl>

 

 





