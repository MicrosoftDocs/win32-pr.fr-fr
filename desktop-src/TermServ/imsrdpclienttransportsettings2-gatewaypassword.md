---
title: IMsRdpClientTransportSettings2 propriété GatewayPassword
description: Spécifie le mot de passe qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).
ms.assetid: f29078e5-49ab-45a0-8d79-4b57d7c35e3a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayPassword
- Services Bureau à distance de la propriété GatewayPassword, interface IMsRdpClientTransportSettings2
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings2, propriété GatewayPassword
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings2.GatewayPassword
- IMsRdpClientTransportSettings2.put_GatewayPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d532f28023b7ff0eb3b8571e3875d0b63606535
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508381"
---
# <a name="imsrdpclienttransportsettings2gatewaypassword-property"></a><span data-ttu-id="4cb1e-106">IMsRdpClientTransportSettings2 :: GatewayPassword, propriété</span><span class="sxs-lookup"><span data-stu-id="4cb1e-106">IMsRdpClientTransportSettings2::GatewayPassword property</span></span>

<span data-ttu-id="4cb1e-107">Spécifie le mot de passe qu’un utilisateur fournit pour se connecter au serveur de passerelle Bureau à distance (passerelle des services Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="4cb1e-107">Specifies the password that a user provides to connect to the Remote Desktop Gateway (RD Gateway) server.</span></span>

<span data-ttu-id="4cb1e-108">Cette propriété est en écriture seule.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-108">This property is write-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cb1e-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4cb1e-109">Syntax</span></span>


```C++
HRESULT put_GatewayPassword(
  [in] BSTR proxyPassword
);
```



## <a name="property-value"></a><span data-ttu-id="4cb1e-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="4cb1e-110">Property value</span></span>

<span data-ttu-id="4cb1e-111">Mot de passe fourni par l’utilisateur pour se connecter au serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-111">The password that a user provides to connect to the RD Gateway server.</span></span>

## <a name="error-codes"></a><span data-ttu-id="4cb1e-112">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="4cb1e-112">Error codes</span></span>

<span data-ttu-id="4cb1e-113">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="4cb1e-113">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cb1e-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4cb1e-114">Requirements</span></span>



| <span data-ttu-id="4cb1e-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4cb1e-115">Requirement</span></span> | <span data-ttu-id="4cb1e-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="4cb1e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cb1e-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cb1e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4cb1e-118">Windows Vista avec SP1</span><span class="sxs-lookup"><span data-stu-id="4cb1e-118">Windows Vista with SP1</span></span><br/>                                                                 |
| <span data-ttu-id="4cb1e-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4cb1e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4cb1e-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4cb1e-120">Windows Server 2008</span></span><br/>                                                                    |
| <span data-ttu-id="4cb1e-121">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="4cb1e-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="4cb1e-122"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-122"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4cb1e-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4cb1e-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4cb1e-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4cb1e-124"><dt>MsTscAx.dll</dt></span></span> </dl>            |
| <span data-ttu-id="4cb1e-125">IID</span><span class="sxs-lookup"><span data-stu-id="4cb1e-125">IID</span></span><br/>                      | <span data-ttu-id="4cb1e-126">IID \_ IMsRdpClientTransportSettings2 est défini comme 67341688-D606-4C73-A5D2-2E0489009319</span><span class="sxs-lookup"><span data-stu-id="4cb1e-126">IID\_IMsRdpClientTransportSettings2 is defined as 67341688-D606-4c73-A5D2-2E0489009319</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cb1e-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4cb1e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cb1e-128">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="4cb1e-128">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> <dt>

[<span data-ttu-id="4cb1e-129">**IMsRdpClientTransportSettings2**</span><span class="sxs-lookup"><span data-stu-id="4cb1e-129">**IMsRdpClientTransportSettings2**</span></span>](imsrdpclienttransportsettings2.md)
</dt> </dl>

 

 





