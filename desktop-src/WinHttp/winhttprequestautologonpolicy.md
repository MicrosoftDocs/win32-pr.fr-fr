---
description: Comprend les paramètres possibles pour la stratégie d’ouverture de session automatique.
ms.assetid: dad4f6a7-8e84-4f4f-b962-4189e3dc01f7
title: Énumération WinHttpRequestAutoLogonPolicy
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WinHttpRequestAutoLogonPolicy
api_type:
- IDLDef
api_location:
- HttpRequest.idl
ms.openlocfilehash: dab3dc14dd194e36b9b4d1225f77161005b9d21b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515456"
---
# <a name="winhttprequestautologonpolicy-enumeration"></a><span data-ttu-id="3e145-103">Énumération WinHttpRequestAutoLogonPolicy</span><span class="sxs-lookup"><span data-stu-id="3e145-103">WinHttpRequestAutoLogonPolicy enumeration</span></span>

<span data-ttu-id="3e145-104">L’énumération **WinHttpRequestAutoLogonPolicy** comprend des paramètres possibles pour la [stratégie d’ouverture de session automatique](authentication-in-winhttp.md).</span><span class="sxs-lookup"><span data-stu-id="3e145-104">The **WinHttpRequestAutoLogonPolicy** enumeration includes possible settings for the [Automatic Logon Policy](authentication-in-winhttp.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="3e145-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3e145-105">Syntax</span></span>


```C++
typedef enum WinHttpRequestAutoLogonPolicy { 
  AutoLogonPolicy_Always             = 0,
  AutoLogonPolicy_OnlyIfBypassProxy  = 1,
  AutoLogonPolicy_Never              = 2
} WinHttpRequestAutoLogonPolicy;
```



## <a name="constants"></a><span data-ttu-id="3e145-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="3e145-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3e145-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy \_ toujours**</span><span class="sxs-lookup"><span data-stu-id="3e145-107"><span id="AutoLogonPolicy_Always"></span><span id="autologonpolicy_always"></span><span id="AUTOLOGONPOLICY_ALWAYS"></span>**AutoLogonPolicy\_Always**</span></span>
</dt> <dd>

<span data-ttu-id="3e145-108">Une ouverture de session authentifiée, à l’aide des informations d’identification par défaut, est effectuée pour toutes les demandes.</span><span class="sxs-lookup"><span data-stu-id="3e145-108">An authenticated log on, using the default credentials, is performed for all requests.</span></span>

</dd> <dt>

<span data-ttu-id="3e145-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy \_ OnlyIfBypassProxy**</span><span class="sxs-lookup"><span data-stu-id="3e145-109"><span id="AutoLogonPolicy_OnlyIfBypassProxy"></span><span id="autologonpolicy_onlyifbypassproxy"></span><span id="AUTOLOGONPOLICY_ONLYIFBYPASSPROXY"></span>**AutoLogonPolicy\_OnlyIfBypassProxy**</span></span>
</dt> <dd>

<span data-ttu-id="3e145-110">Une ouverture de session authentifiée, à l’aide des informations d’identification par défaut, est exécutée uniquement pour les demandes sur l’intranet local.</span><span class="sxs-lookup"><span data-stu-id="3e145-110">An authenticated log on, using the default credentials, is performed only for requests on the local intranet.</span></span> <span data-ttu-id="3e145-111">L’intranet local est considéré comme n’importe quel serveur de la liste de contournement du proxy dans la configuration du proxy actuel.</span><span class="sxs-lookup"><span data-stu-id="3e145-111">The local intranet is considered to be any server on the proxy bypass list in the current proxy configuration.</span></span>

</dd> <dt>

<span data-ttu-id="3e145-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy \_ jamais**</span><span class="sxs-lookup"><span data-stu-id="3e145-112"><span id="AutoLogonPolicy_Never"></span><span id="autologonpolicy_never"></span><span id="AUTOLOGONPOLICY_NEVER"></span>**AutoLogonPolicy\_Never**</span></span>
</dt> <dd>

<span data-ttu-id="3e145-113">L’authentification n’est pas utilisée automatiquement.</span><span class="sxs-lookup"><span data-stu-id="3e145-113">Authentication is not used automatically.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3e145-114">Notes</span><span class="sxs-lookup"><span data-stu-id="3e145-114">Remarks</span></span>

<span data-ttu-id="3e145-115">Pour définir la stratégie d’ouverture de session automatique, appelez la méthode [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) et spécifiez l’une des constantes précédentes.</span><span class="sxs-lookup"><span data-stu-id="3e145-115">To set the automatic logon policy, call the [**SetAutoLogonPolicy**](iwinhttprequest-setautologonpolicy.md) method and specify one of the preceding constants.</span></span>

> [!Note]  
> <span data-ttu-id="3e145-116">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="3e145-116">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHTTP start page.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e145-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e145-117">Requirements</span></span>



| <span data-ttu-id="3e145-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e145-118">Requirement</span></span> | <span data-ttu-id="3e145-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e145-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e145-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e145-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3e145-121">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e145-121">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="3e145-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e145-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3e145-123">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e145-123">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="3e145-124">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="3e145-124">Redistributable</span></span><br/>          | <span data-ttu-id="3e145-125">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="3e145-125">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="3e145-126">MIDL</span><span class="sxs-lookup"><span data-stu-id="3e145-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e145-127"><dt>HttpRequest. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e145-127"><dt>HttpRequest.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e145-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3e145-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e145-129">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="3e145-129">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

 




