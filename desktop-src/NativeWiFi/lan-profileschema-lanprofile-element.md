---
description: Contient un profil de réseau câblé.
ms.assetid: f5f9fcdc-febf-4730-8be4-5e1885d9ab08
title: Élément LANProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LANProfile
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 58ad88c9f975455bdd2d77a0ef8ee028d9027d9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203764"
---
# <a name="lanprofile-element"></a><span data-ttu-id="c600c-103">Élément LANProfile</span><span class="sxs-lookup"><span data-stu-id="c600c-103">LANProfile Element</span></span>

<span data-ttu-id="c600c-104">L’élément LANProfile contient un profil de réseau câblé.</span><span class="sxs-lookup"><span data-stu-id="c600c-104">The LANProfile element contains a wired network profile.</span></span> <span data-ttu-id="c600c-105">Cet élément est l’élément racine unique d’un profil de réseau câblé.</span><span class="sxs-lookup"><span data-stu-id="c600c-105">This element is the unique root element for a wired network profile.</span></span>

<span data-ttu-id="c600c-106">L’espace de noms cible de l’élément LANProfile est `https://www.microsoft.com/networking/LAN/profile/v1` .</span><span class="sxs-lookup"><span data-stu-id="c600c-106">The target namespace for the LANProfile element is `https://www.microsoft.com/networking/LAN/profile/v1`.</span></span>

``` syntax
<xs:element name="LANProfile">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="MSM">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="security">
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="OneXEnforced"
                                        type="boolean"
                                     />
                                    <xs:element name="OneXEnabled"
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
                        <xs:any
                            processContents="lax"
                            minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="c600c-107">Éléments enfants</span><span class="sxs-lookup"><span data-stu-id="c600c-107">Child elements</span></span>



| <span data-ttu-id="c600c-108">Élément</span><span class="sxs-lookup"><span data-stu-id="c600c-108">Element</span></span>                                                                 | <span data-ttu-id="c600c-109">Type</span><span class="sxs-lookup"><span data-stu-id="c600c-109">Type</span></span>    | <span data-ttu-id="c600c-110">Description</span><span class="sxs-lookup"><span data-stu-id="c600c-110">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c600c-111">**MSM**</span><span class="sxs-lookup"><span data-stu-id="c600c-111">**MSM**</span></span>](lan-profileschema-msm-lanprofile-element.md)                 |         | <span data-ttu-id="c600c-112">Contient les paramètres de module spécifique au média (MSM).</span><span class="sxs-lookup"><span data-stu-id="c600c-112">Contains media-specific module (MSM) settings.</span></span> <br/>                                                                               |
| [<span data-ttu-id="c600c-113">**OneXEnabled**</span><span class="sxs-lookup"><span data-stu-id="c600c-113">**OneXEnabled**</span></span>](lan-profileschema-onexenabled-security-element.md)   | <span data-ttu-id="c600c-114">boolean</span><span class="sxs-lookup"><span data-stu-id="c600c-114">boolean</span></span> | <span data-ttu-id="c600c-115">Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="c600c-115">Specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <br/>      |
| [<span data-ttu-id="c600c-116">**OneXEnforced**</span><span class="sxs-lookup"><span data-stu-id="c600c-116">**OneXEnforced**</span></span>](lan-profileschema-onexenforced-security-element.md) | <span data-ttu-id="c600c-117">boolean</span><span class="sxs-lookup"><span data-stu-id="c600c-117">boolean</span></span> | <span data-ttu-id="c600c-118">Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="c600c-118">Specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <br/> |
| [<span data-ttu-id="c600c-119">**caution**</span><span class="sxs-lookup"><span data-stu-id="c600c-119">**security**</span></span>](lan-profileschema-security-msm-element.md)              |         | <span data-ttu-id="c600c-120">Contient les paramètres de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c600c-120">Contains security settings.</span></span> <br/>                                                                                                  |



## <a name="remarks"></a><span data-ttu-id="c600c-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c600c-121">Remarks</span></span>

<span data-ttu-id="c600c-122">Pour afficher la liste des éléments enfants dans une structure de type arborescence, consultez [ \_ éléments de schéma de profil de réseau local](lan-profileschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="c600c-122">To view the list of child elements in a tree-like structure, see [LAN\_profile Schema Elements](lan-profileschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c600c-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c600c-123">Requirements</span></span>



| <span data-ttu-id="c600c-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c600c-124">Requirement</span></span> | <span data-ttu-id="c600c-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="c600c-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c600c-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c600c-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c600c-127">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c600c-127">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c600c-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c600c-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c600c-129">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c600c-129">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




