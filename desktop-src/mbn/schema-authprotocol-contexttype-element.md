---
description: Spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: Élément AuthProtocol (contextType)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 8626d17a234784491c5f186f800943a6ab208bf0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516867"
---
# <a name="authprotocol-contexttype-element"></a><span data-ttu-id="812a8-103">Élément AuthProtocol (contextType)</span><span class="sxs-lookup"><span data-stu-id="812a8-103">AuthProtocol (contextType) Element</span></span>

<span data-ttu-id="812a8-104">L’élément **AuthProtocol (ContextType)** spécifie le protocole d’authentification à utiliser pour l’activation d’un contexte PDP (Packet Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="812a8-104">The **AuthProtocol (contextType)** element specifies the authentication protocol to be used for activating a Packet Data Protocol (PDP) context.</span></span>

<span data-ttu-id="812a8-105">L’élément peut avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="812a8-105">The element can have one of the following values.</span></span>

| <span data-ttu-id="812a8-106">Valeur</span><span class="sxs-lookup"><span data-stu-id="812a8-106">Value</span></span>      | <span data-ttu-id="812a8-107">Signification</span><span class="sxs-lookup"><span data-stu-id="812a8-107">Meaning</span></span>                                                                 |
|------------|-------------------------------------------------------------------------|
| <span data-ttu-id="812a8-108">None</span><span class="sxs-lookup"><span data-stu-id="812a8-108">"NONE"</span></span>     | <span data-ttu-id="812a8-109">Aucun protocole d’authentification.</span><span class="sxs-lookup"><span data-stu-id="812a8-109">No authentication protocol.</span></span>                                             |
| <span data-ttu-id="812a8-110">Protocole</span><span class="sxs-lookup"><span data-stu-id="812a8-110">"PAP"</span></span>      | <span data-ttu-id="812a8-111">Authentification par mot de passe non chiffrée.</span><span class="sxs-lookup"><span data-stu-id="812a8-111">Unencrypted password authentication.</span></span>                                    |
| <span data-ttu-id="812a8-112">CHAP</span><span class="sxs-lookup"><span data-stu-id="812a8-112">"CHAP"</span></span>     | <span data-ttu-id="812a8-113">Protocole CHAP (Challenge Handshake Authentication Protocol).</span><span class="sxs-lookup"><span data-stu-id="812a8-113">Challenge Handshake Authentication Protocol(CHAP).</span></span>                      |
|  <span data-ttu-id="812a8-114">MsCHAPV2</span><span class="sxs-lookup"><span data-stu-id="812a8-114">MsCHAPV2"</span></span> | <span data-ttu-id="812a8-115">Utilisez le protocole CHAP (Microsoft s Challenge Handshake Authentication Protocol) v 2.0.</span><span class="sxs-lookup"><span data-stu-id="812a8-115">Use Microsoft s Challenge Handshake Authentication Protocol(CHAP) v2.0.</span></span> |



 

<span data-ttu-id="812a8-116">Cet élément est facultatif et n’est utilisé que pour les profils GSM.</span><span class="sxs-lookup"><span data-stu-id="812a8-116">This element is optional and is used only for GSM profiles.</span></span> <span data-ttu-id="812a8-117">Si l’élément n’est pas spécifié et que le profil est destiné à un appareil GSM, le service haut débit mobile utilise **« None »**.</span><span class="sxs-lookup"><span data-stu-id="812a8-117">If the element is not specified and the profile is for a GSM device, then the Mobile Broadband service will use **"NONE"**.</span></span>

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

<span data-ttu-id="812a8-118">L’élément **AuthProtocol** est défini par le type complexe [**ContextType**](schema-contexttype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="812a8-118">The **AuthProtocol** element is defined by the [**contextType**](schema-contexttype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="812a8-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="812a8-119">Requirements</span></span>



| <span data-ttu-id="812a8-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="812a8-120">Requirement</span></span> | <span data-ttu-id="812a8-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="812a8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="812a8-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="812a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="812a8-123">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="812a8-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="812a8-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="812a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="812a8-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="812a8-125">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="812a8-126">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="812a8-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="812a8-127">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="812a8-127">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="812a8-128">**contextType**</span><span class="sxs-lookup"><span data-stu-id="812a8-128">**contextType**</span></span>](schema-contexttype-complextype.md)
</dt> <dt>

<span data-ttu-id="812a8-129">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="812a8-129">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="812a8-130">**Contexte (MBNProfile)**</span><span class="sxs-lookup"><span data-stu-id="812a8-130">**Context (MBNProfile)**</span></span>](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




