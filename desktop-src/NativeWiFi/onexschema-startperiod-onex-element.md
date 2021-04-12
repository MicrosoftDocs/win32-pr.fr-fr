---
description: Spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.
ms.assetid: 6163eeb9-23a8-4e34-ad3f-016946e241e2
title: Élément startPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- startPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: a583403a354cbefe93387be2d5af06958bbf6b28
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319114"
---
# <a name="startperiod-onex-element"></a><span data-ttu-id="31e0a-103">Élément startPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="31e0a-103">startPeriod (OneX) Element</span></span>

<span data-ttu-id="31e0a-104">L’élément startPeriod (OneX) spécifie la durée d’attente, en secondes, avant l’envoi d’un EAPOL-Start.</span><span class="sxs-lookup"><span data-stu-id="31e0a-104">The startPeriod (OneX) element specifies the length of time, in seconds, to wait before an EAPOL-Start is sent.</span></span> <span data-ttu-id="31e0a-105">Un message de EAPOL-Start est envoyé pour démarrer le processus d’authentification 802.1 X.</span><span class="sxs-lookup"><span data-stu-id="31e0a-105">An EAPOL-Start message is sent to start the 802.1X authentication process.</span></span>

<span data-ttu-id="31e0a-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="31e0a-106">This element is optional.</span></span> <span data-ttu-id="31e0a-107">Quand startPeriod n’est pas spécifié dans un profil, une valeur de 5 secondes est utilisée.</span><span class="sxs-lookup"><span data-stu-id="31e0a-107">When startPeriod is not specified in a profile, a value of 5 seconds is used.</span></span>

<span data-ttu-id="31e0a-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="31e0a-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="startPeriod">
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
```

<span data-ttu-id="31e0a-109">L’élément **startPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="31e0a-109">The **startPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="31e0a-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="31e0a-110">Requirements</span></span>



| <span data-ttu-id="31e0a-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="31e0a-111">Requirement</span></span> | <span data-ttu-id="31e0a-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="31e0a-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31e0a-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e0a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="31e0a-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31e0a-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31e0a-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="31e0a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="31e0a-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="31e0a-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="31e0a-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31e0a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="31e0a-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="31e0a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="31e0a-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="31e0a-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="31e0a-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="31e0a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="31e0a-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="31e0a-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




