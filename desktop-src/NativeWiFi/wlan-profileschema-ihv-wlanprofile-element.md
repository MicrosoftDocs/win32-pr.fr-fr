---
description: Contient différents paramètres pour les fournisseurs de matériel indépendants.
ms.assetid: 4ad8c991-7849-41d6-9852-1ecadc372a2d
title: Élément IHV (WLANProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IHV
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d2d2902522c84ebe2939d42301a491521ac8a70f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524513"
---
# <a name="ihv-wlanprofile-element"></a><span data-ttu-id="707cb-103">Élément IHV (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="707cb-103">IHV (WLANProfile) Element</span></span>

<span data-ttu-id="707cb-104">L’élément IHV (WLANProfile) contient différents paramètres pour les fournisseurs de matériel indépendants.</span><span class="sxs-lookup"><span data-stu-id="707cb-104">The IHV (WLANProfile) element contains various settings for independent hardware vendors.</span></span> <span data-ttu-id="707cb-105">Si un profil comprend des paramètres de sécurité IHV, ceux-ci remplacent toute sécurité définie par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="707cb-105">If a profile includes IHV security settings, they override any Microsoft-defined security.</span></span>

<span data-ttu-id="707cb-106">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="707cb-106">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="IHV"
    minOccurs="0"
>
    <xs:complexType>
        <xs:sequence>
            <xs:element name="OUIHeader">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="OUI">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="3"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
                        </xs:element>
                        <xs:element name="type">
                            <xs:simpleType>
                                <xs:restriction
                                    base="hexBinary"
                                >
                                    <xs:length
                                        value="1"
                                     />
                                </xs:restriction>
                            </xs:simpleType>
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
            <xs:element name="connectivity"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="security"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
            <xs:element name="useMSOneX"
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
```

<span data-ttu-id="707cb-107">L’élément est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="707cb-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="707cb-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="707cb-108">Child elements</span></span>



| <span data-ttu-id="707cb-109">Élément</span><span class="sxs-lookup"><span data-stu-id="707cb-109">Element</span></span>                                                             | <span data-ttu-id="707cb-110">Type</span><span class="sxs-lookup"><span data-stu-id="707cb-110">Type</span></span>                                                              | <span data-ttu-id="707cb-111">Description</span><span class="sxs-lookup"><span data-stu-id="707cb-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="707cb-112">**connectivité**</span><span class="sxs-lookup"><span data-stu-id="707cb-112">**connectivity**</span></span>](wlan-profileschema-connectivity-ihv-element.md) |                                                                   | <span data-ttu-id="707cb-113">Contient des paramètres de connectivité liés aux IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-113">Contains IHV-related connectivity settings.</span></span><br/>                                                                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="707cb-114">**OUI**</span><span class="sxs-lookup"><span data-stu-id="707cb-114">**OUI**</span></span>](wlan-profileschema-oui-ouiheader-element.md)             |                                                                   | <span data-ttu-id="707cb-115">Contient une hexBinary de 3 octets qui identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-115">Contains a 3 byte hexBinary that identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="707cb-116">**OUIHeader**</span><span class="sxs-lookup"><span data-stu-id="707cb-116">**OUIHeader**</span></span>](wlan-profileschema-ouiheader-ihv-element.md)       |                                                                   | <span data-ttu-id="707cb-117">Identifie le IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-117">Identifies the IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="707cb-118">**caution**</span><span class="sxs-lookup"><span data-stu-id="707cb-118">**security**</span></span>](wlan-profileschema-security-ihv-element.md)         |                                                                   | <span data-ttu-id="707cb-119">Contient des paramètres de sécurité spécifiques au IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-119">Contains IHV-specific security settings.</span></span> <span data-ttu-id="707cb-120">Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="707cb-120">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="707cb-121">Le profil entier n’est pas valide si les deux paramètres de sécurité sont présents.</span><span class="sxs-lookup"><span data-stu-id="707cb-121">The entire profile is invalid if both security settings are present.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="707cb-122">**entrer**</span><span class="sxs-lookup"><span data-stu-id="707cb-122">**type**</span></span>](wlan-profileschema-type-ouiheader-element.md)           |                                                                   | <span data-ttu-id="707cb-123">Contient une valeur hexBinary de 1 octet qui est utilisée pour différencier les cartes réseau par le même IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-123">Contains a 1 byte hexBinary that is used to differentiate NICs by the same IHV.</span></span><br/>                                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="707cb-124">**useMSOneX**</span><span class="sxs-lookup"><span data-stu-id="707cb-124">**useMSOneX**</span></span>](wlan-profileschema-usemsonex-ihv-element.md)       | [<span data-ttu-id="707cb-125">boolean</span><span class="sxs-lookup"><span data-stu-id="707cb-125">boolean</span></span>](/dotnet/api/system.boolean) | <span data-ttu-id="707cb-126">Spécifie l’origine des paramètres de sécurité 802.1 X utilisés par un composant de sécurité IHV.</span><span class="sxs-lookup"><span data-stu-id="707cb-126">Specifies the origin of 802.1X security settings used by an IHV security component.</span></span> <span data-ttu-id="707cb-127">Quand [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) a la valeur true, les composants de sécurité IHV utilisent les paramètres 802.1 x définis par Microsoft.</span><span class="sxs-lookup"><span data-stu-id="707cb-127">When [**useMSOneX**](wlan-profileschema-usemsonex-ihv-element.md) is true, IHV security components use Microsoft-defined 802.1X settings.</span></span> <span data-ttu-id="707cb-128">Quand **useMSOneX** a la valeur false, les composants de sécurité IHV utilisent les paramètres 802.1 x fournis par le fournisseur.</span><span class="sxs-lookup"><span data-stu-id="707cb-128">When **useMSOneX** is false, IHV security components use vendor-supplied 802.1X settings.</span></span> <span data-ttu-id="707cb-129">Par défaut, **useMSOneX** a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="707cb-129">By default, **useMSOneX** is false.</span></span> <span data-ttu-id="707cb-130">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="707cb-130">This element is optional.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="707cb-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="707cb-131">Requirements</span></span>



| <span data-ttu-id="707cb-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="707cb-132">Requirement</span></span> | <span data-ttu-id="707cb-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="707cb-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="707cb-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707cb-134">Minimum supported client</span></span><br/> | <span data-ttu-id="707cb-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707cb-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="707cb-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="707cb-136">Minimum supported server</span></span><br/> | <span data-ttu-id="707cb-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="707cb-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="707cb-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="707cb-138">See also</span></span>

<dl> <dt>

<span data-ttu-id="707cb-139">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="707cb-139">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="707cb-140">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="707cb-140">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="707cb-141">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="707cb-141">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="707cb-142">**WLANProfile**</span><span class="sxs-lookup"><span data-stu-id="707cb-142">**WLANProfile**</span></span>](wlan-profileschema-wlanprofile-element.md)
</dt> </dl>

 

 
