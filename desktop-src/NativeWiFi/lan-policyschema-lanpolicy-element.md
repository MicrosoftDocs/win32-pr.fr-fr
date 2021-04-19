---
description: Contient une stratégie de réseau local câblé.
ms.assetid: c06bdbc4-4199-4eec-a22f-684745912970
title: Élément LANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 1b424a47405aa8f32276019a85902bd51b173cc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518784"
---
# <a name="lanpolicy-element"></a><span data-ttu-id="40e32-103">Élément LANPolicy</span><span class="sxs-lookup"><span data-stu-id="40e32-103">LANPolicy Element</span></span>

<span data-ttu-id="40e32-104">L’élément LANPolicy contient une stratégie de réseau local câblé.</span><span class="sxs-lookup"><span data-stu-id="40e32-104">The LANPolicy element contains a wired LAN policy.</span></span> <span data-ttu-id="40e32-105">Cet élément est l’élément racine unique d’un profil de stratégie de réseau câblé.</span><span class="sxs-lookup"><span data-stu-id="40e32-105">This element is the unique root element for a wired network policy profile.</span></span>

<span data-ttu-id="40e32-106">L’espace de noms cible de l’élément **LANPolicy** est `https://www.microsoft.com/networking/LAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="40e32-106">The target namespace for the **LANPolicy** element is `https://www.microsoft.com/networking/LAN/policy/v1`.</span></span>

``` syntax
<xs:element name="LANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="40e32-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="40e32-107">Child elements</span></span>



| <span data-ttu-id="40e32-108">Élément</span><span class="sxs-lookup"><span data-stu-id="40e32-108">Element</span></span>                                                                           | <span data-ttu-id="40e32-109">Type</span><span class="sxs-lookup"><span data-stu-id="40e32-109">Type</span></span>                                                     | <span data-ttu-id="40e32-110">Description</span><span class="sxs-lookup"><span data-stu-id="40e32-110">Description</span></span>                                                                                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="40e32-111">**descriptive**</span><span class="sxs-lookup"><span data-stu-id="40e32-111">**description**</span></span>](lan-policyschema-description-lanpolicy-element.md)             | [<span data-ttu-id="40e32-112">**nameType**</span><span class="sxs-lookup"><span data-stu-id="40e32-112">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="40e32-113">Contient la description d’une stratégie de réseau local câblé.</span><span class="sxs-lookup"><span data-stu-id="40e32-113">Contains the description of a wired LAN policy.</span></span> <br/>                                                                                                                          |
| [<span data-ttu-id="40e32-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="40e32-114">**enableAutoConfig**</span></span>](lan-policyschema-enableautoconfig-globalflags-element.md) | <span data-ttu-id="40e32-115">boolean</span><span class="sxs-lookup"><span data-stu-id="40e32-115">boolean</span></span>                                                  | <span data-ttu-id="40e32-116">Spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 X).</span><span class="sxs-lookup"><span data-stu-id="40e32-116">Specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span><br/> |
| [<span data-ttu-id="40e32-117">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="40e32-117">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)             |                                                          | <span data-ttu-id="40e32-118">Contient les paramètres globaux de la configuration automatique des réseaux câblés.</span><span class="sxs-lookup"><span data-stu-id="40e32-118">Contains the global settings for the automatic configuration of wired networks.</span></span> <br/>                                                                                          |
| [<span data-ttu-id="40e32-119">**nomme**</span><span class="sxs-lookup"><span data-stu-id="40e32-119">**name**</span></span>](lan-policyschema-name-lanpolicy-element.md)                           | [<span data-ttu-id="40e32-120">**nameType**</span><span class="sxs-lookup"><span data-stu-id="40e32-120">**nameType**</span></span>](lan-policyschema-nametype-simpletype.md) | <span data-ttu-id="40e32-121">Contient le nom d’une stratégie de réseau local câblé.</span><span class="sxs-lookup"><span data-stu-id="40e32-121">Contains the name of a wired LAN policy.</span></span> <br/>                                                                                                                                 |
| [<span data-ttu-id="40e32-122">**profileList**</span><span class="sxs-lookup"><span data-stu-id="40e32-122">**profileList**</span></span>](lan-policyschema-profilelist-lanpolicy-element.md)             |                                                          | <span data-ttu-id="40e32-123">Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="40e32-123">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                                                                |



## <a name="remarks"></a><span data-ttu-id="40e32-124">Notes</span><span class="sxs-lookup"><span data-stu-id="40e32-124">Remarks</span></span>

<span data-ttu-id="40e32-125">Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de stratégie LAN](lan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="40e32-125">To view the list of child elements in a tree-like structure, see [LAN\_policy Schema Elements](lan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="40e32-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="40e32-126">Requirements</span></span>



| <span data-ttu-id="40e32-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="40e32-127">Requirement</span></span> | <span data-ttu-id="40e32-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="40e32-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="40e32-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40e32-129">Minimum supported client</span></span><br/> | <span data-ttu-id="40e32-130">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40e32-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="40e32-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="40e32-131">Minimum supported server</span></span><br/> | <span data-ttu-id="40e32-132">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="40e32-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




