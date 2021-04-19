---
title: IMsRdpClientTransportSettings propriété GatewayDefaultUsageMethod
description: Méthode d’utilisation par défaut pour la passerelle des services Bureau à Bureau à distance.
ms.assetid: 7014538d-550a-4246-ad32-406ef67fb112
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété GatewayDefaultUsageMethod
- Services Bureau à distance de la propriété GatewayDefaultUsageMethod, interface IMsRdpClientTransportSettings
- Services Bureau à distance de l’interface IMsRdpClientTransportSettings, propriété GatewayDefaultUsageMethod
topic_type:
- apiref
api_name:
- IMsRdpClientTransportSettings.GatewayDefaultUsageMethod
- IMsRdpClientTransportSettings.get_GatewayDefaultUsageMethod
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8417da30f9a692e6e233174a33f4b03682a5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513766"
---
# <a name="imsrdpclienttransportsettingsgatewaydefaultusagemethod-property"></a><span data-ttu-id="92560-106">IMsRdpClientTransportSettings :: GatewayDefaultUsageMethod, propriété</span><span class="sxs-lookup"><span data-stu-id="92560-106">IMsRdpClientTransportSettings::GatewayDefaultUsageMethod property</span></span>

<span data-ttu-id="92560-107">Méthode d’utilisation par défaut pour la passerelle des services Bureau à Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="92560-107">The default usage method for Remote Desktop Gateway (RD Gateway).</span></span>

<span data-ttu-id="92560-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="92560-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="92560-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92560-109">Syntax</span></span>


```C++
HRESULT get_GatewayDefaultUsageMethod(
  [out] ULONG *pulProxyDefaultUsageMethod
);
```



## <a name="property-value"></a><span data-ttu-id="92560-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="92560-110">Property value</span></span>

<span data-ttu-id="92560-111">Pointeur vers la méthode d’utilisation par défaut pour la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="92560-111">A pointer to the default usage method for RD Gateway.</span></span> <span data-ttu-id="92560-112">Retourne une Union des paramètres utilisateur définis par [**put \_ GatewayUsageMethod ()**](imsrdpclienttransportsettings-gatewayusagemethod.md)et des paramètres de stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="92560-112">Returns a union of the user settings that are set by [**put\_GatewayUsageMethod()**](imsrdpclienttransportsettings-gatewayusagemethod.md), and group policy settings.</span></span> <span data-ttu-id="92560-113">Si aucun paramètre utilisateur n’a été défini par **put \_ GatewayUsageMethod ()**, **\_ GatewayDefaultUsageMethod ()** retourne la valeur par défaut de la **\_ \_ \_ détection du mode proxy TSC**.</span><span class="sxs-lookup"><span data-stu-id="92560-113">If no user settings were set by **put\_GatewayUsageMethod()**, **get\_GatewayDefaultUsageMethod()** will return the default value of **TSC\_PROXY\_MODE\_DETECT**.</span></span>

## <a name="error-codes"></a><span data-ttu-id="92560-114">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="92560-114">Error codes</span></span>

<span data-ttu-id="92560-115">Retourne **S \_ OK** en cas de réussite.</span><span class="sxs-lookup"><span data-stu-id="92560-115">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="92560-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92560-116">Requirements</span></span>



| <span data-ttu-id="92560-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92560-117">Requirement</span></span> | <span data-ttu-id="92560-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="92560-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92560-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92560-119">Minimum supported client</span></span><br/> | <span data-ttu-id="92560-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="92560-120">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="92560-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="92560-121">Minimum supported server</span></span><br/> | <span data-ttu-id="92560-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="92560-122">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="92560-123">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="92560-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="92560-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92560-124"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="92560-125">DLL</span><span class="sxs-lookup"><span data-stu-id="92560-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92560-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92560-126"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="92560-127">IID</span><span class="sxs-lookup"><span data-stu-id="92560-127">IID</span></span><br/>                      | <span data-ttu-id="92560-128">IID \_ IMsRdpClientTransportSettings est défini en tant que 720298C0-A099-46f5-9F82-96921BAE4701</span><span class="sxs-lookup"><span data-stu-id="92560-128">IID\_IMsRdpClientTransportSettings is defined as 720298C0-A099-46f5-9F82-96921BAE4701</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92560-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92560-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92560-130">**IMsRdpClientTransportSettings**</span><span class="sxs-lookup"><span data-stu-id="92560-130">**IMsRdpClientTransportSettings**</span></span>](imsrdpclienttransportsettings.md)
</dt> </dl>

 

 





