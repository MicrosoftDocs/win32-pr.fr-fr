---
description: La structure UpdateEndpointProxySettings définit les paramètres de proxy utilisés lors de la demande d’un jeton.
ms.assetid: 24AA8843-D4EE-4F17-8B96-63ED25B365D2
title: UpdateEndpointProxySettings, structure (UpdateEndpointAuth. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointProxySettings
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: aad6ad294baab37b7516152438dbc9fd05f7036a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034033"
---
# <a name="updateendpointproxysettings-structure"></a><span data-ttu-id="0c5f2-103">UpdateEndpointProxySettings, structure</span><span class="sxs-lookup"><span data-stu-id="0c5f2-103">UpdateEndpointProxySettings structure</span></span>

<span data-ttu-id="0c5f2-104">La structure **UpdateEndpointProxySettings** définit les paramètres de proxy utilisés lors de la demande d’un jeton.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-104">The **UpdateEndpointProxySettings** structure defines the proxy settings used when requesting a token.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c5f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0c5f2-105">Syntax</span></span>


```C++
typedef struct tagUpdateEndpointProxySettings {
  BSTR szProxyAddr;
  BSTR szBypassList;
  BSTR szUserName;
  BSTR szPassword;
} UpdateEndpointProxySettings;
```



## <a name="members"></a><span data-ttu-id="0c5f2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="0c5f2-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="0c5f2-107">**szProxyAddr**</span><span class="sxs-lookup"><span data-stu-id="0c5f2-107">**szProxyAddr**</span></span>
</dt> <dd>

<span data-ttu-id="0c5f2-108">Le nom DNS ou l’adresse IP du serveur proxy à utiliser (par exemple, « proxy.somecorp.com » ou « 192.168.0.4 »), ou une chaîne vide si aucun proxy ne doit être utilisé.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-108">The DNS name or IP address of the proxy server to use (for example, "proxy.somecorp.com" or "192.168.0.4"), or an empty string if no proxy should be used.</span></span>

</dd> <dt>

<span data-ttu-id="0c5f2-109">**szBypassList**</span><span class="sxs-lookup"><span data-stu-id="0c5f2-109">**szBypassList**</span></span>
</dt> <dd>

<span data-ttu-id="0c5f2-110">Liste des adresses d’hôtes qui doivent contourner le serveur proxy, ou une chaîne vide si toutes les adresses d’hôte doivent utiliser le serveur proxy</span><span class="sxs-lookup"><span data-stu-id="0c5f2-110">A list of host addresses that should bypass the proxy server, or an empty string if all host addresses should use the proxy server</span></span>

<span data-ttu-id="0c5f2-111">WUA n’utilise pas ces données si **szProxyAddr** est vide.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-111">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c5f2-112">**szUserName**</span><span class="sxs-lookup"><span data-stu-id="0c5f2-112">**szUserName**</span></span>
</dt> <dd>

<span data-ttu-id="0c5f2-113">Nom d’utilisateur utilisé pour l’authentification auprès du serveur proxy, ou chaîne vide si aucune authentification n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-113">The username that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="0c5f2-114">WUA n’utilise pas ces données si **szProxyAddr** est vide.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-114">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> <dt>

<span data-ttu-id="0c5f2-115">**szPassword**</span><span class="sxs-lookup"><span data-stu-id="0c5f2-115">**szPassword**</span></span>
</dt> <dd>

<span data-ttu-id="0c5f2-116">Mot de passe utilisé pour l’authentification auprès du serveur proxy, ou chaîne vide si aucune authentification n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-116">The password that is used to authenticate with the proxy server, or the empty string if no authentication is needed.</span></span>

<span data-ttu-id="0c5f2-117">WUA n’utilise pas ces données si **szProxyAddr** est vide.</span><span class="sxs-lookup"><span data-stu-id="0c5f2-117">WUA does not use this data if **szProxyAddr** is empty.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0c5f2-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0c5f2-118">Requirements</span></span>



| <span data-ttu-id="0c5f2-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0c5f2-119">Requirement</span></span> | <span data-ttu-id="0c5f2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0c5f2-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c5f2-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c5f2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0c5f2-122">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c5f2-122">Windows 8 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="0c5f2-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0c5f2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0c5f2-124">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0c5f2-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0c5f2-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="0c5f2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c5f2-126"><dt>UpdateEndpointAuth. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c5f2-126"><dt>UpdateEndpointAuth.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c5f2-127">MIDL</span><span class="sxs-lookup"><span data-stu-id="0c5f2-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0c5f2-128"><dt>UpdateEndpointAuth. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0c5f2-128"><dt>UpdateEndpointAuth.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c5f2-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c5f2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c5f2-130">**GetEndpointToken**</span><span class="sxs-lookup"><span data-stu-id="0c5f2-130">**GetEndpointToken**</span></span>](iupdateendpointauthprovider-getendpointtoken.md)
</dt> </dl>

 

 




