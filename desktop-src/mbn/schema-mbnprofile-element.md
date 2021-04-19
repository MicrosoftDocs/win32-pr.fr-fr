---
description: Est l’élément racine qui identifie un profil haut débit mobile.
ms.assetid: 08302e7f-3024-439b-a2ad-a4ae9487b82b
title: Élément MBNProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MBNProfile
api_type:
- Schema
ms.openlocfilehash: 7016d492a70192a7d6accdcb3aaa57a9c564960e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516489"
---
# <a name="mbnprofile-element"></a><span data-ttu-id="41d8a-103">Élément MBNProfile</span><span class="sxs-lookup"><span data-stu-id="41d8a-103">MBNProfile Element</span></span>

<span data-ttu-id="41d8a-104">L’élément **MBNProfile** est l’élément racine qui identifie un profil haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="41d8a-104">The **MBNProfile** element is the root element that identifies a Mobile Broadband profile.</span></span>

<span data-ttu-id="41d8a-105">Il ne peut y avoir qu’un seul élément de ce type par document.</span><span class="sxs-lookup"><span data-stu-id="41d8a-105">There can only be one element of this type per document.</span></span>

``` syntax
<xs:element name="MBNProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="Name"
                type="nameType"
             />
            <xs:element name="Description"
                type="nameType"
                minOccurs="0"
             />
            <xs:element name="ICONFilePath"
                type="iconFileType"
                minOccurs="0"
             />
            <xs:element name="IsDefault"
                type="boolean"
             />
            <xs:element name="ProfileCreationType"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="token"
                    >
                        <xs:enumeration
                            value="UserProvisioned"
                         />
                        <xs:enumeration
                            value="AdminProvisioned"
                         />
                        <xs:enumeration
                            value="OperatorProvisioned"
                         />
                        <xs:enumeration
                            value="DeviceProvisioned"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="SubscriberID"
                type="subscriberIdType"
             />
            <xs:element name="SimIccID"
                type="simIccIDType"
                minOccurs="0"
             />
            <xs:element name="HomeProviderName"
                type="providerNameType"
                minOccurs="0"
             />
            <xs:element name="AutoConnectOnInternet"
                type="boolean"
                minOccurs="0"
             />
            <xs:element name="ConnectionMode"
                minOccurs="0"
            >
                <xs:simpleType>
                    <xs:restriction
                        base="string"
                    >
                        <xs:enumeration
                            value="manual"
                         />
                        <xs:enumeration
                            value="auto"
                         />
                        <xs:enumeration
                            value="auto-home"
                         />
                    </xs:restriction>
                </xs:simpleType>
            </xs:element>
            <xs:element name="Context"
                type="contextType"
                minOccurs="0"
             />
            <xs:element name="DataRoamingPartners"
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
```

## <a name="child-elements"></a><span data-ttu-id="41d8a-106">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="41d8a-106">Child elements</span></span>



| <span data-ttu-id="41d8a-107">Élément</span><span class="sxs-lookup"><span data-stu-id="41d8a-107">Element</span></span>                                                                          | <span data-ttu-id="41d8a-108">Type</span><span class="sxs-lookup"><span data-stu-id="41d8a-108">Type</span></span>                                                           | <span data-ttu-id="41d8a-109">Description</span><span class="sxs-lookup"><span data-stu-id="41d8a-109">Description</span></span>                                               |
|----------------------------------------------------------------------------------|----------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="41d8a-110">**AutoConnectOnInternet**</span><span class="sxs-lookup"><span data-stu-id="41d8a-110">**AutoConnectOnInternet**</span></span>](schema-autoconnectoninternet-mbnprofile-element.md) | <span data-ttu-id="41d8a-111">boolean</span><span class="sxs-lookup"><span data-stu-id="41d8a-111">boolean</span></span>                                                        | <span data-ttu-id="41d8a-112">Indique si l’appareil se connecte automatiquement.</span><span class="sxs-lookup"><span data-stu-id="41d8a-112">Whether the device will automatically connect.</span></span><br/> |
| [<span data-ttu-id="41d8a-113">**ConnectionMode**</span><span class="sxs-lookup"><span data-stu-id="41d8a-113">**ConnectionMode**</span></span>](schema-connectionmode-mbnprofile-element.md)               |                                                                | <span data-ttu-id="41d8a-114">Paramètres de connexion automatique de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="41d8a-114">The device auto connection settings.</span></span><br/>           |
| [<span data-ttu-id="41d8a-115">**Context**</span><span class="sxs-lookup"><span data-stu-id="41d8a-115">**Context**</span></span>](schema-context-mbnprofile-element.md)                             | [<span data-ttu-id="41d8a-116">**contextType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-116">**contextType**</span></span>](schema-contexttype-complextype.md)          | <span data-ttu-id="41d8a-117">Paramètres de configuration de la connexion de données.</span><span class="sxs-lookup"><span data-stu-id="41d8a-117">Data connection setup parameters.</span></span><br/>              |
| [<span data-ttu-id="41d8a-118">**DataRoamingPartners**</span><span class="sxs-lookup"><span data-stu-id="41d8a-118">**DataRoamingPartners**</span></span>](schema-dataroamingpartners-mbnprofile-element.md)     |                                                                | <span data-ttu-id="41d8a-119">Fournisseurs de réseau préférés pour l’itinérance.</span><span class="sxs-lookup"><span data-stu-id="41d8a-119">Preferred network providers for roaming.</span></span><br/>       |
| [<span data-ttu-id="41d8a-120">**Description**</span><span class="sxs-lookup"><span data-stu-id="41d8a-120">**Description**</span></span>](schema-description-mbnprofile-element.md)                     | [<span data-ttu-id="41d8a-121">**nameType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-121">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="41d8a-122">Description du profil.</span><span class="sxs-lookup"><span data-stu-id="41d8a-122">Description of the profile.</span></span><br/>                    |
| [<span data-ttu-id="41d8a-123">**HomeProviderName**</span><span class="sxs-lookup"><span data-stu-id="41d8a-123">**HomeProviderName**</span></span>](schema-homeprovidername-mbnprofile-element.md)           | [<span data-ttu-id="41d8a-124">**providerNameType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-124">**providerNameType**</span></span>](schema-providernametype-simpletype.md) | <span data-ttu-id="41d8a-125">Nom du fournisseur d’hébergement.</span><span class="sxs-lookup"><span data-stu-id="41d8a-125">Name of the home provider.</span></span><br/>                     |
| [<span data-ttu-id="41d8a-126">**ICONFilePath**</span><span class="sxs-lookup"><span data-stu-id="41d8a-126">**ICONFilePath**</span></span>](schema-iconfilepath-mbnprofile-element.md)                   | [<span data-ttu-id="41d8a-127">**iconFileType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-127">**iconFileType**</span></span>](schema-iconfiletype-simpletype.md)         | <span data-ttu-id="41d8a-128">Chemin d’accès au fichier d’icône.</span><span class="sxs-lookup"><span data-stu-id="41d8a-128">Path to the icon file.</span></span><br/>                         |
| [<span data-ttu-id="41d8a-129">**IsDefault**</span><span class="sxs-lookup"><span data-stu-id="41d8a-129">**IsDefault**</span></span>](schema-isdefault-mbnprofile-element.md)                         | <span data-ttu-id="41d8a-130">boolean</span><span class="sxs-lookup"><span data-stu-id="41d8a-130">boolean</span></span>                                                        | <span data-ttu-id="41d8a-131">Indique si le profil est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="41d8a-131">Whether the profile is the default.</span></span><br/>            |
| [<span data-ttu-id="41d8a-132">**Nom**</span><span class="sxs-lookup"><span data-stu-id="41d8a-132">**Name**</span></span>](schema-name-mbnprofile-element.md)                                   | [<span data-ttu-id="41d8a-133">**nameType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-133">**nameType**</span></span>](schema-nametype-simpletype.md)                 | <span data-ttu-id="41d8a-134">Nom du profil.</span><span class="sxs-lookup"><span data-stu-id="41d8a-134">Name of the profile.</span></span><br/>                           |
| [<span data-ttu-id="41d8a-135">**ProfileCreationType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-135">**ProfileCreationType**</span></span>](schema-profilecreationtype-mbnprofile-element.md)     |                                                                | <span data-ttu-id="41d8a-136">Informations sur le créateur du profil.</span><span class="sxs-lookup"><span data-stu-id="41d8a-136">Information about the profile creator.</span></span><br/>         |
| [<span data-ttu-id="41d8a-137">**SimIccID**</span><span class="sxs-lookup"><span data-stu-id="41d8a-137">**SimIccID**</span></span>](schema-simiccid-mbnprofile-element.md)                           | [<span data-ttu-id="41d8a-138">**simIccIDType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-138">**simIccIDType**</span></span>](schema-simiccidtype-simpletype.md)         | <span data-ttu-id="41d8a-139">Numéro d’identification SIM pour les appareils GSM.</span><span class="sxs-lookup"><span data-stu-id="41d8a-139">SIM identification number for GSM devices.</span></span><br/>     |
| [<span data-ttu-id="41d8a-140">**Abonné**</span><span class="sxs-lookup"><span data-stu-id="41d8a-140">**SubscriberID**</span></span>](schema-subscriberid-mbnprofile-element.md)                   | [<span data-ttu-id="41d8a-141">**subscriberIdType**</span><span class="sxs-lookup"><span data-stu-id="41d8a-141">**subscriberIdType**</span></span>](schema-subscriberidtype-simpletype.md) | <span data-ttu-id="41d8a-142">Identificateur unique du profil.</span><span class="sxs-lookup"><span data-stu-id="41d8a-142">Unique identifier of the profile.</span></span><br/>              |



## <a name="requirements"></a><span data-ttu-id="41d8a-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="41d8a-143">Requirements</span></span>



| <span data-ttu-id="41d8a-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="41d8a-144">Requirement</span></span> | <span data-ttu-id="41d8a-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="41d8a-145">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="41d8a-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d8a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="41d8a-147">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="41d8a-147">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="41d8a-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d8a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="41d8a-149">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="41d8a-149">None supported</span></span><br/>                         |



 

 




