---
title: Interface IMsRdpClientAdvancedSettings3
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings2.
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings3, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741348"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="8df0d-106">Interface IMsRdpClientAdvancedSettings3</span><span class="sxs-lookup"><span data-stu-id="8df0d-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="8df0d-107">Gère les paramètres client avancés.</span><span class="sxs-lookup"><span data-stu-id="8df0d-107">Manages advanced client settings.</span></span> <span data-ttu-id="8df0d-108">Dérive de l’interface [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) .</span><span class="sxs-lookup"><span data-stu-id="8df0d-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="8df0d-109">Cette interface comprend des méthodes pour récupérer et définir des propriétés avancées (facultatives) pour le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8df0d-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="8df0d-110">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="8df0d-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="8df0d-111">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings3** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="8df0d-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="8df0d-112">Membres</span><span class="sxs-lookup"><span data-stu-id="8df0d-112">Members</span></span>

<span data-ttu-id="8df0d-113">L’interface **IMsRdpClientAdvancedSettings3** hérite de [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span><span class="sxs-lookup"><span data-stu-id="8df0d-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="8df0d-114">**IMsRdpClientAdvancedSettings3** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="8df0d-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="8df0d-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8df0d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="8df0d-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="8df0d-116">Properties</span></span>

<span data-ttu-id="8df0d-117">L’interface **IMsRdpClientAdvancedSettings3** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="8df0d-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="8df0d-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="8df0d-118">Property</span></span>                                                                                                            | <span data-ttu-id="8df0d-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="8df0d-119">Access type</span></span>           | <span data-ttu-id="8df0d-120">Description</span><span class="sxs-lookup"><span data-stu-id="8df0d-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="8df0d-121">**ConnectionBarShowMinimizeButton**</span><span class="sxs-lookup"><span data-stu-id="8df0d-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="8df0d-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8df0d-122">Read/write</span></span><br/> | <span data-ttu-id="8df0d-123">Spécifie s’il faut afficher le bouton **réduire** sur la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="8df0d-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="8df0d-124">**ConnectionBarShowRestoreButton**</span><span class="sxs-lookup"><span data-stu-id="8df0d-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="8df0d-125">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="8df0d-125">Read/write</span></span><br/> | <span data-ttu-id="8df0d-126">Spécifie s’il faut afficher le bouton **restaurer** sur la barre de connexion.</span><span class="sxs-lookup"><span data-stu-id="8df0d-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="8df0d-127">Notes</span><span class="sxs-lookup"><span data-stu-id="8df0d-127">Remarks</span></span>

<span data-ttu-id="8df0d-128">Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :</span><span class="sxs-lookup"><span data-stu-id="8df0d-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="8df0d-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="8df0d-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="8df0d-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="8df0d-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="8df0d-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="8df0d-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="8df0d-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="8df0d-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="8df0d-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="8df0d-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="8df0d-134">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="8df0d-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8df0d-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8df0d-135">Requirements</span></span>



| <span data-ttu-id="8df0d-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8df0d-136">Requirement</span></span> | <span data-ttu-id="8df0d-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="8df0d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df0d-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df0d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="8df0d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8df0d-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="8df0d-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8df0d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="8df0d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8df0d-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="8df0d-142">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="8df0d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="8df0d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df0d-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8df0d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="8df0d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df0d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8df0d-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="8df0d-146">IID</span><span class="sxs-lookup"><span data-stu-id="8df0d-146">IID</span></span><br/>                      | <span data-ttu-id="8df0d-147">IID \_ IMsRdpClientAdvancedSettings3 est défini en tant que 19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="8df0d-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8df0d-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8df0d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df0d-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="8df0d-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="8df0d-150">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8df0d-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8df0d-151">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="8df0d-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="8df0d-152">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="8df0d-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

