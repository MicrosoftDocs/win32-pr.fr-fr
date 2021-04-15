---
title: Interface IMsRdpClientAdvancedSettings4
description: Gère les paramètres client avancés. Dérive de l’interface IMsRdpClientAdvancedSettings3.
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings4, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384588"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="77cff-106">Interface IMsRdpClientAdvancedSettings4</span><span class="sxs-lookup"><span data-stu-id="77cff-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="77cff-107">Gère les paramètres client avancés.</span><span class="sxs-lookup"><span data-stu-id="77cff-107">Manages advanced client settings.</span></span> <span data-ttu-id="77cff-108">Dérive de l’interface [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) .</span><span class="sxs-lookup"><span data-stu-id="77cff-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="77cff-109">Cette interface comprend des méthodes pour récupérer et définir des propriétés avancées (facultatives) pour le contrôle ActiveX Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="77cff-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="77cff-110">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="77cff-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="77cff-111">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings4** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="77cff-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="77cff-112">Membres</span><span class="sxs-lookup"><span data-stu-id="77cff-112">Members</span></span>

<span data-ttu-id="77cff-113">L’interface **IMsRdpClientAdvancedSettings4** hérite de [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span><span class="sxs-lookup"><span data-stu-id="77cff-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="77cff-114">**IMsRdpClientAdvancedSettings4** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="77cff-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="77cff-115">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77cff-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="77cff-116">Propriétés</span><span class="sxs-lookup"><span data-stu-id="77cff-116">Properties</span></span>

<span data-ttu-id="77cff-117">L’interface **IMsRdpClientAdvancedSettings4** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="77cff-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="77cff-118">Propriété</span><span class="sxs-lookup"><span data-stu-id="77cff-118">Property</span></span>                                                                                    | <span data-ttu-id="77cff-119">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="77cff-119">Access type</span></span>           | <span data-ttu-id="77cff-120">Description</span><span class="sxs-lookup"><span data-stu-id="77cff-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="77cff-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="77cff-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="77cff-122">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="77cff-122">Read/write</span></span><br/> | <span data-ttu-id="77cff-123">Spécifie le niveau d’authentification à utiliser pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="77cff-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="77cff-124">Notes</span><span class="sxs-lookup"><span data-stu-id="77cff-124">Remarks</span></span>

<span data-ttu-id="77cff-125">Cette interface a été étendue par les interfaces suivantes, chaque nouvelle interface héritant de toutes les méthodes et propriétés des interfaces précédentes :</span><span class="sxs-lookup"><span data-stu-id="77cff-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="77cff-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="77cff-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="77cff-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="77cff-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="77cff-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="77cff-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="77cff-129">Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="77cff-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77cff-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="77cff-130">Requirements</span></span>



| <span data-ttu-id="77cff-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="77cff-131">Requirement</span></span> | <span data-ttu-id="77cff-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="77cff-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77cff-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cff-133">Minimum supported client</span></span><br/> | <span data-ttu-id="77cff-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77cff-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="77cff-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="77cff-135">Minimum supported server</span></span><br/> | <span data-ttu-id="77cff-136">Windows Server 2008, Windows Server 2008 avec SP1</span><span class="sxs-lookup"><span data-stu-id="77cff-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="77cff-137">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="77cff-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="77cff-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77cff-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77cff-139">DLL</span><span class="sxs-lookup"><span data-stu-id="77cff-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77cff-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77cff-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77cff-141">IID</span><span class="sxs-lookup"><span data-stu-id="77cff-141">IID</span></span><br/>                      | <span data-ttu-id="77cff-142">IID \_ IMsRdpClientAdvancedSettings4 est défini en tant que FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="77cff-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77cff-143">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="77cff-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77cff-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="77cff-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="77cff-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="77cff-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="77cff-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="77cff-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="77cff-147">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="77cff-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="77cff-148">Référence Connexion Bureau à distance par le Web</span><span class="sxs-lookup"><span data-stu-id="77cff-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

