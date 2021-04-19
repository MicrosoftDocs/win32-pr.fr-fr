---
description: Spécifie le nombre maximal de messages EAPOL-Start envoyés.
ms.assetid: 4e48f8b6-46eb-426e-ad22-3aa53cb66a17
title: Élément maxStart (OneX)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- maxStart
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 14bf40538eafb3c8e78b68b7a435d0d37d401960
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529818"
---
# <a name="maxstart-onex-element"></a><span data-ttu-id="7e4d8-103">Élément maxStart (OneX)</span><span class="sxs-lookup"><span data-stu-id="7e4d8-103">maxStart (OneX) Element</span></span>

<span data-ttu-id="7e4d8-104">L’élément maxStart (OneX) spécifie le nombre maximal de messages EAPOL-Start envoyés.</span><span class="sxs-lookup"><span data-stu-id="7e4d8-104">The maxStart (OneX) element specifies the maximum number of EAPOL-Start messages sent.</span></span> <span data-ttu-id="7e4d8-105">Une fois que le nombre maximal de messages de EAPOL-Start a été envoyé, le client suppose qu’il n’y a aucun authentificateur présent sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="7e4d8-105">After the maximum number of EAPOL-Start messages has been sent, the client assumes that there is no authenticator present on the network.</span></span>

<span data-ttu-id="7e4d8-106">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="7e4d8-106">This element is optional.</span></span> <span data-ttu-id="7e4d8-107">Quand maxStart n’est pas spécifié dans un profil, une valeur de 3 messages est utilisée.</span><span class="sxs-lookup"><span data-stu-id="7e4d8-107">When maxStart is not specified in a profile, a value of 3 messages is used.</span></span>

<span data-ttu-id="7e4d8-108">**Windows XP avec SP3 et l’API de réseau local sans fil pour Windows XP avec SP2 :** Cet élément sera ignoré s’il est présent dans un profil.</span><span class="sxs-lookup"><span data-stu-id="7e4d8-108">**Windows XP with SP3 and Wireless LAN API for Windows XP with SP2:** This element will be ignored if it is present in a profile.</span></span>

``` syntax
<xs:element name="maxStart">
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
```

<span data-ttu-id="7e4d8-109">L’élément **Maxstart** est défini par l’élément [**Onex**](onexschema-onex-element.md) .</span><span class="sxs-lookup"><span data-stu-id="7e4d8-109">The **maxStart** element is defined by the [**OneX**](onexschema-onex-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e4d8-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7e4d8-110">Requirements</span></span>



| <span data-ttu-id="7e4d8-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7e4d8-111">Requirement</span></span> | <span data-ttu-id="7e4d8-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7e4d8-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7e4d8-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e4d8-113">Minimum supported client</span></span><br/> | <span data-ttu-id="7e4d8-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e4d8-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7e4d8-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7e4d8-115">Minimum supported server</span></span><br/> | <span data-ttu-id="7e4d8-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7e4d8-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7e4d8-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7e4d8-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="7e4d8-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="7e4d8-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="7e4d8-119">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="7e4d8-119">**OneX**</span></span>](onexschema-onex-element.md)
</dt> <dt>

<span data-ttu-id="7e4d8-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="7e4d8-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="7e4d8-121">**802.1x**</span><span class="sxs-lookup"><span data-stu-id="7e4d8-121">**OneX**</span></span>](onexschema-onex-element.md)
</dt> </dl>

 

 




