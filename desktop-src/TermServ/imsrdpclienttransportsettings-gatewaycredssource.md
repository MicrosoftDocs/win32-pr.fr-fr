---
title: IMsRdpClientTransportSettings propriété GatewayCredsSource
description: Spécifie ou récupère la méthode d’authentification de la passerelle des services Bureau à Bureau à distance.
ms.assetid: 3b05edcb-f678-4d80-99fd-b76d27c80c68
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayCredsSource
- Services Bureau à distance de la propriété GatewayCredsSource, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayCredsSource
- IMsRdpClientTransportSettings.get_GatewayCredsSource
- IMsRdpClientTransportSettings.put_GatewayCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2771998ddc7c53d05c5d0db452f34a734a7c3e58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384175"
---
# <a name="imsrdpclienttransportsettingsgatewaycredssource-property"></a><span data-ttu-id="cc0db-106">IMsRdpClientTransportSettings :: GatewayCredsSource, propriété</span><span class="sxs-lookup"><span data-stu-id="cc0db-106">IMsRdpClientTransportSettings::GatewayCredsSource property</span></span>

<span data-ttu-id="cc0db-107">Spécifie ou récupère la méthode d’authentification de la passerelle des services Bureau à Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc0db-107">Specifies or retrieves the Remote Desktop Gateway (RD Gateway) authentication method.</span></span>

<span data-ttu-id="cc0db-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="cc0db-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc0db-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc0db-109">Syntax</span></span>


```C++
HRESULT put_GatewayCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="cc0db-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="cc0db-110">Property value</span></span>

<span data-ttu-id="cc0db-111">Variable **ULong** qui spécifie la méthode d’authentification de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc0db-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="cc0db-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="cc0db-112">This parameter can be one of the following values.</span></span>

<dt>

<span data-ttu-id="cc0db-113">MODE d’identification du \_ proxy TSC \_ \_ \_ USERPASS (0)</span><span class="sxs-lookup"><span data-stu-id="cc0db-113">TSC\_PROXY\_CREDS\_MODE\_USERPASS (0)</span></span>
</dt> <dd>

<span data-ttu-id="cc0db-114">Utilisez un mot de passe (NTLM) comme méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc0db-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="cc0db-115">\_Carte à puce en mode d’identification TSC proxy \_ \_ \_ (1)</span><span class="sxs-lookup"><span data-stu-id="cc0db-115">TSC\_PROXY\_CREDS\_MODE\_SMARTCARD (1)</span></span>
</dt> <dd>

<span data-ttu-id="cc0db-116">Utilisez une carte à puce comme méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc0db-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="cc0db-117">MODE d’identification TSC du \_ proxy \_ \_ \_ Any (4)</span><span class="sxs-lookup"><span data-stu-id="cc0db-117">TSC\_PROXY\_CREDS\_MODE\_ANY (4)</span></span>
</dt> <dd>

<span data-ttu-id="cc0db-118">Utilisez n’importe quelle méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cc0db-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="cc0db-119">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="cc0db-119">Error codes</span></span>

<span data-ttu-id="cc0db-120">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="cc0db-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc0db-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cc0db-121">Requirements</span></span>



| <span data-ttu-id="cc0db-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cc0db-122">Requirement</span></span> | <span data-ttu-id="cc0db-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="cc0db-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc0db-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc0db-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cc0db-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cc0db-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="cc0db-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cc0db-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cc0db-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cc0db-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="cc0db-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="cc0db-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="cc0db-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc0db-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cc0db-130">DLL</span><span class="sxs-lookup"><span data-stu-id="cc0db-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cc0db-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cc0db-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="cc0db-132">IID</span><span class="sxs-lookup"><span data-stu-id="cc0db-132">IID</span></span><br/>                      | <span data-ttu-id="cc0db-133">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="cc0db-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cc0db-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cc0db-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc0db-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="cc0db-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





