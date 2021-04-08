---
title: Extension de session Broker des services Terminal Server
description: Vous pouvez étendre TS \ 160 ; Session Broker à l’aide de l’interface IWTSSBPlugin COM.
ms.assetid: f111d6e6-90ca-4eff-ab0e-02de25f7d6ad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b84471bcf2125017b8eef273cdb78e61a9bc620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729292"
---
# <a name="extending-terminal-services-session-broker"></a><span data-ttu-id="4b7c0-103">Extension de session Broker des services Terminal Server</span><span class="sxs-lookup"><span data-stu-id="4b7c0-103">Extending Terminal Services Session Broker</span></span>

<span data-ttu-id="4b7c0-104">Session Broker TS (session Broker TS) détermine si une session est déjà ouverte pour un utilisateur qui initie une connexion.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-104">Terminal Services Session Broker (TS Session Broker) determines whether a user who initiates a connection has a session open already.</span></span> <span data-ttu-id="4b7c0-105">Dans ce cas, le service session Broker TS achemine la connexion entrante vers le serveur hôte de session Bureau à distance (hôte de session Bureau à distance) avec la session existante.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-105">If so, TS Session Broker routes the incoming connection to the Remote Desktop Session Host (RD Session Host) server with the existing session.</span></span> <span data-ttu-id="4b7c0-106">Si ce n’est pas le cas, le service session Broker TS achemine la connexion entrante vers le serveur hôte de session Bureau à distance avec le moins de sessions.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-106">If not, TS Session Broker routes the incoming connection to the RD Session Host server with the fewest sessions.</span></span>

<span data-ttu-id="4b7c0-107">Vous pouvez étendre session Broker TS à l’aide de l’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) com.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-107">You can extend TS Session Broker by using the [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) COM interface.</span></span> <span data-ttu-id="4b7c0-108">Vous pouvez utiliser cette interface pour gérer les connexions aux serveurs hôtes de session Bureau à distance, ainsi qu’à tout type de connexion protocole RDP (Remote Desktop Protocol) (RDP), par exemple, les connexions aux machines virtuelles invitées qui exécutent Windows Vista Enterprise central Desktop (VECD) sur un ordinateur hôte d’ordinateur virtuel Hyper-V Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-108">You can use this interface to manage connections to RD Session Host servers as well as any kind of Remote Desktop Protocol (RDP) connection, for example, connections to guest virtual machines that are running Windows Vista Enterprise Centralized Desktop (VECD) on a Windows Server 2008 Hyper-V virtual machine host.</span></span>

<span data-ttu-id="4b7c0-109">L’interface [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) offre plusieurs avantages :</span><span class="sxs-lookup"><span data-stu-id="4b7c0-109">The [**IWTSSBPlugin**](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin) interface offers several benefits:</span></span>

-   <span data-ttu-id="4b7c0-110">Il n’est pas nécessaire d’installer un agent sur le client ou le serveur hôte de session Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-110">It is not necessary to install an agent on the client or the RD Session Host server.</span></span>
-   <span data-ttu-id="4b7c0-111">Le plug-in peut interagir de façon transparente avec d’autres services de rôle Services Bureau à distance, tels que Bureau à distance passerelle (passerelle des services Bureau à distance), et s’appuyer sur les informations de session Broker TS sur les États de session et d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-111">The plug-in can interact seamlessly with other Remote Desktop Services role services, such as Remote Desktop Gateway (RD Gateway), and rely on information from TS Session Broker about session and computer states.</span></span>
-   <span data-ttu-id="4b7c0-112">Vous pouvez utiliser le plug-in pour gérer les connexions avec des appareils client ou serveur qui prennent en charge RDP 5,2 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-112">You can use the plug-in to manage connections with client or server devices that support RDP 5.2 or later.</span></span>
-   <span data-ttu-id="4b7c0-113">Vous pouvez utiliser le plug-in pour activer les solutions de bureau centralisées de Windows Vista Enterprise.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-113">You can use the plug-in to enable Windows Vista Enterprise Centralized Desktop solutions.</span></span>

<span data-ttu-id="4b7c0-114">Lorsque vous implémentez les méthodes de cette interface, gardez les points suivants à l’esprit :</span><span class="sxs-lookup"><span data-stu-id="4b7c0-114">When you implement the methods of this interface, keep the following points in mind:</span></span>

-   <span data-ttu-id="4b7c0-115">Session Broker TS peut appeler les méthodes de cet objet COM à partir de plusieurs threads.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-115">TS Session Broker might call the methods of this COM object from multiple threads.</span></span>
-   <span data-ttu-id="4b7c0-116">Si l’une des méthodes appelées ne retourne pas immédiatement et avec succès, le service session Broker TS n’effectue plus d’appels au plug-in et revient à sa logique d’équilibrage de charge native.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-116">If any of the called methods do not return immediately and successfully, TS Session Broker makes no more calls to the plug-in and reverts to its native load-balancing logic.</span></span> <span data-ttu-id="4b7c0-117">Pour reprendre les appels au plug-in, vous devez redémarrer le service session Broker des services Terminal Server.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-117">To resume calls to the plug-in, you must restart the Terminal Services Session Broker service.</span></span>
-   <span data-ttu-id="4b7c0-118">Vous devez inscrire le plug-in en tant qu’objet COM à l’ensemble du système à l’aide de Regsvr32.exe.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-118">You must register the plug-in as a system-wide COM object by using Regsvr32.exe.</span></span> <span data-ttu-id="4b7c0-119">Étant donné que le service session Broker des services Terminal Server s’exécute sous le compte « NetworkService », vous devez accorder au compte « NetworkService » les autorisations de lancement, d’activation et d’accès requises à l’aide de Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="4b7c0-119">Because the Terminal Services Session Broker service runs under the "NetworkService" account, you must give the "NetworkService" account the required launch, activation, and access permissions by using Dcomcnfg.exe.</span></span> <span data-ttu-id="4b7c0-120">Le service session Broker TS recherche le CLSID de l’objet COM qui représente le plug-in dans la sous-clé de Registre suivante :</span><span class="sxs-lookup"><span data-stu-id="4b7c0-120">The Terminal Services Session Broker service looks for the CLSID of the COM object that represents the plug-in in the following registry subkey:</span></span>

    <span data-ttu-id="4b7c0-121">**HKEY \_ Paramètres \_** de Tssdis des services de l’ordinateur local \\  \\  \\  \\  \\ **paramètres** \\ **ExtensibilityPluginCLSID**</span><span class="sxs-lookup"><span data-stu-id="4b7c0-121">**HKEY\_LOCAL\_MACHINE**\\**SYSTEM**\\**CurrentControlSet**\\**Services**\\**Tssdis**\\**Parameters**\\**ExtensibilityPluginCLSID**</span></span>

<span data-ttu-id="4b7c0-122">Pour plus d’informations sur la Dcomcnfg.exe, consultez Activation de la [sécurité com à l’aide de DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span><span class="sxs-lookup"><span data-stu-id="4b7c0-122">For more information about Dcomcnfg.exe, see [Enabling COM Security Using DCOMCNFG](/windows/desktop/com/enabling-com-security-using-dcomcnfg).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b7c0-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4b7c0-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b7c0-124">**IWTSSBPlugin**</span><span class="sxs-lookup"><span data-stu-id="4b7c0-124">**IWTSSBPlugin**</span></span>](/windows/desktop/api/Tssbx/nn-tssbx-iwtssbplugin)
</dt> </dl>

 

 