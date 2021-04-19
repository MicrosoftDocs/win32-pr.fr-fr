---
title: Interface IMsRdpClientAdvancedSettings6
description: Expose les propriétés qui gèrent les paramètres de contrôle ActiveX avancés.
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6
- Services Bureau à distance de l’interface IMsRdpClientAdvancedSettings6, Description
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513798"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="50e36-105">Interface IMsRdpClientAdvancedSettings6</span><span class="sxs-lookup"><span data-stu-id="50e36-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="50e36-106">Expose les propriétés qui gèrent les paramètres de contrôle ActiveX avancés.</span><span class="sxs-lookup"><span data-stu-id="50e36-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="50e36-107">L’interface **IMsRdpClientAdvancedSettings6** est dérivée de l’interface [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) .</span><span class="sxs-lookup"><span data-stu-id="50e36-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="50e36-108">Pour obtenir une instance de cette interface, utilisez la propriété [**IMsTscAx :: AdvancedSettings**](imstscax-advancedsettings.md) pour obtenir un pointeur d’interface [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="50e36-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="50e36-109">Appelez ensuite [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur le pointeur **IMsTscAdvancedSettings** et transmettez **IID \_ IMsRdpClientAdvancedSettings6** à **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="50e36-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="50e36-110">Membres</span><span class="sxs-lookup"><span data-stu-id="50e36-110">Members</span></span>

<span data-ttu-id="50e36-111">L’interface **IMsRdpClientAdvancedSettings6** hérite de [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span><span class="sxs-lookup"><span data-stu-id="50e36-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="50e36-112">**IMsRdpClientAdvancedSettings6** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="50e36-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="50e36-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50e36-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="50e36-114">Propriétés</span><span class="sxs-lookup"><span data-stu-id="50e36-114">Properties</span></span>

<span data-ttu-id="50e36-115">L’interface **IMsRdpClientAdvancedSettings6** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="50e36-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="50e36-116">Propriété</span><span class="sxs-lookup"><span data-stu-id="50e36-116">Property</span></span>                                                                                                  | <span data-ttu-id="50e36-117">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="50e36-117">Access type</span></span>           | <span data-ttu-id="50e36-118">Description</span><span class="sxs-lookup"><span data-stu-id="50e36-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50e36-119">**AuthenticationServiceClass**</span><span class="sxs-lookup"><span data-stu-id="50e36-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="50e36-120">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-120">Read/write</span></span><br/> | <span data-ttu-id="50e36-121">Spécifie le nom de principal du service (SPN) à utiliser pour l’authentification auprès du serveur.</span><span class="sxs-lookup"><span data-stu-id="50e36-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="50e36-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="50e36-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="50e36-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="50e36-123">Read-only</span></span><br/>  | <span data-ttu-id="50e36-124">Spécifie le type d’authentification utilisé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="50e36-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="50e36-125">**ConnectToAdministerServer**</span><span class="sxs-lookup"><span data-stu-id="50e36-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="50e36-126">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-126">Read/write</span></span><br/> | <span data-ttu-id="50e36-127">Récupère ou spécifie si le contrôle ActiveX doit tenter de se connecter au serveur à des fins d’administration.</span><span class="sxs-lookup"><span data-stu-id="50e36-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="50e36-128">**EnableCredSspSupport**</span><span class="sxs-lookup"><span data-stu-id="50e36-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="50e36-129">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-129">Read/write</span></span><br/> | <span data-ttu-id="50e36-130">Spécifie si le fournisseur de services de sécurité des informations d’identification (CredSSP) est activé pour cette connexion.</span><span class="sxs-lookup"><span data-stu-id="50e36-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="50e36-131">**HotKeyFocusReleaseLeft**</span><span class="sxs-lookup"><span data-stu-id="50e36-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="50e36-132">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-132">Read/write</span></span><br/> | <span data-ttu-id="50e36-133">Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + gauche.</span><span class="sxs-lookup"><span data-stu-id="50e36-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="50e36-134">**HotKeyFocusReleaseRight**</span><span class="sxs-lookup"><span data-stu-id="50e36-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="50e36-135">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-135">Read/write</span></span><br/> | <span data-ttu-id="50e36-136">Spécifie le code de la touche virtuelle à ajouter à CTRL + ALT pour déterminer le remplacement des raccourcis clavier pour CTRL + ALT + droite.</span><span class="sxs-lookup"><span data-stu-id="50e36-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="50e36-137">**PCB**</span><span class="sxs-lookup"><span data-stu-id="50e36-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="50e36-138">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-138">Read/write</span></span><br/> | <span data-ttu-id="50e36-139">Spécifie le paramètre d’objet BLOB de préconnexion à utiliser avant la connexion pour la transmission au serveur.</span><span class="sxs-lookup"><span data-stu-id="50e36-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="50e36-140">**RelativeMouseMode**</span><span class="sxs-lookup"><span data-stu-id="50e36-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="50e36-141">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="50e36-141">Read/write</span></span><br/> | <span data-ttu-id="50e36-142">Spécifie si la souris doit utiliser le mode relatif.</span><span class="sxs-lookup"><span data-stu-id="50e36-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="50e36-143">Notes</span><span class="sxs-lookup"><span data-stu-id="50e36-143">Remarks</span></span>

<span data-ttu-id="50e36-144">Cette interface a été étendue par l’interface [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) , qui hérite de toutes les méthodes et propriétés des interfaces précédentes.</span><span class="sxs-lookup"><span data-stu-id="50e36-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="50e36-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="50e36-145">Requirements</span></span>



| <span data-ttu-id="50e36-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="50e36-146">Requirement</span></span> | <span data-ttu-id="50e36-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="50e36-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="50e36-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50e36-148">Minimum supported client</span></span><br/> | <span data-ttu-id="50e36-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="50e36-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="50e36-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="50e36-150">Minimum supported server</span></span><br/> | <span data-ttu-id="50e36-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="50e36-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="50e36-152">Bibliothèque de types</span><span class="sxs-lookup"><span data-stu-id="50e36-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="50e36-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e36-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="50e36-154">DLL</span><span class="sxs-lookup"><span data-stu-id="50e36-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="50e36-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="50e36-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="50e36-156">IID</span><span class="sxs-lookup"><span data-stu-id="50e36-156">IID</span></span><br/>                      | <span data-ttu-id="50e36-157">IID \_ IMsRdpClientAdvancedSettings6 est défini en tant que 222c4b5d-45d9-4DF0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="50e36-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="50e36-158">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="50e36-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50e36-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="50e36-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="50e36-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="50e36-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="50e36-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="50e36-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="50e36-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="50e36-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="50e36-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="50e36-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="50e36-164">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="50e36-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

