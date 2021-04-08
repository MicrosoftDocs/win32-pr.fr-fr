---
description: Spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.
ms.assetid: 5cb2e164-913f-4c35-854f-aac8ed180c46
title: Élément authPeriod (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- authPeriod
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 098391a672eedd2657dbd7ad5913fef13fde98cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034482"
---
# <a name="authperiod-onex-element"></a><span data-ttu-id="bbcd4-103">Élément authPeriod (OneX)</span><span class="sxs-lookup"><span data-stu-id="bbcd4-103">authPeriod (OneX) Element</span></span>

<span data-ttu-id="bbcd4-104">L’élément authPeriod (OneX) spécifie la durée maximale, en secondes, pendant laquelle un client attend une réponse de l’authentificateur.</span><span class="sxs-lookup"><span data-stu-id="bbcd4-104">The authPeriod (OneX) element specifies the maximum length of time, in seconds, in which a client waits for a response from the authenticator.</span></span> <span data-ttu-id="bbcd4-105">Si aucune réponse n’est reçue pendant la période spécifiée, le client part du principe qu’aucun authentificateur n’est présent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="bbcd4-105">If a response is not received within the specified period, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="bbcd4-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="bbcd4-106">This element is optional.</span></span> <span data-ttu-id="bbcd4-107">Quand authPeriod n’est pas spécifié dans un profil, une valeur de 18 secondes est utilisée.</span><span class="sxs-lookup"><span data-stu-id="bbcd4-107">When authPeriod is not specified in a profile, a value of 18 seconds is used.</span></span>

<span data-ttu-id="bbcd4-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="bbcd4-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="authPeriod">
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

<span data-ttu-id="bbcd4-109">L’élément **authPeriod** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="bbcd4-109">The **authPeriod** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="bbcd4-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bbcd4-110">Requirements</span></span>



| <span data-ttu-id="bbcd4-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bbcd4-111">Requirement</span></span> | <span data-ttu-id="bbcd4-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="bbcd4-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbcd4-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbcd4-113">Minimum supported client</span></span><br/> | <span data-ttu-id="bbcd4-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbcd4-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbcd4-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bbcd4-115">Minimum supported server</span></span><br/> | <span data-ttu-id="bbcd4-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bbcd4-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbcd4-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bbcd4-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="bbcd4-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="bbcd4-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="bbcd4-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bbcd4-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="bbcd4-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="bbcd4-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="bbcd4-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="bbcd4-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




