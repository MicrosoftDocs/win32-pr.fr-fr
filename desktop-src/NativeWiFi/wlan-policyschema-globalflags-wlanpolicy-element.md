---
description: Contient les paramètres globaux du module d’auto-configuration (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Élément globalFlags (WLANPolicy)
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
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530093"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="70ddc-103">Élément globalFlags (WLANPolicy)</span><span class="sxs-lookup"><span data-stu-id="70ddc-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="70ddc-104">L’élément globalFlags (WLANPolicy) contient les paramètres globaux du module d’auto-configuration (ACM).</span><span class="sxs-lookup"><span data-stu-id="70ddc-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="70ddc-105">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="70ddc-105">This element is mandatory.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
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

<span data-ttu-id="70ddc-106">L’élément **globalFlags** est défini par l’élément [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="70ddc-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="70ddc-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="70ddc-107">Child elements</span></span>



| <span data-ttu-id="70ddc-108">Élément</span><span class="sxs-lookup"><span data-stu-id="70ddc-108">Element</span></span>                                                                                                                    | <span data-ttu-id="70ddc-109">Type</span><span class="sxs-lookup"><span data-stu-id="70ddc-109">Type</span></span>    | <span data-ttu-id="70ddc-110">Description</span><span class="sxs-lookup"><span data-stu-id="70ddc-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70ddc-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="70ddc-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="70ddc-112">boolean</span><span class="sxs-lookup"><span data-stu-id="70ddc-112">boolean</span></span> | <span data-ttu-id="70ddc-113">Spécifie si un utilisateur peut créer un profil tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="70ddc-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="70ddc-114">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="70ddc-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="70ddc-115">boolean</span><span class="sxs-lookup"><span data-stu-id="70ddc-115">boolean</span></span> | <span data-ttu-id="70ddc-116">Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil.</span><span class="sxs-lookup"><span data-stu-id="70ddc-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="70ddc-117">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="70ddc-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="70ddc-118">boolean</span><span class="sxs-lookup"><span data-stu-id="70ddc-118">boolean</span></span> | <span data-ttu-id="70ddc-119">Spécifie si les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** .</span><span class="sxs-lookup"><span data-stu-id="70ddc-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="70ddc-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="70ddc-120">Requirements</span></span>



| <span data-ttu-id="70ddc-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="70ddc-121">Requirement</span></span> | <span data-ttu-id="70ddc-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="70ddc-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="70ddc-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70ddc-123">Minimum supported client</span></span><br/> | <span data-ttu-id="70ddc-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70ddc-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="70ddc-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="70ddc-125">Minimum supported server</span></span><br/> | <span data-ttu-id="70ddc-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="70ddc-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="70ddc-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70ddc-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="70ddc-128">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="70ddc-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="70ddc-129">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="70ddc-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="70ddc-130">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="70ddc-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="70ddc-131">**WLANPolicy**</span><span class="sxs-lookup"><span data-stu-id="70ddc-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




