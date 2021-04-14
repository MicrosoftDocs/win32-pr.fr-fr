---
title: Services Bureau à distance les classes de configuration
description: Le fournisseur WMI de configuration Services Bureau à distance fournit les classes suivantes. Une illustration suit.
ms.assetid: 94f61783-b259-4f0f-ac06-84bfbf4f5996
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc9c58be85b8b4efc35495f35902ab67b35ad153
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382001"
---
# <a name="remote-desktop-services-configuration-classes"></a><span data-ttu-id="8cdf0-104">Services Bureau à distance les classes de configuration</span><span class="sxs-lookup"><span data-stu-id="8cdf0-104">Remote Desktop Services Configuration classes</span></span>

<span data-ttu-id="8cdf0-105">Le fournisseur WMI de configuration Services Bureau à distance fournit les classes suivantes.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-105">The Remote Desktop Services Configuration WMI provider provides the following classes.</span></span> <span data-ttu-id="8cdf0-106">Une illustration suit.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-106">An illustration follows.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8cdf0-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8cdf0-107">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="8cdf0-108">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-108">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-109">Représente l’association entre les éléments système managés et la classe de paramètres définie pour eux.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-109">Represents the association between managed system elements and the setting class defined for them.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-110">**\_LOGICALELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-110">**CIM\_LogicalElement**</span></span>](cim-logicalelement.md)
</dt> <dd>

<span data-ttu-id="8cdf0-111">Classe de base pour tous les composants système qui représentent des composants système abstraits, tels que des profils, des processus ou des fonctionnalités système, sous la forme d’unités logiques.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-111">The base class for all system components that represent abstract system components, such as profiles, processes, or system capabilities, in the form of logical devices.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-112">**\_MANAGEDSYSTEMELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-112">**CIM\_ManagedSystemElement**</span></span>](cim-managedsystemelement.md)
</dt> <dd>

<span data-ttu-id="8cdf0-113">Classe de base pour la hiérarchie des éléments système.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-113">The base class for the system element hierarchy.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-114">**\_Paramètre CIM**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-114">**CIM\_Setting**</span></span>](cim-setting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-115">Représente des paramètres de configuration et opérationnels pour un ou plusieurs éléments système gérés.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-115">Represents configuration-related and operational parameters for one or more managed system elements.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-116">**\_Terminal Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-116">**Win32\_Terminal**</span></span>](win32-terminal.md)
</dt> <dd>

<span data-ttu-id="8cdf0-117">représente un terminal.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-117">represents a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-118">**\_TerminalError Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-118">**Win32\_TerminalError**</span></span>](win32-terminalerror.md)
</dt> <dd>

<span data-ttu-id="8cdf0-119">Représente une erreur de terminal.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-119">Represents a terminal error.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-120">**\_TerminalService Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-120">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dd>

<span data-ttu-id="8cdf0-121">une sous-classe de la classe de [**\_ service Win32**](/windows/desktop/CIMWin32Prov/win32-service) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-121">a subclass of the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) class.</span></span> <span data-ttu-id="8cdf0-122">[**Win32 \_ TerminalService**](win32-terminalservice.md) représente la propriété d' **élément** de l’Association [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-122">[**Win32\_TerminalService**](win32-terminalservice.md) represents the **Element** property of the [**Win32\_TerminalServiceToSetting**](win32-terminalservicetosetting.md) association.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-123">**\_TerminalServiceSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-123">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-124">représente la configuration d’un serveur hôte de session Bureau à distance (hôte de session Bureau à distance).</span><span class="sxs-lookup"><span data-stu-id="8cdf0-124">represents the configuration for a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-125">**\_TerminalServiceToSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-125">**Win32\_TerminalServiceToSetting**</span></span>](win32-terminalservicetosetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-126">représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et le paramètre d’une propriété [**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) particulière.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-126">represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and the setting of a particular [**Win32\_TerminalServiceSetting**](win32-terminalservicesetting.md) property.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-127">**\_TerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-127">**Win32\_TerminalSetting**</span></span>](win32-terminalsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-128">représente les paramètres qui peuvent être appliqués à un terminal.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-128">represents the settings that can be applied to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-129">**\_TerminalTerminalSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-129">**Win32\_TerminalTerminalSetting**</span></span>](win32-terminalterminalsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-130">représente l’association entre un terminal et ses paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-130">represents the association between a terminal and its configuration settings.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-131">**\_TSAccount Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-131">**Win32\_TSAccount**</span></span>](win32-tsaccount.md)
</dt> <dd>

<span data-ttu-id="8cdf0-132">autorise la suppression d’un compte qui existe sur [**le \_ Terminal Win32**](win32-terminal.md) et la modification des autorisations existantes.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-132">allows deletion of an account that exists on the [**Win32\_Terminal**](win32-terminal.md) and modification of existing permissions.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-133">**\_TSClientSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-133">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-134">définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) associée à la stratégie de connexion.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-134">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to connection policy.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-135">**\_TSDiscoveredLicenseServer Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-135">**Win32\_TSDiscoveredLicenseServer**</span></span>](win32-tsdiscoveredlicenseserver.md)
</dt> <dd>

<span data-ttu-id="8cdf0-136">Fournit des détails sur le serveur de licences Bureau à distance détecté.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-136">Provides details about the discovered Remote Desktop license server.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-137">**\_TSEnvironmentSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-137">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-138">définit les paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris la stratégie de programme initiale.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-138">defines the configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including initial program policy.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-139">**\_TSGeneralSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-139">**Win32\_TSGeneralSetting**</span></span>](win32-tsgeneralsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-140">représente les paramètres généraux du terminal, tels que le niveau de chiffrement et le protocole de transport.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-140">represents general settings of the terminal such as the encryption level and transport protocol.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-141">**\_TSLogonSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-141">**Win32\_TSLogonSetting**</span></span>](win32-tslogonsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-142">définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) relative à l’ouverture de session client.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-142">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class related to client logon.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-143">**\_TSNetworkAdapterListSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-143">**Win32\_TSNetworkAdapterListSetting**</span></span>](win32-tsnetworkadapterlistsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-144">énumère la liste des cartes réseau qui peuvent être configurées pour un [**\_ Terminal Win32**](win32-terminal.md), selon le protocole terminal et la méthode de transport spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-144">enumerates the list of network adapters that can be configured for a [**Win32\_Terminal**](win32-terminal.md), based on the specified terminal protocol and transport method.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-145">**\_TSNetworkAdapterSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-145">**Win32\_TSNetworkAdapterSetting**</span></span>](win32-tsnetworkadaptersetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-146">définit différents paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , y compris les propriétés associées à la carte réseau et le nombre maximal de connexions autorisées.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-146">defines various configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class including properties related to the network adapter and the maximum number of connections allowed.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-147">**\_TSPermissionsSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-147">**Win32\_TSPermissionsSetting**</span></span>](win32-tspermissionssetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-148">comprend une méthode pour ajouter de nouveaux comptes au terminal et une méthode pour restaurer les autorisations par défaut sur un terminal.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-148">includes a method to add new accounts to the terminal and a method to restore the default permissions to a terminal.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-149">**\_TSRemoteControlSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-149">**Win32\_TSRemoteControlSetting**</span></span>](win32-tsremotecontrolsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-150">définit les paramètres de configuration du contrôle à distance pour la classe de [**\_ Terminal Win32**](win32-terminal.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-150">defines the remote control configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-151">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-151">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> <dd>

<span data-ttu-id="8cdf0-152">Définit les paramètres de configuration du Service Broker pour les connexions Bureau à distance Connexion Bureau à distance pour la classe [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-152">Defines the Remote Desktop Connection Broker (RD Connection Broker) configuration settings for the [**Win32\_TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-153">**\_TSSessionDirectorySetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-153">**Win32\_TSSessionDirectorySetting**</span></span>](win32-tssessiondirectorysetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-154">Représente l’association entre une instance de la classe [**Win32 \_ TerminalService**](win32-terminalservice.md) et une instance de la classe [**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-154">Represents the association between an instance of the [**Win32\_TerminalService**](win32-terminalservice.md) class and an instance of the [**Win32\_TSSessionDirectory**](win32-tssessiondirectory.md) class.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-155">**\_TSSessionSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-155">**Win32\_TSSessionSetting**</span></span>](win32-tssessionsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-156">définit des paramètres de configuration pour la classe de [**\_ Terminal Win32**](win32-terminal.md) , tels que les limites de temps, les actions de déconnexion et de reconnexion.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-156">defines configuration settings for the [**Win32\_Terminal**](win32-terminal.md) class such as time-limits, and disconnection and reconnection actions.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-157">**\_TSVirtualIP Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-157">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> <dd>

<span data-ttu-id="8cdf0-158">Définit les paramètres de virtualisation IP (Internet Protocol) pour un serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-158">Defines Internet protocol (IP) virtualization settings for a RD Session Host server.</span></span>

</dd> <dt>

[<span data-ttu-id="8cdf0-159">**\_TSVirtualIPSetting Win32**</span><span class="sxs-lookup"><span data-stu-id="8cdf0-159">**Win32\_TSVirtualIPSetting**</span></span>](win32-tsvirtualipsetting.md)
</dt> <dd>

<span data-ttu-id="8cdf0-160">Représente l’association entre une classe d’élément [**Win32 \_ TerminalService**](win32-terminalservice.md) et une classe de paramètre [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="8cdf0-160">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

</dd> </dl>

<span data-ttu-id="8cdf0-161">L’illustration suivante montre les relations entre ces classes.</span><span class="sxs-lookup"><span data-stu-id="8cdf0-161">The following illustration shows the relationships between these classes.</span></span>

![relations entre les classes prises en charge](images/tswmi.png)

 

 