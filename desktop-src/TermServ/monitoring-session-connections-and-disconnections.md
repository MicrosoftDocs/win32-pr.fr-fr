---
title: Surveillance des connexions et des déconnexions de session
description: Pour inscrire une application avec Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé.
ms.assetid: 8524cb7a-a930-431a-bc5f-b0793781de15
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e819b13594ecec14a2b425560152cadedd4e9122
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031344"
---
# <a name="monitoring-session-connections-and-disconnections"></a><span data-ttu-id="cbb58-103">Surveillance des connexions et des déconnexions de session</span><span class="sxs-lookup"><span data-stu-id="cbb58-103">Monitoring session connections and disconnections</span></span>

<span data-ttu-id="cbb58-104">Pour une application de service, telle qu’une application de serveur de canal virtuel, pour surveiller les connexions et les déconnexions de session, vous devez l’inscrire auprès de Services Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="cbb58-104">For a service application, such as a virtual channel server application, to monitor session connections and disconnections, you must register it with Remote Desktop Services.</span></span> <span data-ttu-id="cbb58-105">Pour inscrire l’application auprès de Services Bureau à distance, stockez le nom de l’application de serveur de canal virtuel dans le registre en ajoutant une sous-clé sous l’emplacement suivant :</span><span class="sxs-lookup"><span data-stu-id="cbb58-105">To register the application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey under the following location:</span></span>

<span data-ttu-id="cbb58-106">**HKEY \_ \_** \\  \\  \\  \\  \\ **Compléments** TerminalServer du contrôle CurrentControlSet du système de l’ordinateur local</span><span class="sxs-lookup"><span data-stu-id="cbb58-106">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**</span></span>

<span data-ttu-id="cbb58-107">La sous-clé peut avoir n’importe quel nom.</span><span class="sxs-lookup"><span data-stu-id="cbb58-107">The subkey can have any name.</span></span> <span data-ttu-id="cbb58-108">Elle doit avoir une valeur **reg \_ SZ** , **Name**, qui contient le nom symbolique de l’application.</span><span class="sxs-lookup"><span data-stu-id="cbb58-108">It must have a **REG\_SZ** value, **Name**, that contains the symbolic name of the application.</span></span>

``` syntax
Name = AddinName
```

<span data-ttu-id="cbb58-109">La longueur maximale de la sous-clé et de la valeur de **Name** est de 99 caractères.</span><span class="sxs-lookup"><span data-stu-id="cbb58-109">The maximum length of both the subkey and the value of **Name** is 99 characters.</span></span>

<span data-ttu-id="cbb58-110">La sous-clé doit également avoir une valeur **reg \_ DWORD** qui indique le type d’application serveur.</span><span class="sxs-lookup"><span data-stu-id="cbb58-110">The subkey must also have a **REG\_DWORD** value that indicates the type of server application.</span></span>

``` syntax
Type = AddinType
```

<span data-ttu-id="cbb58-111">*AddinType* doit avoir la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="cbb58-111">*AddinType* must be the following value.</span></span>



| <span data-ttu-id="cbb58-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="cbb58-112">Value</span></span> | <span data-ttu-id="cbb58-113">Signification</span><span class="sxs-lookup"><span data-stu-id="cbb58-113">Meaning</span></span>                               |
|-------|---------------------------------------|
| <span data-ttu-id="cbb58-114">3</span><span class="sxs-lookup"><span data-stu-id="cbb58-114">3</span></span>     | <span data-ttu-id="cbb58-115">Application en mode utilisateur, espace de session.</span><span class="sxs-lookup"><span data-stu-id="cbb58-115">User-mode application, session space.</span></span> |



 

<span data-ttu-id="cbb58-116">L’inscription de l’application de service prend effet uniquement dans les sessions créées après l’inscription.</span><span class="sxs-lookup"><span data-stu-id="cbb58-116">Registration of the service application takes effect only in sessions created after the registration was performed.</span></span>

<span data-ttu-id="cbb58-117">Pour chaque application de service inscrite, Services Bureau à distance signale un ensemble d’objets d’événement lorsqu’un client se connecte ou se déconnecte de la session.</span><span class="sxs-lookup"><span data-stu-id="cbb58-117">For each registered service application, Remote Desktop Services will signal a set of event objects when a client connects or disconnects from the session.</span></span> <span data-ttu-id="cbb58-118">Chaque plug-in de canal virtuel doit s’inscrire et créer les événements de notification en appelant [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span><span class="sxs-lookup"><span data-stu-id="cbb58-118">Each virtual channel plug-in must register itself and create the notification events by calling [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa).</span></span> <span data-ttu-id="cbb58-119">Les noms de ces objets d’événement respectent le format suivant.</span><span class="sxs-lookup"><span data-stu-id="cbb58-119">The names of these event objects adhere to the following format.</span></span>

``` syntax
AddinName-Reconnect

AddinName-Disconnect
```

<span data-ttu-id="cbb58-120">*AddInName* est la chaîne spécifiée dans la valeur **Name** de la sous-clé de Registre sous laquelle l’application serveur est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cbb58-120">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="cbb58-121">La création de ces événements dans une session entraîne leur création dans un répertoire d’événements par session spécial.</span><span class="sxs-lookup"><span data-stu-id="cbb58-121">Creating these events under a session causes them to be created in a special per-session event directory.</span></span> <span data-ttu-id="cbb58-122">Le répertoire des événements fournit une sécurité supplémentaire en empêchant les applications d’autres sessions de modifier l’état de ces événements.</span><span class="sxs-lookup"><span data-stu-id="cbb58-122">The event directory provides added security by preventing applications in other sessions from modifying the state of these events.</span></span>

<span data-ttu-id="cbb58-123">Pour contrôler si les événements de reconnexion et de déconnexion sont reçus sur le serveur, vous pouvez placer l’indicateur **RemoteControlPersistent** dans le Registre sous la clé suivante :</span><span class="sxs-lookup"><span data-stu-id="cbb58-123">To control whether RECONNECT and DISCONNECT events are received on the server, you can place the **RemoteControlPersistent** flag in the registry under the following key:</span></span>

<span data-ttu-id="cbb58-124">**HKEY \_ Système d' \_ ordinateur local** \\  \\  \\ **contrôle** CurrentControlSet \\ **TerminalServer** \\ **AddIns** \\ *AddInName*</span><span class="sxs-lookup"><span data-stu-id="cbb58-124">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Control**\\**TerminalServer**\\**Addins**\\*addinname*</span></span>

<span data-ttu-id="cbb58-125">L’indicateur active ou désactive les événements de reconnexion et de déconnexion lorsqu’une session cliente démarre ou s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cbb58-125">The flag enables or disables RECONNECT and DISCONNECT events from being signaled when a client session starts or stops.</span></span> <span data-ttu-id="cbb58-126">La syntaxe de la valeur **reg \_ DWORD** est la suivante.</span><span class="sxs-lookup"><span data-stu-id="cbb58-126">The syntax of the **REG\_DWORD** value is the following.</span></span>

``` syntax
RemoteControlPersistent = flag
```

<span data-ttu-id="cbb58-127">La valeur de *Flag* peut être un ou zéro.</span><span class="sxs-lookup"><span data-stu-id="cbb58-127">The value of *flag* can be one or zero.</span></span> <span data-ttu-id="cbb58-128">Zéro est la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="cbb58-128">Zero is the default value.</span></span> <span data-ttu-id="cbb58-129">Si la valeur est définie sur un, l’application de service n’est pas avertie si la session cliente est démarrée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="cbb58-129">If set to one, the service application will not be notified if the client session is started or stopped.</span></span> <span data-ttu-id="cbb58-130">Si la valeur est zéro, un événement de reconnexion est signalé au démarrage de la session cliente et un événement de déconnexion est signalé lorsque la session cliente s’arrête.</span><span class="sxs-lookup"><span data-stu-id="cbb58-130">If set to zero, a RECONNECT event is signaled when the client session starts, and a DISCONNECT event is signaled when the client session stops.</span></span>

<span data-ttu-id="cbb58-131">Le format de nom d’objet d’événement précédent est toujours pris en charge dans Windows Server 2008 pour des raisons de compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="cbb58-131">The previous event-object name format is still supported in Windows Server 2008 for backward compatibility.</span></span> <span data-ttu-id="cbb58-132">Nous vous recommandons d’utiliser le format Windows Server 2008 plus récent, car il est plus sécurisé.</span><span class="sxs-lookup"><span data-stu-id="cbb58-132">It is recommended that you use the newer Windows Server 2008 format because it is more secure.</span></span>

<span data-ttu-id="cbb58-133">Le format d’événement précédent est le suivant.</span><span class="sxs-lookup"><span data-stu-id="cbb58-133">The previous event format is as follows.</span></span>

``` syntax
Global\AddinName-SessionId-Reconnect
 
Global\AddinName-SessionId-Disconnect
```

<span data-ttu-id="cbb58-134">*AddInName* est la chaîne spécifiée dans la valeur **Name** de la sous-clé de Registre sous laquelle l’application serveur est inscrite.</span><span class="sxs-lookup"><span data-stu-id="cbb58-134">*AddinName* is the string specified in the **Name** value of the registry subkey under which the server application is registered.</span></span> <span data-ttu-id="cbb58-135">*SessionID* est l’identificateur de session d’une session cliente.</span><span class="sxs-lookup"><span data-stu-id="cbb58-135">*SessionId* is the session identifier of a client session.</span></span>

 

 