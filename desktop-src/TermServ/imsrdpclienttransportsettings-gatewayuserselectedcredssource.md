---
title: IMsRdpClientTransportSettings propriété GatewayUserSelectedCredsSource
description: Définit ou récupère la source des informations d’identification spécifiées par l’utilisateur Bureau à distance passerelle des services Bureau à distance.
ms.assetid: 0c12ddf6-52c2-40a2-af2b-effd4e8bbdb6
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayUserSelectedCredsSource
- Services Bureau à distance de la propriété GatewayUserSelectedCredsSource, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayUserSelectedCredsSource
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.get_GatewayUserSelectedCredsSource
- IMsRdpClientTransportSettings.put_GatewayUserSelectedCredsSource
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1556088e62221df7ff91b4b0069bb1ec938ebf23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508382"
---
# <a name="imsrdpclienttransportsettingsgatewayuserselectedcredssource-property"></a><span data-ttu-id="b772c-106">IMsRdpClientTransportSettings :: GatewayUserSelectedCredsSource, propriété</span><span class="sxs-lookup"><span data-stu-id="b772c-106">IMsRdpClientTransportSettings::GatewayUserSelectedCredsSource property</span></span>

<span data-ttu-id="b772c-107">Définit ou récupère la source des informations d’identification spécifiées par l’utilisateur Bureau à distance passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b772c-107">Sets or retrieves the user-specified Remote Desktop Gateway (RD Gateway) credential source.</span></span>

<span data-ttu-id="b772c-108">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="b772c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b772c-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b772c-109">Syntax</span></span>


```C++
HRESULT put_GatewayUserSelectedCredsSource(
  [in]  ULONG ulProxyCredsSource
);

HRESULT get_GatewayUserSelectedCredsSource(
  [out] ULONG *pulProxyCredsSource
);
```



## <a name="property-value"></a><span data-ttu-id="b772c-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="b772c-110">Property value</span></span>

<span data-ttu-id="b772c-111">Variable **ULong** qui spécifie la méthode d’authentification de la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b772c-111">A **ULONG** variable that specifies the RD Gateway authentication method.</span></span> <span data-ttu-id="b772c-112">Ce paramètre peut prendre les valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="b772c-112">This parameter can be one of the following values.</span></span>

<dt>

<span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>

<span data-ttu-id="b772c-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC \_ MODE d’identification du PROXY \_ \_ \_ USERPASS** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="b772c-113"><span id="TSC_PROXY_CREDS_MODE_USERPASS"></span><span id="tsc_proxy_creds_mode_userpass"></span>**TSC\_PROXY\_CREDS\_MODE\_USERPASS** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="b772c-114">Utilisez un mot de passe (NTLM) comme méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b772c-114">Use a password (NTLM) as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>

<span data-ttu-id="b772c-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC \_ \_ \_ \_ Carte à puce mode** d’identification du proxy (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="b772c-115"><span id="TSC_PROXY_CREDS_MODE_SMARTCARD"></span><span id="tsc_proxy_creds_mode_smartcard"></span>**TSC\_PROXY\_CREDS\_MODE\_SMARTCARD** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="b772c-116">Utilisez une carte à puce comme méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b772c-116">Use a smart card as the authentication method for RD Gateway.</span></span>

</dd> <dt>

<span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>

<span data-ttu-id="b772c-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC \_ \_ \_ Mode \_ d’identification du proxy any** (4 (0x4))</span><span class="sxs-lookup"><span data-stu-id="b772c-117"><span id="TSC_PROXY_CREDS_MODE_ANY"></span><span id="tsc_proxy_creds_mode_any"></span>**TSC\_PROXY\_CREDS\_MODE\_ANY** (4 (0x4))</span></span>


</dt> <dd>

<span data-ttu-id="b772c-118">Utilisez n’importe quelle méthode d’authentification pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="b772c-118">Use any authentication method for RD Gateway.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="b772c-119">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="b772c-119">Error codes</span></span>

<span data-ttu-id="b772c-120">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="b772c-120">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="b772c-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b772c-121">Requirements</span></span>



| <span data-ttu-id="b772c-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b772c-122">Requirement</span></span> | <span data-ttu-id="b772c-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b772c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b772c-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b772c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b772c-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b772c-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="b772c-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b772c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b772c-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b772c-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="b772c-128">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="b772c-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="b772c-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b772c-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b772c-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b772c-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b772c-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b772c-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="b772c-132">IID</span><span class="sxs-lookup"><span data-stu-id="b772c-132">IID</span></span><br/>                      | <span data-ttu-id="b772c-133">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="b772c-133">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b772c-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b772c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b772c-135">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="b772c-135">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





