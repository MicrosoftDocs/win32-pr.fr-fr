---
title: Classe Win32_TSGatewayRADIUSServer
description: Décrit un serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS), qui dispose d’un ensemble de stratégies d’autorisation de connexion Services Bureau à distance (RD \ 160 ; Majuscules).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance
- Win32_TSGatewayRADIUSServer de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465087"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="4bde6-105">\_Classe TSGatewayRADIUSServer Win32</span><span class="sxs-lookup"><span data-stu-id="4bde6-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="4bde6-106">Décrit un serveur protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS), qui dispose d’un ensemble de stratégies d’autorisation de connexion Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4bde6-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="4bde6-107">RADIUS est un protocole standard utilisé pour transmettre les informations d’authentification, d’autorisation et de configuration entre un ordinateur serveur et un serveur d’authentification, appelé serveur RADIUS, avec une base de données qui stocke les informations utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4bde6-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="4bde6-108">Pour plus d’informations, consultez [protocole Radius](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="4bde6-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="4bde6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4bde6-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="4bde6-110">Membres</span><span class="sxs-lookup"><span data-stu-id="4bde6-110">Members</span></span>

<span data-ttu-id="4bde6-111">La classe **Win32 \_ TSGatewayRADIUSServer** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="4bde6-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="4bde6-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4bde6-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="4bde6-113">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4bde6-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="4bde6-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="4bde6-114">Methods</span></span>

<span data-ttu-id="4bde6-115">La classe **Win32 \_ TSGatewayRADIUSServer** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="4bde6-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="4bde6-116">Méthode</span><span class="sxs-lookup"><span data-stu-id="4bde6-116">Method</span></span>                                                                 | <span data-ttu-id="4bde6-117">Description</span><span class="sxs-lookup"><span data-stu-id="4bde6-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="4bde6-118">**Complémentaires**</span><span class="sxs-lookup"><span data-stu-id="4bde6-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="4bde6-119">Ajoute un nouveau serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="4bde6-120">**Descendre**</span><span class="sxs-lookup"><span data-stu-id="4bde6-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="4bde6-121">Déplace ce serveur RADIUS d’une position vers le dessous dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="4bde6-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="4bde6-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="4bde6-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="4bde6-123">Déplace ce serveur RADIUS d’une position vers le haut dans l’ordre de priorité.</span><span class="sxs-lookup"><span data-stu-id="4bde6-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="4bde6-124">**Installez**</span><span class="sxs-lookup"><span data-stu-id="4bde6-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="4bde6-125">Supprime le serveur RADIUS actuel.</span><span class="sxs-lookup"><span data-stu-id="4bde6-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="4bde6-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="4bde6-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="4bde6-127">Définit la propriété de **nom** pour ce serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="4bde6-128">**SetSharedSecret**</span><span class="sxs-lookup"><span data-stu-id="4bde6-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="4bde6-129">Définit la **propriété de serveur** à la une pour ce serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="4bde6-130">**Mise à jour**</span><span class="sxs-lookup"><span data-stu-id="4bde6-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="4bde6-131">Met à jour le serveur RADIUS actuel.</span><span class="sxs-lookup"><span data-stu-id="4bde6-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="4bde6-132">Propriétés</span><span class="sxs-lookup"><span data-stu-id="4bde6-132">Properties</span></span>

<span data-ttu-id="4bde6-133">La classe **Win32 \_ TSGatewayRADIUSServer** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="4bde6-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4bde6-134">**Nom**</span><span class="sxs-lookup"><span data-stu-id="4bde6-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bde6-135">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bde6-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bde6-136">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bde6-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4bde6-137">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4bde6-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4bde6-138">Nom du serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-138">Name of the RADIUS server.</span></span> <span data-ttu-id="4bde6-139">Cette propriété peut être modifiée à l’aide de la méthode [**SetName**](setname-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="4bde6-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="4bde6-140">**Priorité**</span><span class="sxs-lookup"><span data-stu-id="4bde6-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bde6-141">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="4bde6-142">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bde6-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bde6-143">Priorité du serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="4bde6-144">Le serveur de passerelle Bureau à distance recherche les Cap des services Bureau à distance sur les serveurs RADIUS en fonction de la priorité.</span><span class="sxs-lookup"><span data-stu-id="4bde6-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="4bde6-145">Cette propriété peut être modifiée avec les méthodes [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)et [**Remove**](win32-tsgatewayradiusserver-remove.md) .</span><span class="sxs-lookup"><span data-stu-id="4bde6-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="4bde6-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="4bde6-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4bde6-147">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="4bde6-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4bde6-148">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="4bde6-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="4bde6-149">Secret partagé pour le serveur RADIUS.</span><span class="sxs-lookup"><span data-stu-id="4bde6-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="4bde6-150">Cette propriété peut être modifiée à l’aide de la méthode [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) .</span><span class="sxs-lookup"><span data-stu-id="4bde6-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4bde6-151">Notes</span><span class="sxs-lookup"><span data-stu-id="4bde6-151">Remarks</span></span>

<span data-ttu-id="4bde6-152">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="4bde6-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="4bde6-153">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="4bde6-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="4bde6-154">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="4bde6-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="4bde6-155">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="4bde6-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="4bde6-156">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="4bde6-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bde6-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4bde6-157">Requirements</span></span>



| <span data-ttu-id="4bde6-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4bde6-158">Requirement</span></span> | <span data-ttu-id="4bde6-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="4bde6-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bde6-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bde6-160">Minimum supported client</span></span><br/> | <span data-ttu-id="4bde6-161">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bde6-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="4bde6-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4bde6-162">Minimum supported server</span></span><br/> | <span data-ttu-id="4bde6-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4bde6-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="4bde6-164">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="4bde6-164">Namespace</span></span><br/>                | <span data-ttu-id="4bde6-165">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="4bde6-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="4bde6-166">MOF</span><span class="sxs-lookup"><span data-stu-id="4bde6-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bde6-167"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4bde6-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bde6-168">DLL</span><span class="sxs-lookup"><span data-stu-id="4bde6-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bde6-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bde6-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="4bde6-170">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4bde6-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bde6-171">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="4bde6-172">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="4bde6-173">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="4bde6-174">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="4bde6-175">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="4bde6-176">**\_TSGatewayServerSettings Win32**</span><span class="sxs-lookup"><span data-stu-id="4bde6-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

