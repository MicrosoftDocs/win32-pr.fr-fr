---
description: Spécifie si les ordinateurs utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil.
ms.assetid: c255e0a0-65ae-44a8-95cb-1a000394109d
title: enableAutoConfig (globalFlags), élément (LAN_policy) pour WLAN
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- enableAutoConfig
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5105b8e634aa5affa8648b763a82bbd60cbaec17
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2021
ms.locfileid: "106531177"
---
# <a name="enableautoconfig-globalflags-element-lan_policy-for-wlan"></a><span data-ttu-id="67466-103">enableAutoConfig (globalFlags), élément (LAN_policy) pour WLAN</span><span class="sxs-lookup"><span data-stu-id="67466-103">enableAutoConfig (globalFlags) Element (LAN_policy) for WLAN</span></span> 

<span data-ttu-id="67466-104">L’élément **enableAutoConfig** (globalFlags) spécifie si les machines utilisent le service de configuration automatique intégré (AutoConfig) pour gérer les connexions sans fil.</span><span class="sxs-lookup"><span data-stu-id="67466-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <span data-ttu-id="67466-105">Lorsque **enableAutoConfig** a la valeur false, les ordinateurs ne doivent pas utiliser la configuration automatique pour gérer les connexions sans fil, et le service de configuration automatique répond uniquement aux demandes d’activation du service.</span><span class="sxs-lookup"><span data-stu-id="67466-105">When **enableAutoConfig** has a value of FALSE, machines must not use AutoConfig to manage wireless connections, and the AutoConfig service only responds to requests to enable the service.</span></span> <span data-ttu-id="67466-106">Lorsque **enableAutoConfig** a la valeur true, les machines peuvent utiliser le service de configuration automatique.</span><span class="sxs-lookup"><span data-stu-id="67466-106">When **enableAutoConfig** has a value of TRUE, machines may use the AutoConfig service.</span></span>

<span data-ttu-id="67466-107">Cet élément est obligatoire.</span><span class="sxs-lookup"><span data-stu-id="67466-107">This element is mandatory.</span></span> <span data-ttu-id="67466-108">Lorsqu’un profil est créé par le service de configuration automatique, cet élément a la valeur par défaut TRUE.</span><span class="sxs-lookup"><span data-stu-id="67466-108">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="67466-109">L’élément **enableAutoConfig** est défini par l’élément [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="67466-109">The **enableAutoConfig** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="67466-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67466-110">Requirements</span></span>



| <span data-ttu-id="67466-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67466-111">Requirement</span></span> | <span data-ttu-id="67466-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="67466-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="67466-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67466-113">Minimum supported client</span></span><br/> | <span data-ttu-id="67466-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67466-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="67466-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67466-115">Minimum supported server</span></span><br/> | <span data-ttu-id="67466-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67466-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67466-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67466-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="67466-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="67466-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="67466-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="67466-119">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="67466-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="67466-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="67466-121">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="67466-121">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




