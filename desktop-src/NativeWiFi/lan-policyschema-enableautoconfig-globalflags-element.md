---
description: Spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 X).
ms.assetid: c7a0f6bc-4d42-4d95-8483-2c480f4d8db9
title: enableAutoConfig (globalFlags), élément (LAN_policy)
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
ms.openlocfilehash: af1ca32f177140bbfc6563f74df5afc519ee0c75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103757798"
---
# <a name="enableautoconfig-globalflags-element-lan_policy"></a><span data-ttu-id="f9d3c-103">enableAutoConfig (globalFlags), élément (LAN_policy)</span><span class="sxs-lookup"><span data-stu-id="f9d3c-103">enableAutoConfig (globalFlags) Element (LAN_policy)</span></span>

<span data-ttu-id="f9d3c-104">L’élément **enableAutoConfig** (globalFlags) spécifie si les machines utilisent le service de configuration automatique intégré pour gérer les connexions aux réseaux câblés qui requièrent l’authentification de couche 2 (par exemple, 802.1 x).</span><span class="sxs-lookup"><span data-stu-id="f9d3c-104">The **enableAutoConfig** (globalFlags) element specifies whether machines use the built-in automatic configuration service to manage connections to wired networks that require layer 2 authentication (such as 802.1X).</span></span>

<span data-ttu-id="f9d3c-105">Lorsque **enableAutoConfig** a la valeur false, les ordinateurs ne doivent pas utiliser le service de configuration automatique intégré pour gérer les connexions qui requièrent l’authentification de couche 2.</span><span class="sxs-lookup"><span data-stu-id="f9d3c-105">When **enableAutoConfig** has a value of FALSE, machines must not use built-in automatic configuration service to manage connections that require layer 2 authentication.</span></span> <span data-ttu-id="f9d3c-106">Au lieu de cela, le réseau spécifié dans l’élément [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) est le seul réseau disponible pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="f9d3c-106">Instead, the network specified in the [**profileList**](lan-policyschema-profilelist-lanpolicy-element.md) element is the only network available for connection.</span></span> <span data-ttu-id="f9d3c-107">Le service de configuration automatique répond uniquement aux demandes d’activation du service.</span><span class="sxs-lookup"><span data-stu-id="f9d3c-107">The automatic configuration service will only respond to requests to enable the service.</span></span>

<span data-ttu-id="f9d3c-108">Lorsque **enableAutoConfig** a la valeur true, les machines peuvent utiliser le service de configuration automatique intégré pour se connecter aux réseaux câblés qui requièrent l’authentification de couche 2.</span><span class="sxs-lookup"><span data-stu-id="f9d3c-108">When **enableAutoConfig** has a value of TRUE, machines may use the built-in automatic configuration service to connect to wired networks that require layer 2 authentication.</span></span>

``` syntax
<xs:element name="enableAutoConfig"
    type="boolean"
 />
```

<span data-ttu-id="f9d3c-109">L’élément **enableAutoConfig** est défini par l’élément [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f9d3c-109">The **enableAutoConfig** element is defined by the [**globalFlags**](lan-policyschema-globalflags-lanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d3c-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9d3c-110">Requirements</span></span>



| <span data-ttu-id="f9d3c-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9d3c-111">Requirement</span></span> | <span data-ttu-id="f9d3c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9d3c-112">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9d3c-113">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9d3c-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f9d3c-114">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9d3c-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f9d3c-115">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f9d3c-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f9d3c-116">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f9d3c-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9d3c-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9d3c-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="f9d3c-118">**Contexte de définition de l’élément dans le schéma**</span><span class="sxs-lookup"><span data-stu-id="f9d3c-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f9d3c-119">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="f9d3c-119">**globalFlags**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="f9d3c-120">**Élément parent immédiat possible dans l’instance de schéma**</span><span class="sxs-lookup"><span data-stu-id="f9d3c-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f9d3c-121">**globalFlags (LANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="f9d3c-121">**globalFlags (LANPolicy)**</span></span>](lan-policyschema-globalflags-lanpolicy-element.md)
</dt> </dl>

 

 




