---
description: Étend le schéma de profil WLAN v1 pour prendre en charge les réseaux hotspot 2,0.
ms.assetid: DE30DBCB-80B9-43D0-8DE1-56BBA99DBF31
title: Élément Hotspot2 (WLANProfile)
ms.topic: reference
ms.date: 10/08/2019
topic_type:
- APIRef
- kbSyntax
api_name:
- Hotspot2
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 0e372c1025a74dfb304cacdb0f3a4cf18bcdbabd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514855"
---
# <a name="hotspot2-wlanprofile-element"></a><span data-ttu-id="c7c24-103">Élément Hotspot2 (WLANProfile)</span><span class="sxs-lookup"><span data-stu-id="c7c24-103">Hotspot2 (WLANProfile) element</span></span>

<span data-ttu-id="c7c24-104">Étend le schéma de profil WLAN v1 pour prendre en charge les réseaux hotspot 2,0.</span><span class="sxs-lookup"><span data-stu-id="c7c24-104">Extends the WLAN Profile Schema v1 to support Hotspot 2.0 networks.</span></span> <span data-ttu-id="c7c24-105">La zone réactive 2,0 permet la connexion automatique aux services de Wi-Fi publics à l’aide des informations d’identification existantes et de l’appartenance aux réseaux de fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="c7c24-105">Hotspot 2.0 enables automatic connection to public Wi-Fi services using existing credentials and membership in service provider networks.</span></span> <span data-ttu-id="c7c24-106">Les fournisseurs de services spécifient la façon dont les connexions sont établies à l’aide des nouveaux éléments de schéma pour décrire les réseaux à utiliser et comment s’y authentifier.</span><span class="sxs-lookup"><span data-stu-id="c7c24-106">Service providers specify how connections are made using the new schema elements to describe which networks to use, and how to authenticate to them.</span></span>

``` syntax
<xs:element name="Hotspot2">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="DomainName"
                minOccurs="0"
             />
            <xs:element name="NAIRealm"
                minOccurs="0"
             />
            <xs:element name="Network3GPP"
                minOccurs="0"
             />
            <xs:element name="RoamingConsortium"
                minOccurs="0"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="c7c24-107">L’élément est défini par l’élément [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c7c24-107">The element is defined by the [**WLANProfile**](wlan-profileschema-wlanprofile-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7c24-108">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c7c24-108">Child elements</span></span>

| <span data-ttu-id="c7c24-109">Élément</span><span class="sxs-lookup"><span data-stu-id="c7c24-109">Element</span></span> | <span data-ttu-id="c7c24-110">Type</span><span class="sxs-lookup"><span data-stu-id="c7c24-110">Type</span></span> | <span data-ttu-id="c7c24-111">Description</span><span class="sxs-lookup"><span data-stu-id="c7c24-111">Description</span></span> |
|-|-|-|
| [<span data-ttu-id="c7c24-112">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="c7c24-112">**DomainName**</span></span>](wlan-profileschema-hotspot2-domainname-element.md) | | <span data-ttu-id="c7c24-113">Nom de domaine pour le fournisseur de réseau local de l’appareil, identifiant l’opérateur du réseau.</span><span class="sxs-lookup"><span data-stu-id="c7c24-113">The domain name for the device's Home Network Provider, identifying the operator of the network.</span></span> |
| [<span data-ttu-id="c7c24-114">**NAIRealm**</span><span class="sxs-lookup"><span data-stu-id="c7c24-114">**NAIRealm**</span></span>](wlan-profileschema-hotspot2-nairealm-element.md) | | <span data-ttu-id="c7c24-115">Liste d’identificateurs de domaine NAI (Network Access identifier).</span><span class="sxs-lookup"><span data-stu-id="c7c24-115">A list of Network Access Identifier (NAI) Realm identifiers.</span></span> <span data-ttu-id="c7c24-116">Les entrées de cette liste sont généralement de la forme user@domain .</span><span class="sxs-lookup"><span data-stu-id="c7c24-116">Entries in this list are usually of the form user@domain.</span></span> |
| [<span data-ttu-id="c7c24-117">**Network3GPP**</span><span class="sxs-lookup"><span data-stu-id="c7c24-117">**Network3GPP**</span></span>](wlan-profileschema-hotspot2-network3gpp-element.md) | | <span data-ttu-id="c7c24-118">Liste des ID PLMN (public Land Mobile Network).</span><span class="sxs-lookup"><span data-stu-id="c7c24-118">A list of Public Land Mobile Network (PLMN) IDs.</span></span> |
| [<span data-ttu-id="c7c24-119">**RoamingConsortium**</span><span class="sxs-lookup"><span data-stu-id="c7c24-119">**RoamingConsortium**</span></span>](wlan-profileschema-hotspot2-roamingconsortium-element.md) | | <span data-ttu-id="c7c24-120">Liste des identificateurs uniques (OUI) attribués par IEEE.</span><span class="sxs-lookup"><span data-stu-id="c7c24-120">A list of Organizationally Unique Identifiers (OUI) assigned by IEEE.</span></span>  |

## <a name="examples"></a><span data-ttu-id="c7c24-121">Exemples</span><span class="sxs-lookup"><span data-stu-id="c7c24-121">Examples</span></span>

```xml
<Hotspot2>
  <DomainName>contoso.com</DomainName>
  <NAIRealm>
    <name>test1@contoso.com</name>
    <name>test2@contoso.com</name>
  </NAIRealm>
  <Network3GPP>
    <PLMNID>12345</PLMNID>
    <PLMNID>123456</PLMNID>
  </Network3GPP>
  <RoamingConsortium>
    <OUI>00AABB</OUI>
    <OUI>001122</OUI>
  </RoamingConsortium>
</Hotspot2>
```
