---
title: Interface IMsRdpClientSecuredSettings
description: Comprend des méthodes pour récupérer et définir des propriétés du contrôle ActiveX Bureau à distance qui sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques. | Interface IMsRdpClientSecuredSettings
ms.assetid: 56d3193d-a0fb-468a-9fb3-c080db5500b7
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, Description
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 396e6b58b2be0122076b5529b910423377417fa6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/09/2021
ms.locfileid: "106523777"
---
# <a name="imsrdpclientsecuredsettings-interface"></a><span data-ttu-id="36211-106">Interface IMsRdpClientSecuredSettings</span><span class="sxs-lookup"><span data-stu-id="36211-106">IMsRdpClientSecuredSettings interface</span></span>

<span data-ttu-id="36211-107">Comprend des méthodes pour récupérer et définir des propriétés du contrôle ActiveX Bureau à distance qui sont limitées à des zones de sécurité d’URL Internet Explorer spécifiques.</span><span class="sxs-lookup"><span data-stu-id="36211-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span>

## <a name="members"></a><span data-ttu-id="36211-108">Membres</span><span class="sxs-lookup"><span data-stu-id="36211-108">Members</span></span>

<span data-ttu-id="36211-109">L’interface **IMsRdpClientSecuredSettings** hérite de [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="36211-109">The **IMsRdpClientSecuredSettings** interface inherits from [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span> <span data-ttu-id="36211-110">**IMsRdpClientSecuredSettings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="36211-110">**IMsRdpClientSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="36211-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36211-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="36211-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="36211-112">Properties</span></span>

<span data-ttu-id="36211-113">L’interface **IMsRdpClientSecuredSettings** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="36211-113">The **IMsRdpClientSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="36211-114">Propriété</span><span class="sxs-lookup"><span data-stu-id="36211-114">Property</span></span>                                                                                   | <span data-ttu-id="36211-115">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="36211-115">Access type</span></span>           | <span data-ttu-id="36211-116">Description</span><span class="sxs-lookup"><span data-stu-id="36211-116">Description</span></span>                                   |
|:-------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [<span data-ttu-id="36211-117">**AudioRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="36211-117">**AudioRedirectionMode**</span></span>](imsrdpclientsecuredsettings-autoredirectionmode.md)<br/> | <span data-ttu-id="36211-118">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36211-118">Read/write</span></span><br/> | <span data-ttu-id="36211-119">Paramètres de redirection audio.</span><span class="sxs-lookup"><span data-stu-id="36211-119">The audio redirection settings.</span></span><br/>    |
| [<span data-ttu-id="36211-120">**KeyboardHookMode**</span><span class="sxs-lookup"><span data-stu-id="36211-120">**KeyboardHookMode**</span></span>](imsrdpclientsecuredsettings-keyboardhookmode.md)<br/>        | <span data-ttu-id="36211-121">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="36211-121">Read/write</span></span><br/> | <span data-ttu-id="36211-122">Paramètres de redirection du clavier.</span><span class="sxs-lookup"><span data-stu-id="36211-122">The keyboard redirection settings.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="36211-123">Notes</span><span class="sxs-lookup"><span data-stu-id="36211-123">Remarks</span></span>

<span data-ttu-id="36211-124">Ces propriétés ne peuvent pas être définies lorsque le contrôle est connecté.</span><span class="sxs-lookup"><span data-stu-id="36211-124">These properties cannot be set when the control is connected.</span></span>

<span data-ttu-id="36211-125">Pour plus d’informations sur les méthodes de cette interface, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .</span><span class="sxs-lookup"><span data-stu-id="36211-125">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="36211-126">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="36211-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="36211-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36211-127">Requirements</span></span>



| <span data-ttu-id="36211-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36211-128">Requirement</span></span> | <span data-ttu-id="36211-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="36211-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36211-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36211-130">Minimum supported client</span></span><br/> | <span data-ttu-id="36211-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="36211-131">Windows Vista</span></span><br/>                                                                       |
| <span data-ttu-id="36211-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36211-132">Minimum supported server</span></span><br/> | <span data-ttu-id="36211-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="36211-133">Windows Server 2008</span></span><br/>                                                                 |
| <span data-ttu-id="36211-134">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="36211-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="36211-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36211-135"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="36211-136">DLL</span><span class="sxs-lookup"><span data-stu-id="36211-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36211-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="36211-137"><dt>MsTscAx.dll</dt></span></span> </dl>         |
| <span data-ttu-id="36211-138">IID</span><span class="sxs-lookup"><span data-stu-id="36211-138">IID</span></span><br/>                      | <span data-ttu-id="36211-139">IID \_ IMsRdpClientSecuredSettings est défini en tant que 605befcf-39c1-45cc-A811-068fb7be346d</span><span class="sxs-lookup"><span data-stu-id="36211-139">IID\_IMsRdpClientSecuredSettings is defined as 605befcf-39c1-45cc-a811-068fb7be346d</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="36211-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36211-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36211-141">**IMsTscSecuredSettings**</span><span class="sxs-lookup"><span data-stu-id="36211-141">**IMsTscSecuredSettings**</span></span>](imstscsecuredsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="36211-142">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="36211-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





