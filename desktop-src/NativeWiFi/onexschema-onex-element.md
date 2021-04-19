---
description: Spécifie les informations de configuration 802.1 X pour un profil de réseau local câblé ou sans fil.
ms.assetid: 4528fcb5-ee8e-4824-a69e-8d67622c4b4d
title: Élément OneX
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneX
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 4b3e3d91087a394efb7909d36d6244bfbf6115e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524633"
---
# <a name="onex-element"></a><span data-ttu-id="d4090-103">Élément OneX</span><span class="sxs-lookup"><span data-stu-id="d4090-103">OneX Element</span></span>

<span data-ttu-id="d4090-104">L’élément OneX spécifie les informations de configuration 802.1 X pour un profil de réseau local câblé ou sans fil.</span><span class="sxs-lookup"><span data-stu-id="d4090-104">The OneX element specifies 802.1X configuration information for a wired or wireless LAN profile.</span></span> <span data-ttu-id="d4090-105">Cet élément est l’élément racine unique pour un profil 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="d4090-105">This element is the unique root element for an 802.1X profile.</span></span>

<span data-ttu-id="d4090-106">L’espace de noms cible de l’élément OneX est `https://www.microsoft.com/networking/OneX/v1` .</span><span class="sxs-lookup"><span data-stu-id="d4090-106">The target namespace for the OneX element is `https://www.microsoft.com/networking/OneX/v1`.</span></span> <span data-ttu-id="d4090-107">La plupart des éléments enfants de l’élément OneX se trouvent dans l' `OneX` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d4090-107">Most child elements of the OneX element are in the `OneX` namespace.</span></span> <span data-ttu-id="d4090-108">Il existe une exception : l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est dans l' `https://www.microsoft.com/provisioning/EapHostConfig` espace de noms.</span><span class="sxs-lookup"><span data-stu-id="d4090-108">There is one exception: the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is in the `https://www.microsoft.com/provisioning/EapHostConfig` namespace.</span></span>

<span data-ttu-id="d4090-109">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Seul l’élément [**EAPConfig**](onexschema-eapconfig-onex-element.md) est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d4090-109">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** Only the [**EAPConfig**](onexschema-eapconfig-onex-element.md) element is supported.</span></span> <span data-ttu-id="d4090-110">Les autres éléments, s’ils sont présents dans un profil, seront ignorés.</span><span class="sxs-lookup"><span data-stu-id="d4090-110">Other elements, if present in a profile, will be ignored.</span></span>

``` syntax
<xs:element name="OneX">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="cacheUserData"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="heldPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="startPeriod"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="integer"
                    >
                        <xs:enumeration
                            value="1"
                         />
                        <xs:enumeration
                            value="3600"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="maxStart"
                minOccurs="0"
            >
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
            <xs:element name="maxAuthFailures"
                minOccurs="0"
            >
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
            <xs:element name="supplicantMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="inhibitTransmission"
                         />
                        <xs:enumeration
                            value="includeLearning"
                         />
                        <xs:enumeration
                            value="compliant"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="authMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="machineOrUser"
                         />
                        <xs:enumeration
                            value="machine"
                         />
                        <xs:enumeration
                            value="user"
                         />
                        <xs:enumeration
                            value="guest"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="singleSignOn"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="type"
                            minOccurs="1"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="string"
                                >
                                    <xs:enumeration
                                        value="preLogon"
                                     />
                                    <xs:enumeration
                                        value="postLogon"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="maxDelay"
                            minOccurs="0"
                        >
                            <xs:simpleType>
                                <xs:restriction
                                    base="integer"
                                >
                                    <xs:enumeration
                                        value="0"
                                     />
                                    <xs:enumeration
                                        value="120"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="userBasedVirtualLan"
                            type="boolean"
                            minOccurs="0"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="EAPConfig">
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            minOccurs="1"
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

## <a name="child-elements"></a><span data-ttu-id="d4090-111">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="d4090-111">Child elements</span></span>



| <span data-ttu-id="d4090-112">Élément</span><span class="sxs-lookup"><span data-stu-id="d4090-112">Element</span></span>                                                                            | <span data-ttu-id="d4090-113">Type</span><span class="sxs-lookup"><span data-stu-id="d4090-113">Type</span></span>    | <span data-ttu-id="d4090-114">Description</span><span class="sxs-lookup"><span data-stu-id="d4090-114">Description</span></span>                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d4090-115">**authMode**</span><span class="sxs-lookup"><span data-stu-id="d4090-115">**authMode**</span></span>](onexschema-authmode-onex-element.md)                               |         | <span data-ttu-id="d4090-116">Spécifie le type d’informations d’identification utilisées pour l’authentification.</span><span class="sxs-lookup"><span data-stu-id="d4090-116">Specifies the type of credentials used for authentication.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d4090-117">**authPeriod**</span><span class="sxs-lookup"><span data-stu-id="d4090-117">**authPeriod**</span></span>](onexschema-authperiod-onex-element.md)                           |         | <span data-ttu-id="d4090-118">Spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="d4090-118">Specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span><br/>                                                                                                  |
| [<span data-ttu-id="d4090-119">**cacheUserData**</span><span class="sxs-lookup"><span data-stu-id="d4090-119">**cacheUserData**</span></span>](onexschema-cacheuserdata-onex-element.md)                     | <span data-ttu-id="d4090-120">boolean</span><span class="sxs-lookup"><span data-stu-id="d4090-120">boolean</span></span> | <span data-ttu-id="d4090-121">Spécifie si les informations d’identification de l’utilisateur sont mises en cache pour les connexions suivantes.</span><span class="sxs-lookup"><span data-stu-id="d4090-121">Specifies whether the user credentials are cached for subsequent connections.</span></span><br/>                                                                                                                                     |
| [<span data-ttu-id="d4090-122">**EAPConfig**</span><span class="sxs-lookup"><span data-stu-id="d4090-122">**EAPConfig**</span></span>](onexschema-eapconfig-onex-element.md)                             |         | <span data-ttu-id="d4090-123">Spécifie la configuration EAPHost.</span><span class="sxs-lookup"><span data-stu-id="d4090-123">Specifies the EAPHost configuration.</span></span><br/>                                                                                                                                                                              |
| [<span data-ttu-id="d4090-124">**heldPeriod**</span><span class="sxs-lookup"><span data-stu-id="d4090-124">**heldPeriod**</span></span>](onexschema-heldperiod-onex-element.md)                           |         | <span data-ttu-id="d4090-125">Spécifie la durée, en secondes, pendant laquelle un client ne tentera pas de nouveau l’authentification après l’échec d’une tentative d’authentification.</span><span class="sxs-lookup"><span data-stu-id="d4090-125">Specifies the length of time, in seconds, in which a client will not re-attempt authentication after a failed authentication attempt.</span></span><br/>                                                                             |
| [<span data-ttu-id="d4090-126">**maxAuthFailures**</span><span class="sxs-lookup"><span data-stu-id="d4090-126">**maxAuthFailures**</span></span>](onexschema-maxauthfailures-onex-element.md)                 |         | <span data-ttu-id="d4090-127">Spécifie le nombre maximal d’échecs d’authentification autorisé pour un ensemble d’informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="d4090-127">Specifies the maximum number of authentication failures allowed for a set of credentials.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="d4090-128">**maxDelay**</span><span class="sxs-lookup"><span data-stu-id="d4090-128">**maxDelay**</span></span>](onexschema-maxdelay-singlesignon-element.md)                       |         | <span data-ttu-id="d4090-129">Spécifie, en secondes, le délai maximal avant que la tentative de connexion d’authentification unique échoue.</span><span class="sxs-lookup"><span data-stu-id="d4090-129">Specifies, in seconds, the maximum delay before the single sign-on connection attempt fails.</span></span><br/>                                                                                                                      |
| [<span data-ttu-id="d4090-130">**maxStart**</span><span class="sxs-lookup"><span data-stu-id="d4090-130">**maxStart**</span></span>](onexschema-maxstart-onex-element.md)                               |         | <span data-ttu-id="d4090-131">Spécifie le nombre maximal de messages EAPOL-Start envoyés.</span><span class="sxs-lookup"><span data-stu-id="d4090-131">Specifies the maximum number of EAPOL-Start messages sent.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="d4090-132">**singleSignOn**</span><span class="sxs-lookup"><span data-stu-id="d4090-132">**singleSignOn**</span></span>](onexschema-singlesignon-onex-element.md)                       |         | <span data-ttu-id="d4090-133">Spécifie les informations de configuration du réseau à authentification unique.</span><span class="sxs-lookup"><span data-stu-id="d4090-133">Specifies single sign-on network configuration information.</span></span><br/>                                                                                                                                                       |
| [<span data-ttu-id="d4090-134">**startPeriod**</span><span class="sxs-lookup"><span data-stu-id="d4090-134">**startPeriod**</span></span>](onexschema-startperiod-onex-element.md)                         |         | <span data-ttu-id="d4090-135">Spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="d4090-135">Specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="d4090-136">**supplicantMode**</span><span class="sxs-lookup"><span data-stu-id="d4090-136">**supplicantMode**</span></span>](onexschema-supplicantmode-onex-element.md)                   |         | <span data-ttu-id="d4090-137">Spécifie la méthode de transmission utilisée pour les paquets EAPOL.</span><span class="sxs-lookup"><span data-stu-id="d4090-137">Specifies the method of transmission used for EAPOL packets.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="d4090-138">**entrer**</span><span class="sxs-lookup"><span data-stu-id="d4090-138">**type**</span></span>](onexschema-type-singlesignon-element.md)                               |         | <span data-ttu-id="d4090-139">Spécifie quand l’authentification unique est effectuée.</span><span class="sxs-lookup"><span data-stu-id="d4090-139">Specifies when single sign-on is performed.</span></span> <span data-ttu-id="d4090-140">Lorsque la valeur `preLogon` est définie sur, l’authentification unique est effectuée avant que l’utilisateur ouvre une session.</span><span class="sxs-lookup"><span data-stu-id="d4090-140">When set to `preLogon`, single sign-on is performed before the user logs on.</span></span> <span data-ttu-id="d4090-141">Lorsque la valeur `postLogon` est définie sur, l’authentification unique est effectuée immédiatement après la connexion de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4090-141">When set to `postLogon`, single sign-on is performed immediately after the user logs on.</span></span><br/> |
| [<span data-ttu-id="d4090-142">**userBasedVirtualLan**</span><span class="sxs-lookup"><span data-stu-id="d4090-142">**userBasedVirtualLan**</span></span>](onexschema-userbasedvirtuallan-singlesignon-element.md) | <span data-ttu-id="d4090-143">boolean</span><span class="sxs-lookup"><span data-stu-id="d4090-143">boolean</span></span> | <span data-ttu-id="d4090-144">Spécifie si le réseau local virtuel (VLAN) utilisé par l’appareil change en fonction des informations d’identification de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d4090-144">Specifies if the virtual LAN (VLAN) used by the device changes based on the user's credentials.</span></span><br/>                                                                                                                   |



## <a name="remarks"></a><span data-ttu-id="d4090-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d4090-145">Remarks</span></span>

<span data-ttu-id="d4090-146">Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [éléments de schéma Onex](onexschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="d4090-146">To view the list of child elements in a tree-like structure, see [OneX Schema Elements](onexschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4090-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4090-147">Requirements</span></span>



| <span data-ttu-id="d4090-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4090-148">Requirement</span></span> | <span data-ttu-id="d4090-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4090-149">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="d4090-150">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4090-150">Minimum supported client</span></span><br/> | <span data-ttu-id="d4090-151">Windows Vista, Windows XP avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4090-151">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d4090-152">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d4090-152">Minimum supported server</span></span><br/> | <span data-ttu-id="d4090-153">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d4090-153">Windows Server 2008 \[desktop apps only\]</span></span><br/>                |
| <span data-ttu-id="d4090-154">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="d4090-154">Redistributable</span></span><br/>          | <span data-ttu-id="d4090-155">API de réseau local sans fil pour Windows XP avec SP2</span><span class="sxs-lookup"><span data-stu-id="d4090-155">Wireless LAN API for Windows XP with SP2</span></span><br/>                 |



 

 




