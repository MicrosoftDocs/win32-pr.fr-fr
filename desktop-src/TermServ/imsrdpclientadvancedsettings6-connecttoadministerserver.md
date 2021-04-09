---
title: IMsRdpClientAdvancedSettings6 propriété ConnectToAdministerServer
description: Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.
ms.assetid: b98f9b9b-a3e7-4a3c-a7e3-e388ce53c5c9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings7
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings7, propriété ConnectToAdministerServer
- Services Bureau à distance de la propriété ConnectToAdministerServer, interface IMsRdpClientAdvancedSettings8
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings8, propriété ConnectToAdministerServer
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings6.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings7.put_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.get_ConnectToAdministerServer
- IMsRdpClientAdvancedSettings8.put_ConnectToAdministerServer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9cad8d50e2e0a4c1ec18fbd33733dc394101a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032866"
---
# <a name="imsrdpclientadvancedsettings6connecttoadministerserver-property"></a><span data-ttu-id="32382-110">IMsRdpClientAdvancedSettings6 :: ConnectToAdministerServer, propriété</span><span class="sxs-lookup"><span data-stu-id="32382-110">IMsRdpClientAdvancedSettings6::ConnectToAdministerServer property</span></span>

<span data-ttu-id="32382-111">Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.</span><span class="sxs-lookup"><span data-stu-id="32382-111">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span>

<span data-ttu-id="32382-112">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="32382-112">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="32382-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="32382-113">Syntax</span></span>


```C++
HRESULT put_ConnectToAdministerServer(
  [in]  VARIANT_BOOL connectToAdministerServer
);

HRESULT get_ConnectToAdministerServer(
  [out] VARIANT_BOOL *pConnectToAdministerServer
);
```



## <a name="property-value"></a><span data-ttu-id="32382-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="32382-114">Property value</span></span>

<span data-ttu-id="32382-115">**Variante \_ TRUE** pour obliger le contrôle ActiveX à tenter de se connecter au serveur à des fins d’administration. Sinon, **Variant \_ false**.</span><span class="sxs-lookup"><span data-stu-id="32382-115">**VARIANT\_TRUE** to cause the ActiveX control to attempt to connect to the server for administrative purposes; otherwise **VARIANT\_FALSE**.</span></span> <span data-ttu-id="32382-116">La valeur par défaut **est \_ false**.</span><span class="sxs-lookup"><span data-stu-id="32382-116">The default value is **VARIANT\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="32382-117">Notes</span><span class="sxs-lookup"><span data-stu-id="32382-117">Remarks</span></span>

<span data-ttu-id="32382-118">Pour utiliser **ConnectToAdministerServer**, vous devez exécuter le client Connexion Bureau À distance (RDC) version 6,1 ou ultérieure.</span><span class="sxs-lookup"><span data-stu-id="32382-118">To use **ConnectToAdministerServer**, you must be running Remote Desktop Connection (RDC) client version 6.1 or later.</span></span>

> [!Note]  
> <span data-ttu-id="32382-119">RDC version 6,1 (6.0.6001) prend en charge protocole RDP (Remote Desktop Protocol) 6,1.</span><span class="sxs-lookup"><span data-stu-id="32382-119">RDC version 6.1 (6.0.6001) supports Remote Desktop Protocol 6.1.</span></span> <span data-ttu-id="32382-120">RDC 6,1 est inclus avec Windows Server 2008 et Windows Vista avec Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="32382-120">RDC 6.1 is included with Windows Server 2008 and Windows Vista with Service Pack 1 (SP1).</span></span>

 

<span data-ttu-id="32382-121">**ConnectToAdministerServer** vous connecte à une session utilisée à des fins administratives sur le serveur distant.</span><span class="sxs-lookup"><span data-stu-id="32382-121">**ConnectToAdministerServer** connects you to a session that is used for administrative purposes on the remote server.</span></span> <span data-ttu-id="32382-122">Si le service de rôle hôte de session Bureau à distance (hôte de session Bureau à distance) est installé sur le serveur distant, **ConnectToAdministerServer** effectue les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="32382-122">If the Remote Desktop Session Host (RD Session Host) role service is installed on the remote server, **ConnectToAdministerServer** does the following:</span></span>

-   <span data-ttu-id="32382-123">Désactive Services Bureau à distance licence d’accès client pour la session.</span><span class="sxs-lookup"><span data-stu-id="32382-123">Disables Remote Desktop Services client access licensing for the session.</span></span>
-   <span data-ttu-id="32382-124">Désactive la redirection de fuseau horaire pour la session.</span><span class="sxs-lookup"><span data-stu-id="32382-124">Disables time zone redirection for the session.</span></span>
-   <span data-ttu-id="32382-125">Désactive Connexion Bureau à distance redirection du Service Broker pour les connexions Bureau à distance pour la session.</span><span class="sxs-lookup"><span data-stu-id="32382-125">Disables Remote Desktop Connection Broker (RD Connection Broker) redirection for the session.</span></span>
-   <span data-ttu-id="32382-126">Désactive Plug-and-Play redirection de périphérique pour la session.</span><span class="sxs-lookup"><span data-stu-id="32382-126">Disables Plug and Play device redirection for the session.</span></span>
-   <span data-ttu-id="32382-127">Modifie le thème de session à distance en Windows Classic pour la session.</span><span class="sxs-lookup"><span data-stu-id="32382-127">Changes the remote session theme to Windows Classic for the session.</span></span>

## <a name="requirements"></a><span data-ttu-id="32382-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="32382-128">Requirements</span></span>



| <span data-ttu-id="32382-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="32382-129">Requirement</span></span> | <span data-ttu-id="32382-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="32382-130">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32382-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32382-131">Minimum supported client</span></span><br/> | <span data-ttu-id="32382-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32382-132">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="32382-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="32382-133">Minimum supported server</span></span><br/> | <span data-ttu-id="32382-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32382-134">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="32382-135">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="32382-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="32382-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32382-136"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="32382-137">DLL</span><span class="sxs-lookup"><span data-stu-id="32382-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32382-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32382-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="32382-139">IID</span><span class="sxs-lookup"><span data-stu-id="32382-139">IID</span></span><br/>                      | <span data-ttu-id="32382-140">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="32382-140">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="32382-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="32382-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32382-142">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="32382-142">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="32382-143">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="32382-143">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="32382-144">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="32382-144">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> </dl>

 

 





