---
description: Spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 X pour l’authentification de port.
ms.assetid: fb01be74-46ad-4d8c-be4c-50ae05a0c33b
title: Élément OneXEnforced (Security)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OneXEnforced
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e6656238b0745f8bfef9aff5bcb0b80775dd1da2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521269"
---
# <a name="onexenforced-security-element"></a><span data-ttu-id="25454-103">Élément OneXEnforced (Security)</span><span class="sxs-lookup"><span data-stu-id="25454-103">OneXEnforced (security) Element</span></span>

<span data-ttu-id="25454-104">L’élément **OneXEnforced** (Security) spécifie si le service de configuration automatique pour les réseaux câblés requiert l’utilisation de 802.1 x pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="25454-104">The **OneXEnforced** (security) element specifies whether the automatic configuration service for wired networks requires the use of 802.1X for port authentication.</span></span> <span data-ttu-id="25454-105">Quand **OneXEnforced** a la valeur true, le service de configuration automatique doit utiliser 802.1 x pour l’authentification de port.</span><span class="sxs-lookup"><span data-stu-id="25454-105">When **OneXEnforced** is TRUE, the automatic configuration service must use 802.1X for port authentication.</span></span> <span data-ttu-id="25454-106">Quand **OneXEnforced** a la valeur false, le service de configuration automatique tente d’utiliser 802.1 x pour l’authentification de port, mais le service revient à aucune authentification si l’authentification 802.1 x échoue pour une raison quelconque.</span><span class="sxs-lookup"><span data-stu-id="25454-106">When **OneXEnforced** is FALSE, then the automatic configuration service will attempt to use 802.1X for port authentication, but the service will fall back to no authentication if 802.1X authentication fails for any reason.</span></span>

<span data-ttu-id="25454-107">Cet élément est facultatif.</span><span class="sxs-lookup"><span data-stu-id="25454-107">This element is optional.</span></span> <span data-ttu-id="25454-108">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="25454-108">The default value is FALSE.</span></span>

<span data-ttu-id="25454-109">Cet élément a une valeur significative uniquement si [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) a la valeur true.</span><span class="sxs-lookup"><span data-stu-id="25454-109">This element only has a meaningful value if [**OneXEnabled**](lan-profileschema-onexenabled-security-element.md) is TRUE.</span></span> <span data-ttu-id="25454-110">Si **OneXEnabled** a la valeur false, la valeur de cet élément est ignorée.</span><span class="sxs-lookup"><span data-stu-id="25454-110">If **OneXEnabled** is FALSE, then the value of this element is ignored.</span></span>

``` syntax
<xs:element name="OneXEnforced"
    type="boolean"
 />
```

<span data-ttu-id="25454-111">L’élément **OneXEnforced** est défini par l’élément de [**sécurité**](lan-profileschema-security-msm-element.md) .</span><span class="sxs-lookup"><span data-stu-id="25454-111">The **OneXEnforced** element is defined by the [**security**](lan-profileschema-security-msm-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="25454-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="25454-112">Requirements</span></span>



| <span data-ttu-id="25454-113">Condition requise</span><span class="sxs-lookup"><span data-stu-id="25454-113">Requirement</span></span> | <span data-ttu-id="25454-114">Valeur</span><span class="sxs-lookup"><span data-stu-id="25454-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="25454-115">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25454-115">Minimum supported client</span></span><br/> | <span data-ttu-id="25454-116">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25454-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="25454-117">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="25454-117">Minimum supported server</span></span><br/> | <span data-ttu-id="25454-118">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="25454-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="25454-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25454-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="25454-120">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="25454-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="25454-121">**caution**</span><span class="sxs-lookup"><span data-stu-id="25454-121">**security**</span></span>](lan-profileschema-security-msm-element.md)
</dt> <dt>

<span data-ttu-id="25454-122">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="25454-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="25454-123">**sécurité (MSM)**</span><span class="sxs-lookup"><span data-stu-id="25454-123">**security (MSM)**</span></span>](lan-profileschema-security-msm-element.md)
</dt> </dl>

 

 




