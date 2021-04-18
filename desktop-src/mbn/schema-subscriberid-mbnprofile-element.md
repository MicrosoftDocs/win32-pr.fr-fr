---
description: Identifie l’identificateur unique du profil.
ms.assetid: 7572ef4f-ce7a-4595-a5ad-ade96e36d7d7
title: Élément abonné (MBNProfile)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SubscriberID
api_type:
- Schema
ms.openlocfilehash: ca098383aadd51e1e05d6b02bdd02a563eb0a09c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526619"
---
# <a name="subscriberid-mbnprofile-element"></a><span data-ttu-id="d0b80-103">Élément abonné (MBNProfile)</span><span class="sxs-lookup"><span data-stu-id="d0b80-103">SubscriberID (MBNProfile) Element</span></span>

<span data-ttu-id="d0b80-104">L’élément **abonné (MBNProfile)** identifie l’identificateur unique du profil.</span><span class="sxs-lookup"><span data-stu-id="d0b80-104">The **SubscriberID (MBNProfile)** element identifies the unique identifier of the profile.</span></span>

<span data-ttu-id="d0b80-105">Pour un réseau GSM, il doit contenir le IMSI (identité de l’abonné mobile international) de la carte SIM et des appareils CDMA. il doit contenir la valeur minimale (numéro d’identification mobile) de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="d0b80-105">For a GSM network this should contain the IMSI (International Mobile Subscriber Identity) of the SIM and for CDMA devices it should contain the MIN (Mobile Identification Number) of the device.</span></span>

<span data-ttu-id="d0b80-106">L’élément est une chaîne numérique d’une longueur maximale de 15 chiffres.</span><span class="sxs-lookup"><span data-stu-id="d0b80-106">The element is is a numeric string with a maximum length 15 digits.</span></span>

<span data-ttu-id="d0b80-107">L’élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d0b80-107">The element is required.</span></span>

``` syntax
<xs:element name="SubscriberID"
    type="subscriberIdType"
 />
```

<span data-ttu-id="d0b80-108">L’élément **abonné** est défini par l’élément [**MBNProfile**](schema-mbnprofile-element.md) .</span><span class="sxs-lookup"><span data-stu-id="d0b80-108">The **SubscriberID** element is defined by the [**MBNProfile**](schema-mbnprofile-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b80-109">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d0b80-109">Requirements</span></span>



| <span data-ttu-id="d0b80-110">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d0b80-110">Requirement</span></span> | <span data-ttu-id="d0b80-111">Valeur</span><span class="sxs-lookup"><span data-stu-id="d0b80-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------|
| <span data-ttu-id="d0b80-112">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0b80-112">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b80-113">Applications Windows 7 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="d0b80-113">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/> |
| <span data-ttu-id="d0b80-114">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0b80-114">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b80-115">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d0b80-115">None supported</span></span><br/>                         |



## <a name="see-also"></a><span data-ttu-id="d0b80-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d0b80-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="d0b80-117">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="d0b80-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="d0b80-118">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d0b80-118">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> <dt>

<span data-ttu-id="d0b80-119">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="d0b80-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="d0b80-120">**MBNProfile**</span><span class="sxs-lookup"><span data-stu-id="d0b80-120">**MBNProfile**</span></span>](schema-mbnprofile-element.md)
</dt> </dl>

 

 




