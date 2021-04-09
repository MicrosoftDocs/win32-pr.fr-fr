---
description: Contient une stratégie de réseau local sans fil.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Élément WLANPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114318"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="50cd8-103">Élément WLANPolicy</span><span class="sxs-lookup"><span data-stu-id="50cd8-103">WLANPolicy Element</span></span>

<span data-ttu-id="50cd8-104">L’élément **WLANPolicy** contient une stratégie de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="50cd8-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="50cd8-105">Cet élément est l’élément racine unique d’un profil de stratégie sans fil.</span><span class="sxs-lookup"><span data-stu-id="50cd8-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="50cd8-106">L’espace de noms cible de l’élément **WLANPolicy** est `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="50cd8-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="50cd8-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="50cd8-107">Child elements</span></span>



| <span data-ttu-id="50cd8-108">Élément</span><span class="sxs-lookup"><span data-stu-id="50cd8-108">Element</span></span>                                                                                                                    | <span data-ttu-id="50cd8-109">Type</span><span class="sxs-lookup"><span data-stu-id="50cd8-109">Type</span></span>                                                                     | <span data-ttu-id="50cd8-110">Description</span><span class="sxs-lookup"><span data-stu-id="50cd8-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50cd8-111">**allowEveryoneToCreateAllUserProfiles**</span><span class="sxs-lookup"><span data-stu-id="50cd8-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="50cd8-112">boolean</span><span class="sxs-lookup"><span data-stu-id="50cd8-112">boolean</span></span>                                                                  | <span data-ttu-id="50cd8-113">Spécifie si un utilisateur peut créer un profil tous les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="50cd8-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="50cd8-114">**allowList**</span><span class="sxs-lookup"><span data-stu-id="50cd8-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="50cd8-115">Liste des réseaux locaux sans fil auxquels un ordinateur doit être autorisé à se connecter.</span><span class="sxs-lookup"><span data-stu-id="50cd8-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="50cd8-116">**Noires**</span><span class="sxs-lookup"><span data-stu-id="50cd8-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="50cd8-117">Liste des réseaux locaux sans fil auxquels un ordinateur ne doit pas se connecter.</span><span class="sxs-lookup"><span data-stu-id="50cd8-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="50cd8-118">**denyAllESS**</span><span class="sxs-lookup"><span data-stu-id="50cd8-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="50cd8-119">boolean</span><span class="sxs-lookup"><span data-stu-id="50cd8-119">boolean</span></span>                                                                  | <span data-ttu-id="50cd8-120">Spécifie si l’accès à tous les réseaux d’infrastructure est bloqué.</span><span class="sxs-lookup"><span data-stu-id="50cd8-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="50cd8-121">**denyAllIBSS**</span><span class="sxs-lookup"><span data-stu-id="50cd8-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="50cd8-122">boolean</span><span class="sxs-lookup"><span data-stu-id="50cd8-122">boolean</span></span>                                                                  | <span data-ttu-id="50cd8-123">Spécifie si l’accès à tous les réseaux ad hoc est bloqué.</span><span class="sxs-lookup"><span data-stu-id="50cd8-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="50cd8-124">**descriptive**</span><span class="sxs-lookup"><span data-stu-id="50cd8-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="50cd8-125">**nameType**</span><span class="sxs-lookup"><span data-stu-id="50cd8-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="50cd8-126">Description d’une stratégie de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="50cd8-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="50cd8-127">**enableAutoConfig**</span><span class="sxs-lookup"><span data-stu-id="50cd8-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="50cd8-128">boolean</span><span class="sxs-lookup"><span data-stu-id="50cd8-128">boolean</span></span>                                                                  | <span data-ttu-id="50cd8-129">Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil.</span><span class="sxs-lookup"><span data-stu-id="50cd8-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="50cd8-130">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="50cd8-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="50cd8-131">Contient les paramètres globaux du module d’auto-configuration (ACM).</span><span class="sxs-lookup"><span data-stu-id="50cd8-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="50cd8-132">**nomme**</span><span class="sxs-lookup"><span data-stu-id="50cd8-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="50cd8-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="50cd8-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="50cd8-134">Nom d’une stratégie de réseau local sans fil.</span><span class="sxs-lookup"><span data-stu-id="50cd8-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="50cd8-135">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="50cd8-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="50cd8-136">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="50cd8-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="50cd8-137">Un réseau autorisé.</span><span class="sxs-lookup"><span data-stu-id="50cd8-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="50cd8-138">**réseaux**</span><span class="sxs-lookup"><span data-stu-id="50cd8-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="50cd8-139">**networkItemType**</span><span class="sxs-lookup"><span data-stu-id="50cd8-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="50cd8-140">Un réseau bloqué.</span><span class="sxs-lookup"><span data-stu-id="50cd8-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="50cd8-141">**networkFilter**</span><span class="sxs-lookup"><span data-stu-id="50cd8-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="50cd8-142">Liste des réseaux autorisés et refusés.</span><span class="sxs-lookup"><span data-stu-id="50cd8-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="50cd8-143">**profileList**</span><span class="sxs-lookup"><span data-stu-id="50cd8-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="50cd8-144">Contient une liste de profils à appliquer au niveau du domaine ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="50cd8-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="50cd8-145">**showDeniedNetwork**</span><span class="sxs-lookup"><span data-stu-id="50cd8-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="50cd8-146">boolean</span><span class="sxs-lookup"><span data-stu-id="50cd8-146">boolean</span></span>                                                                  | <span data-ttu-id="50cd8-147">Spécifie si les réseaux refusés s’affichent dans l’Assistant **connexion à un réseau** .</span><span class="sxs-lookup"><span data-stu-id="50cd8-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="50cd8-148">Notes</span><span class="sxs-lookup"><span data-stu-id="50cd8-148">Remarks</span></span>

<span data-ttu-id="50cd8-149">Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de stratégie WLAN](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="50cd8-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="50cd8-150">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50cd8-150">Requirements</span></span>



| <span data-ttu-id="50cd8-151">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50cd8-151">Requirement</span></span> | <span data-ttu-id="50cd8-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="50cd8-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="50cd8-153">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50cd8-153">Minimum supported client</span></span><br/> | <span data-ttu-id="50cd8-154">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50cd8-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="50cd8-155">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50cd8-155">Minimum supported server</span></span><br/> | <span data-ttu-id="50cd8-156">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="50cd8-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




