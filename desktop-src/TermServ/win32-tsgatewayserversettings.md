---
title: Classe Win32_TSGatewayServerSettings
description: Fournit des méthodes et des propriétés permettant d’afficher et de configurer les paramètres du serveur de passerelle Bureau à distance (passerelle Bureau à distance).
ms.assetid: f772bf71-68ef-4345-8123-f6ad50ee4d61
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance
- Win32_TSGatewayServerSettings de la classe Services Bureau à distance, Description
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings
- Win32_TSGatewayServerSettings.MaxConnections
- Win32_TSGatewayServerSettings.UnlimitedConnections
- Win32_TSGatewayServerSettings.MaximumAllowedConnectionsBySku
- Win32_TSGatewayServerSettings.SkuName
- Win32_TSGatewayServerSettings.MaxProtocols
- Win32_TSGatewayServerSettings.MaxLogEvents
- Win32_TSGatewayServerSettings.adminMessageText
- Win32_TSGatewayServerSettings.adminMessageStartTime
- Win32_TSGatewayServerSettings.adminMessageEndTime
- Win32_TSGatewayServerSettings.consentMessageText
- Win32_TSGatewayServerSettings.OnlyConsentCapableClients
- Win32_TSGatewayServerSettings.CentralCAPEnabled
- Win32_TSGatewayServerSettings.RequestSOH
- Win32_TSGatewayServerSettings.AuthenticationPluginName
- Win32_TSGatewayServerSettings.AuthenticationPluginCLSID
- Win32_TSGatewayServerSettings.AuthenticationPluginDescription
- Win32_TSGatewayServerSettings.AuthorizationPluginName
- Win32_TSGatewayServerSettings.AuthorizationPluginCLSID
- Win32_TSGatewayServerSettings.AuthorizationPluginDescription
- Win32_TSGatewayServerSettings.SslBridging
- Win32_TSGatewayServerSettings.IsConfigured
- Win32_TSGatewayServerSettings.CertHash
- Win32_TSGatewayServerSettings.EnforceChannelBinding
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c0fb9b93f75c47760da8778e4aef8bed7f4e022
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466706"
---
# <a name="win32_tsgatewayserversettings-class"></a><span data-ttu-id="ed4f6-105">\_Classe TSGatewayServerSettings Win32</span><span class="sxs-lookup"><span data-stu-id="ed4f6-105">Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="ed4f6-106">Fournit des méthodes et des propriétés permettant d’afficher et de configurer les paramètres du serveur de passerelle Bureau à distance (passerelle Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="ed4f6-106">Provides methods and properties to view and configure Remote Desktop Gateway (RD Gateway) server settings.</span></span> <span data-ttu-id="ed4f6-107">Un administrateur peut utiliser cette classe pour configurer un ensemble de protocoles, l’ensemble des événements qui seront écrits dans le journal des événements et le nombre maximal de connexions via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-107">An administrator can use this class to configure a set of protocols, the set of events that will be written to the event log, and the maximum number of connections through RD Gateway.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed4f6-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ed4f6-108">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServerSettings
{
  uint32  MaxConnections;
  boolean UnlimitedConnections;
  uint32  MaximumAllowedConnectionsBySku;
  string  SkuName;
  uint32  MaxProtocols;
  uint32  MaxLogEvents;
  string  adminMessageText;
  string  adminMessageStartTime;
  string  adminMessageEndTime;
  string  consentMessageText;
  boolean OnlyConsentCapableClients;
  boolean CentralCAPEnabled;
  boolean RequestSOH;
  string  AuthenticationPluginName;
  string  AuthenticationPluginCLSID;
  string  AuthenticationPluginDescription;
  string  AuthorizationPluginName;
  string  AuthorizationPluginCLSID;
  string  AuthorizationPluginDescription;
  uint32  SslBridging;
  boolean IsConfigured;
  uint8   CertHash[];
  boolean EnforceChannelBinding;
};
```

## <a name="members"></a><span data-ttu-id="ed4f6-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ed4f6-109">Members</span></span>

<span data-ttu-id="ed4f6-110">La classe **Win32 \_ TSGatewayServerSettings** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ed4f6-110">The **Win32\_TSGatewayServerSettings** class has these types of members:</span></span>

-   [<span data-ttu-id="ed4f6-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ed4f6-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="ed4f6-112">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed4f6-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="ed4f6-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ed4f6-113">Methods</span></span>

<span data-ttu-id="ed4f6-114">La classe **Win32 \_ TSGatewayServerSettings** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-114">The **Win32\_TSGatewayServerSettings** class has these methods.</span></span>



| <span data-ttu-id="ed4f6-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="ed4f6-115">Method</span></span>                                                                                                                                             | <span data-ttu-id="ed4f6-116">Description</span><span class="sxs-lookup"><span data-stu-id="ed4f6-116">Description</span></span>                                                                                                                                                                                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed4f6-117">**Configurer**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-117">**Configure**</span></span>](configure-win32-tsgatewayserversettings.md)                                                                                       | <span data-ttu-id="ed4f6-118">Configure les paramètres IIS et RPC requis par le service de passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-118">Configures the IIS and RPC settings required by the RD Gateway service.</span></span><br/> <span data-ttu-id="ed4f6-119">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-119">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                               |
| [<span data-ttu-id="ed4f6-120">**EnableCentralCAP**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-120">**EnableCentralCAP**</span></span>](enablecentralcap-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="ed4f6-121">Active ou désactive la propriété **CentralCAPEnabled** , qui détermine si des serveurs de stratégie d’autorisation de connexion centralisée Bureau à distance sont utilisés pour contrôler les stratégies d’autorisation de connexion pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-121">Enables or disables the **CentralCAPEnabled** property, which controls whether central Remote Desktop connection authorization policy (RD CAP) servers are used for controlling connection authorization policies for this server.</span></span><br/>                    |
| [<span data-ttu-id="ed4f6-122">**EnableLogEvent**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-122">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="ed4f6-123">Active ou désactive la journalisation du type d’événement spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-123">Enables or disables logging of the specified event type.</span></span><br/>                                                                                                                                                                                              |
| [<span data-ttu-id="ed4f6-124">**EnableOnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-124">**EnableOnlyConsentCapableClients**</span></span>](enableonlyconsentcapableclients-win32-tsgatewayserversettings.md)                                           | <span data-ttu-id="ed4f6-125">Définit la propriété **OnlyConsentCapableClients** .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-125">Sets the **OnlyConsentCapableClients** property.</span></span><br/> <span data-ttu-id="ed4f6-126">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-126">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                      |
| [<span data-ttu-id="ed4f6-127">**EnableRequestSOH**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-127">**EnableRequestSOH**</span></span>](win32-tsgatewayserversettings-enablerequestsoh.md)                                                                         | <span data-ttu-id="ed4f6-128">Cette méthode n’est pas prise en charge à partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-128">This method is not supported starting with Windows Server 2016.</span></span><br/> <span data-ttu-id="ed4f6-129">**Windows server 2012 R2, Windows server 2012, Windows server 2008 R2 et Windows server 2008 :** Active ou désactive les demandes pour une déclaration d’intégrité (SoH).</span><span class="sxs-lookup"><span data-stu-id="ed4f6-129">**Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:** Enables or disables requests for a Statement of Health (SoH).</span></span><br/> <br/> |
| [<span data-ttu-id="ed4f6-130">**EnableTransport**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-130">**EnableTransport**</span></span>](enabletransport-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="ed4f6-131">Active ou désactive le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-131">Enables or disables the specified transport.</span></span><br/> <span data-ttu-id="ed4f6-132">**Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-132">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ed4f6-133">**EnumAuthenticationPlugins**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-133">**EnumAuthenticationPlugins**</span></span>](enumauthenticationplugins-win32-tsgatewayserversettings.md)                                                       | <span data-ttu-id="ed4f6-134">Énumère tous les plug-ins d’authentification inscrits.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-134">Enumerates all registered authentication plug-ins.</span></span><br/> <span data-ttu-id="ed4f6-135">**Windows Server 2008 :** Cette méthode n’est pas disponible.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-135">**Windows Server 2008:** This method is not available.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="ed4f6-136">**EnumAuthorizationPlugins**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-136">**EnumAuthorizationPlugins**</span></span>](enumauthorizationplugins-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="ed4f6-137">Énumère tous les plug-ins d’autorisation inscrits.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-137">Enumerates all registered authorization plug-ins.</span></span><br/> <span data-ttu-id="ed4f6-138">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-138">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="ed4f6-139">**GetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-139">**GetIPAndPort**</span></span>](getipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="ed4f6-140">Obtient l’adresse IP d’écoute et le numéro de port pour le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-140">Obtains the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="ed4f6-141">**Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-141">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                 |
| [<span data-ttu-id="ed4f6-142">**GetLogEventName**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-142">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="ed4f6-143">Retourne le nom d’événement du journal pour l’index d’événements de journal spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-143">Returns the log event name for the specified log event index.</span></span><br/>                                                                                                                                                                                         |
| [<span data-ttu-id="ed4f6-144">**GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-144">**GetProtocolName**</span></span>](getprotocolname-win32-tsgatewayserversettings.md)                                                                           | <span data-ttu-id="ed4f6-145">Retourne le nom de protocole pour l’index de protocole spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-145">Returns the protocol name for the specified protocol index.</span></span><br/>                                                                                                                                                                                           |
| [<span data-ttu-id="ed4f6-146">**IsLogEventEnabled**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-146">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="ed4f6-147">Indique si le type de journal des événements spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-147">Indicates whether the specified event log type is enabled.</span></span><br/>                                                                                                                                                                                            |
| [<span data-ttu-id="ed4f6-148">**IsTransportEnabled**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-148">**IsTransportEnabled**</span></span>](istransportenabled-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="ed4f6-149">Détermine si le transport spécifié est activé.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-149">Determines whether the specified transport is enabled.</span></span><br/> <span data-ttu-id="ed4f6-150">**Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-150">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                        |
| [<span data-ttu-id="ed4f6-151">**QueryCertContext**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-151">**QueryCertContext**</span></span>](win32-tsgatewayserversettings-querycertcontext.md)                                                                         | <span data-ttu-id="ed4f6-152">Indique si le certificat spécifié est installé.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-152">Indicates whether the specified certificate is installed.</span></span><br/>                                                                                                                                                                                             |
| [<span data-ttu-id="ed4f6-153">**RecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-153">**RecycleRpcApplicationPools**</span></span>](recyclerpcapplicationpools-win32-tsgatewayserversettings.md)                                                     | <span data-ttu-id="ed4f6-154">Recycle les pools d’applications RPC dans IIS.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-154">Recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="ed4f6-155">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-155">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="ed4f6-156">**RefreshCertContext**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-156">**RefreshCertContext**</span></span>](win32-tsgatewayserversettings-refreshcertcontext.md)                                                                     | <span data-ttu-id="ed4f6-157">Actualise le certificat utilisé par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-157">Refreshes the certificate that is used by the RD Gateway server.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="ed4f6-158">**SetAuthenticationPlugin**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-158">**SetAuthenticationPlugin**</span></span>](setauthenticationplugin-win32-tsgatewayserversettings.md)                                                           | <span data-ttu-id="ed4f6-159">Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-159">Sets the current authentication plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="ed4f6-160">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-160">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="ed4f6-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-161">**SetAuthenticationPluginAndRecycleRpcApplicationPools**</span></span>](setauthenticationpluginandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md) | <span data-ttu-id="ed4f6-162">Définit le plug-in d’authentification actuel pour le serveur de passerelle Bureau à distance et recycle les pools d’applications RPC dans IIS.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-162">Sets the current authentication plug-in for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="ed4f6-163">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-163">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                      |
| [<span data-ttu-id="ed4f6-164">**SetAuthorizationPlugin**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-164">**SetAuthorizationPlugin**</span></span>](setauthorizationplugin-win32-tsgatewayserversettings.md)                                                             | <span data-ttu-id="ed4f6-165">Définit le plug-in d’autorisation actuel pour le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-165">Sets the current authorization plug-in for the RD Gateway server.</span></span><br/> <span data-ttu-id="ed4f6-166">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-166">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                     |
| [<span data-ttu-id="ed4f6-167">**SetCertificate**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-167">**SetCertificate**</span></span>](setcertificate-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="ed4f6-168">Définit le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-168">Sets the certificate hash for HTTPS binding on port 443 in IIS.</span></span><br/> <span data-ttu-id="ed4f6-169">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-169">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                       |
| [<span data-ttu-id="ed4f6-170">**SetCertificateACL**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-170">**SetCertificateACL**</span></span>](setcertificateacl-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="ed4f6-171">Définit les listes de contrôle d’accès (ACL) du certificat pour ce serveur.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-171">Sets the certificate access control lists (ACLs) for this server.</span></span><br/>                                                                                                                                                                                     |
| [<span data-ttu-id="ed4f6-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-172">**SetDefaultPluginsAndRecycleRpcApplicationPools**</span></span>](setdefaultpluginsandrecyclerpcapplicationpools-win32-tsgatewayserversettings.md)             | <span data-ttu-id="ed4f6-173">Définit les plug-ins d’authentification et d’autorisation actuels pour le serveur de passerelle Bureau à distance et recycle les pools d’applications RPC dans IIS.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-173">Sets the current authentication and authorization plug-ins for the RD Gateway server and recycles the RPC application pools in IIS.</span></span><br/> <span data-ttu-id="ed4f6-174">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-174">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                   |
| [<span data-ttu-id="ed4f6-175">**SetEnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-175">**SetEnforceChannelBinding**</span></span>](setenforcechannelbinding-win32-tsgatewayserversettings.md)                                                         | <span data-ttu-id="ed4f6-176">Définit la propriété **EnforceChannelBinding** .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-176">Sets the **EnforceChannelBinding** property.</span></span><br/> <span data-ttu-id="ed4f6-177">**Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-177">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                                                  |
| [<span data-ttu-id="ed4f6-178">**SetIPAndPort**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-178">**SetIPAndPort**</span></span>](setipandport-win32-tsgatewayserversettings.md)                                                                                 | <span data-ttu-id="ed4f6-179">Définit l’adresse IP d’écoute et le numéro de port pour le transport spécifié.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-179">Sets the listening IP address and port number for the specified transport.</span></span><br/> <span data-ttu-id="ed4f6-180">**Windows server 2008 R2 et Windows server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-180">**Windows Server 2008 R2 and Windows Server 2008:** This method is not available before Windows Server 2012.</span></span><br/>                                                    |
| [<span data-ttu-id="ed4f6-181">**SetMaxConnections**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-181">**SetMaxConnections**</span></span>](setmaxconnections-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="ed4f6-182">Définit le nombre maximal de connexions autorisées via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-182">Sets the maximum number of allowed connections through RD Gateway.</span></span> <span data-ttu-id="ed4f6-183">Cette méthode modifie les propriétés **MaxConnections** et **UnlimitedConnections** .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-183">This method changes the **MaxConnections** and **UnlimitedConnections** properties.</span></span><br/>                                                                                                |
| [<span data-ttu-id="ed4f6-184">**SetSslBridging**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-184">**SetSslBridging**</span></span>](setsslbridging-win32-tsgatewayserversettings.md)                                                                             | <span data-ttu-id="ed4f6-185">Définit le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-185">Sets the type of SSL bridging to be used by the RD Gateway server.</span></span><br/> <span data-ttu-id="ed4f6-186">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-186">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                    |
| [<span data-ttu-id="ed4f6-187">**TSGRemoveAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-187">**TSGRemoveAdminMsg**</span></span>](tsgremoveadminmsg-win32-tsgatewayserversettings.md)                                                                       | <span data-ttu-id="ed4f6-188">Supprime le message d’administration pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-188">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="ed4f6-189">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-189">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="ed4f6-190">**TSGRemoveConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-190">**TSGRemoveConsentMsg**</span></span>](tsgremoveconsentmsg-win32-tsgatewayserversettings.md)                                                                   | <span data-ttu-id="ed4f6-191">Supprime le message d’administration pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-191">Removes the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="ed4f6-192">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-192">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="ed4f6-193">**TSGStoreAdminMsg**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-193">**TSGStoreAdminMsg**</span></span>](tsgstoreadminmsg-win32-tsgatewayserversettings.md)                                                                         | <span data-ttu-id="ed4f6-194">Met à jour le message d’administration pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-194">Updates the administrative message for the gateway server.</span></span><br/> <span data-ttu-id="ed4f6-195">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-195">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                            |
| [<span data-ttu-id="ed4f6-196">**TSGStoreConsentMsg**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-196">**TSGStoreConsentMsg**</span></span>](tsgstoreconsentmsg-win32-tsgatewayserversettings.md)                                                                     | <span data-ttu-id="ed4f6-197">Met à jour le message de consentement pour le serveur de passerelle.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-197">Updates the consent message for the gateway server.</span></span><br/> <span data-ttu-id="ed4f6-198">**Windows Server 2008 :** Cette méthode n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-198">**Windows Server 2008:** This method is not available before Windows Server 2008 R2.</span></span><br/>                                                                                                   |



 

### <a name="properties"></a><span data-ttu-id="ed4f6-199">Propriétés</span><span class="sxs-lookup"><span data-stu-id="ed4f6-199">Properties</span></span>

<span data-ttu-id="ed4f6-200">La classe **Win32 \_ TSGatewayServerSettings** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-200">The **Win32\_TSGatewayServerSettings** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="ed4f6-201">**adminMessageEndTime**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-201">**adminMessageEndTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-202">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-202">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-203">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-203">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-204">Heure de fin du message d’administration.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-204">The administrative message end time.</span></span>

<span data-ttu-id="ed4f6-205">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-205">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-206">**adminMessageStartTime**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-206">**adminMessageStartTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-207">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-207">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-208">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-208">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-209">Heure de début du message d’administration.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-209">The administrative message start time.</span></span>

<span data-ttu-id="ed4f6-210">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-210">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-211">**adminMessageText**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-211">**adminMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-212">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-212">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-213">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-213">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-214">Texte du message administratif.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-214">The administrative message text.</span></span>

<span data-ttu-id="ed4f6-215">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-215">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-216">**AuthenticationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-216">**AuthenticationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-217">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-217">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-218">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-218">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-219">CLSID du plug-in d’authentification actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-219">The CLSID of the current authentication plug-in.</span></span>

<span data-ttu-id="ed4f6-220">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-220">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-221">**AuthenticationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-221">**AuthenticationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-222">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-223">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-223">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-224">Description du plug-in d’authentification actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-224">The description of the current authentication plug-in.</span></span>

<span data-ttu-id="ed4f6-225">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-225">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-226">**AuthenticationPluginName**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-226">**AuthenticationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-227">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-227">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-228">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-228">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-229">Nom du plug-in d’authentification actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-229">The name of the current authentication plug-in.</span></span>

<span data-ttu-id="ed4f6-230">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-230">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-231">**AuthorizationPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-231">**AuthorizationPluginCLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-232">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-232">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-233">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-233">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-234">CLSID du plug-in d’autorisation actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-234">The CLSID of the current authorization plug-in.</span></span>

<span data-ttu-id="ed4f6-235">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-235">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-236">**AuthorizationPluginDescription**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-236">**AuthorizationPluginDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-237">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-237">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-238">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-238">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-239">Description du plug-in d’autorisation actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-239">The description of the current authorization plug-in.</span></span>

<span data-ttu-id="ed4f6-240">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-240">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-241">**AuthorizationPluginName**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-241">**AuthorizationPluginName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-242">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-242">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-243">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-243">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-244">Nom du plug-in d’autorisation actuel.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-244">The name of the current authorization plug-in.</span></span>

<span data-ttu-id="ed4f6-245">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-245">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-246">**CentralCAPEnabled**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-246">**CentralCAPEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-247">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-247">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-248">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-249">Spécifie si les serveurs d’accès aux services Bureau à distance centraux sont utilisés pour le contrôle de ce serveur.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-249">Specifies whether central RD CAP servers are used for controlling this server.</span></span> <span data-ttu-id="ed4f6-250">Cette propriété peut être modifiée en appelant la méthode [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-250">This property can be changed by calling the [**EnableCentralCAP**](enablecentralcap-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-251">**CertHash**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-251">**CertHash**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-252">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-252">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-253">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-253">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-254">Spécifie le hachage de certificat pour la liaison HTTPs sur le port 443 dans IIS.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-254">Specifies the certificate hash for HTTPS binding on port 443 in IIS.</span></span>

<span data-ttu-id="ed4f6-255">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-255">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-256">**consentMessageText**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-256">**consentMessageText**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-257">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-257">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-258">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-258">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-259">Texte du message de consentement.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-259">The consent message text.</span></span>

<span data-ttu-id="ed4f6-260">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-260">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-261">**EnforceChannelBinding**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-261">**EnforceChannelBinding**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-262">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-262">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-263">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-263">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-264">Indique si la liaison de canal est appliquée pour le transport HTTP.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-264">Indicates if channel binding is enforced for the HTTP transport.</span></span> <span data-ttu-id="ed4f6-265">Cette valeur de propriété peut être modifiée à l’aide de la méthode [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-265">This property value can be changed by using the [**SetEnforceChannelBinding**](setenforcechannelbinding-win32-tsgatewayserversettings.md) method.</span></span>

<span data-ttu-id="ed4f6-266">**Windows server 2008 R2 et Windows server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-266">**Windows Server 2008 R2 and Windows Server 2008:** This property is not available before Windows Server 2012.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-267">**IsConfigured**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-267">**IsConfigured**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-268">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-268">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-269">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-269">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-270">Spécifie si les paramètres IIS et RPC requis par le service de passerelle des services Bureau à distance sont configurés.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-270">Specifies if IIS and RPC settings required by the RD Gateway service are configured.</span></span>

<span data-ttu-id="ed4f6-271">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-271">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-272">**MaxConnections**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-272">**MaxConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-273">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-273">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-274">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-274">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-275">Qualificateurs : [ **clé**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="ed4f6-275">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-276">Retourne le nombre maximal de connexions autorisées via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-276">Returns the maximum number of connections that are allowed through RD Gateway.</span></span> <span data-ttu-id="ed4f6-277">Cette propriété peut être définie à l’aide de la méthode [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-277">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-278">**MaximumAllowedConnectionsBySku**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-278">**MaximumAllowedConnectionsBySku**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-279">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-279">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-280">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-280">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-281">Nombre maximal de connexions autorisé par l’unité de conservation des stocks (SKU).</span><span class="sxs-lookup"><span data-stu-id="ed4f6-281">Maximum number of connections that the stock-keeping unit (SKU) allows.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-282">**MaxLogEvents**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-282">**MaxLogEvents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-283">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-283">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-284">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-284">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-285">Retourne le nombre maximal d’événements de journal.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-285">Returns the maximum number of log events.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-286">**MaxProtocols**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-286">**MaxProtocols**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-287">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-287">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-288">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-288">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-289">Nombre de protocoles pris en charge par la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-289">Number of protocols supported by RD Gateway.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-290">**OnlyConsentCapableClients**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-290">**OnlyConsentCapableClients**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-291">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-291">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-292">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-292">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-293">Spécifie si seuls les clients pouvant être autorisés à se connecter à la passerelle des services Bureau à distance sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-293">Specifies if only clients capable of consent messages are allowed to connect to the RD Gateway.</span></span>

<span data-ttu-id="ed4f6-294">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-294">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="ed4f6-295">différente</span><span class="sxs-lookup"><span data-stu-id="ed4f6-295">nonzero</span></span>
</dt> <dd>

<span data-ttu-id="ed4f6-296">Seuls les clients pouvant prendre en charge les messages de consentement peuvent se connecter.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-296">Only consent message capable clients can connect.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-297">zéro</span><span class="sxs-lookup"><span data-stu-id="ed4f6-297">zero</span></span>
</dt> <dd>

<span data-ttu-id="ed4f6-298">Les clients qui ne sont pas en mesure de prendre en charge les messages peuvent également se connecter.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-298">Clients that are not consent message capable can also connect.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ed4f6-299">**RequestSOH**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-299">**RequestSOH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-300">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-300">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-301">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-301">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-302">Cette propriété n’est pas prise en charge à partir de Windows Server 2016.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-302">This property is not supported starting with Windows Server 2016.</span></span>

<span data-ttu-id="ed4f6-303">\* \* Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 et Windows Server 2008 : \* \*</span><span class="sxs-lookup"><span data-stu-id="ed4f6-303">\*\*Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 and Windows Server 2008:  \*\*</span></span>

<span data-ttu-id="ed4f6-304">Spécifie si le serveur doit demander une déclaration d’intégrité (SoH) au client.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-304">Specifies whether the server must request a Statement of Health (SoH) from the client.</span></span> <span data-ttu-id="ed4f6-305">Cette propriété peut être modifiée à l’aide de la méthode [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-305">This property can be changed by using the [**EnableRequestSOH**](win32-tsgatewayserversettings-enablerequestsoh.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-306">**SkuName**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-306">**SkuName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-307">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-307">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-308">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-308">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-309">Nom de la SKU.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-309">Name of the SKU.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-310">**SslBridging**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-310">**SslBridging**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-311">Type de données : **UInt32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-311">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-312">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-312">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-313">Spécifie le type de pontage SSL à utiliser par le serveur de passerelle Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-313">Specifies which type of SSL bridging to be used by the RD Gateway server.</span></span> <span data-ttu-id="ed4f6-314">Il peut s’agir de l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-314">This can be one of the following values.</span></span>

<span data-ttu-id="ed4f6-315">**Windows Server 2008 :** Cette propriété n’est pas disponible avant Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-315">**Windows Server 2008:** This property is not available before Windows Server 2008 R2.</span></span>

<dt>

<span data-ttu-id="ed4f6-316">0</span><span class="sxs-lookup"><span data-stu-id="ed4f6-316">0</span></span>
</dt> <dd>

<span data-ttu-id="ed4f6-317">Aucun pontage SSL.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-317">No SSL bridging.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-318">1</span><span class="sxs-lookup"><span data-stu-id="ed4f6-318">1</span></span>
</dt> <dd>

<span data-ttu-id="ed4f6-319">Pontage HTTPs vers HTTP.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-319">HTTPS to HTTP bridging.</span></span>

</dd> <dt>

<span data-ttu-id="ed4f6-320">2</span><span class="sxs-lookup"><span data-stu-id="ed4f6-320">2</span></span>
</dt> <dd>

<span data-ttu-id="ed4f6-321">Pontage HTTPs vers HTTPs.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-321">HTTPS to HTTPS bridging.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="ed4f6-322">**UnlimitedConnections**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-322">**UnlimitedConnections**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ed4f6-323">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-323">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="ed4f6-324">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="ed4f6-324">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="ed4f6-325">Indique si un nombre illimité de connexions est autorisé via la passerelle des services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-325">Indicates whether an unlimited number of connections are allowed through RD Gateway.</span></span> <span data-ttu-id="ed4f6-326">Cette propriété peut être définie à l’aide de la méthode [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) .</span><span class="sxs-lookup"><span data-stu-id="ed4f6-326">This property can be set by using the [**SetMaxConnections**](setmaxconnections-win32-tsgatewayserversettings.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ed4f6-327">Notes</span><span class="sxs-lookup"><span data-stu-id="ed4f6-327">Remarks</span></span>

<span data-ttu-id="ed4f6-328">Pour utiliser cette classe, vous devez être membre du groupe administrateurs.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-328">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="ed4f6-329">Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI).</span><span class="sxs-lookup"><span data-stu-id="ed4f6-329">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ed4f6-330">Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-330">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ed4f6-331">Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur.</span><span class="sxs-lookup"><span data-stu-id="ed4f6-331">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ed4f6-332">Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ed4f6-332">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ed4f6-333">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ed4f6-333">Requirements</span></span>



| <span data-ttu-id="ed4f6-334">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ed4f6-334">Requirement</span></span> | <span data-ttu-id="ed4f6-335">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed4f6-335">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed4f6-336">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed4f6-336">Minimum supported client</span></span><br/> | <span data-ttu-id="ed4f6-337">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed4f6-337">None supported</span></span><br/>                                                                |
| <span data-ttu-id="ed4f6-338">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ed4f6-338">Minimum supported server</span></span><br/> | <span data-ttu-id="ed4f6-339">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed4f6-339">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ed4f6-340">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="ed4f6-340">Namespace</span></span><br/>                | <span data-ttu-id="ed4f6-341">Racine \\ cimv2 \\ licences TS</span><span class="sxs-lookup"><span data-stu-id="ed4f6-341">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="ed4f6-342">MOF</span><span class="sxs-lookup"><span data-stu-id="ed4f6-342">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed4f6-343"><dt>TSGateway. mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed4f6-343"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed4f6-344">DLL</span><span class="sxs-lookup"><span data-stu-id="ed4f6-344">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed4f6-345"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed4f6-345"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ed4f6-346">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ed4f6-346">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed4f6-347">**\_TSGatewayConnection Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-347">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="ed4f6-348">**\_TSGatewayConnectionAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-348">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="ed4f6-349">**\_TSGatewayLoadBalancer Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-349">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="ed4f6-350">**\_TSGatewayRADIUSServer Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-350">**Win32\_TSGatewayRADIUSServer**</span></span>](win32-tsgatewayradiusserver.md)
</dt> <dt>

[<span data-ttu-id="ed4f6-351">**\_TSGatewayResourceAuthorizationPolicy Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-351">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="ed4f6-352">**\_TSGatewayResourceGroup Win32**</span><span class="sxs-lookup"><span data-stu-id="ed4f6-352">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> </dl>

 

