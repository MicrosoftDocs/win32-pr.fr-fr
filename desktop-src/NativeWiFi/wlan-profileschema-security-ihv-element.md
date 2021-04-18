---
description: Contient différents paramètres de sécurité utilisés par des fournisseurs de matériel indépendants.
ms.assetid: 237c5d98-3f3c-4279-b2ad-b0d05df041f9
title: Élément Security (IHV)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- security
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 6ace1bb0ca31f40fdc9d10fba13832797d8d4306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519972"
---
# <a name="security-ihv-element"></a><span data-ttu-id="1414b-103">Élément Security (IHV)</span><span class="sxs-lookup"><span data-stu-id="1414b-103">security (IHV) Element</span></span>

<span data-ttu-id="1414b-104">L’élément Security (IHV) contient différents paramètres de sécurité utilisés par des fournisseurs de matériel indépendants.</span><span class="sxs-lookup"><span data-stu-id="1414b-104">The security (IHV) element contains various security settings used by independent hardware vendors.</span></span>

<span data-ttu-id="1414b-105">Les paramètres de sécurité Microsoft et les paramètres de sécurité IHV s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="1414b-105">Microsoft security settings and IHV security settings are mutually exclusive.</span></span> <span data-ttu-id="1414b-106">Si les deux jeux de paramètres de sécurité sont présents dans le même profil, le profil n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="1414b-106">If both sets of security settings are present in the same profile, the profile is invalid.</span></span>

<span data-ttu-id="1414b-107">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="1414b-107">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element is not supported.</span></span>

``` syntax
<xs:element name="security">
    <xs:complexType>
        <xs:sequence>
            <xs:any
                processContents="lax"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="1414b-108">L’élément **Security** est défini par l’élément [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1414b-108">The **security** element is defined by the [**IHV**](wlan-profileschema-ihv-wlanprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="1414b-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1414b-109">Requirements</span></span>



| <span data-ttu-id="1414b-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1414b-110">Requirement</span></span> | <span data-ttu-id="1414b-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="1414b-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1414b-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1414b-112">Minimum supported client</span></span><br/> | <span data-ttu-id="1414b-113">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1414b-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1414b-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="1414b-114">Minimum supported server</span></span><br/> | <span data-ttu-id="1414b-115">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="1414b-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1414b-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1414b-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="1414b-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="1414b-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="1414b-118">**FABRICANTS**</span><span class="sxs-lookup"><span data-stu-id="1414b-118">**IHV**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> <dt>

<span data-ttu-id="1414b-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="1414b-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="1414b-120">**IHV (WLANProfile)**</span><span class="sxs-lookup"><span data-stu-id="1414b-120">**IHV (WLANProfile)**</span></span>](wlan-profileschema-ihv-wlanprofile-element.md)
</dt> </dl>

 

 




