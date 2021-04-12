---
description: Spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 X.
ms.assetid: ab6cfc59-9cfd-45d3-ad27-306ad4f6d4e1
title: Élément OneXEnabled (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnabled
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 9c76fce3b42cff648d03f520ddeb569a39e99f99
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203761"
---
# <a name="onexenabled-security-element"></a><span data-ttu-id="a2eb5-103">Élément OneXEnabled (Security)</span><span class="sxs-lookup"><span data-stu-id="a2eb5-103">OneXEnabled (security) Element</span></span>

<span data-ttu-id="a2eb5-104">L’élément **OneXEnabled** (sécurité) spécifie si le service de configuration automatique pour les réseaux câblés tente une authentification de port à l’aide de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-104">The **OneXEnabled** (security) element specifies whether the automatic configuration service for wired networks will attempt port authentication using 802.1X.</span></span> <span data-ttu-id="a2eb5-105">Quand **OneXEnabled** a la valeur false, le service de configuration automatique n’utilise jamais 802.1 x pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-105">When **OneXEnabled** is FALSE, the automatic configuration service never uses 802.1X for port authentication.</span></span> <span data-ttu-id="a2eb5-106">Quand **OneXEnabled** a la valeur true, le service de configuration automatique tente l’authentification de port à l’aide de 802.1 x.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-106">When **OneXEnabled** is TRUE, then the automatic configuration service attempts port authentication using 802.1X.</span></span>

<span data-ttu-id="a2eb5-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-107">This element is optional.</span></span> <span data-ttu-id="a2eb5-108">La valeur par défaut est TRUE.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-108">The default value is TRUE.</span></span> <span data-ttu-id="a2eb5-109">Quand **OneXEnabled** n’est pas spécifié dans un profil, 802.1 x peut être utilisé pour l’authentification du port.</span><span class="sxs-lookup"><span data-stu-id="a2eb5-109">When **OneXEnabled** is not specified in a profile, then 802.1X may be used for port authentication.</span></span>

``` syntax
<xs:element name="OneXEnabled"
    type="boolean"
 />
```

<span data-ttu-id="a2eb5-110">L’élément **OneXEnabled** est défini par l’élément de [**sécurité**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="a2eb5-110">The **OneXEnabled** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2eb5-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2eb5-111">Requirements</span></span>



| <span data-ttu-id="a2eb5-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2eb5-112">Requirement</span></span> | <span data-ttu-id="a2eb5-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2eb5-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a2eb5-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2eb5-114">Minimum supported client</span></span><br/> | <span data-ttu-id="a2eb5-115">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2eb5-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a2eb5-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2eb5-116">Minimum supported server</span></span><br/> | <span data-ttu-id="a2eb5-117">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2eb5-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a2eb5-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a2eb5-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="a2eb5-119">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="a2eb5-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a2eb5-120">**caution**</span><span class="sxs-lookup"><span data-stu-id="a2eb5-120">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="a2eb5-121">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="a2eb5-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a2eb5-122">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="a2eb5-122">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




