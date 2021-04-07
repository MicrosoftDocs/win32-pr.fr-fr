---
title: Inscription du serveur DLL pour l’activation du remplacement
description: Inscription du serveur DLL pour l’activation du remplacement
ms.assetid: 7133daa4-43b2-402e-a8ac-b357bea745d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca0af764bebf54590442f87f0b4ffdb1a681012
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730468"
---
# <a name="registering-the-dll-server-for-surrogate-activation"></a><span data-ttu-id="0ad6a-103">Inscription du serveur DLL pour l’activation du remplacement</span><span class="sxs-lookup"><span data-stu-id="0ad6a-103">Registering the DLL Server for Surrogate Activation</span></span>

<span data-ttu-id="0ad6a-104">Un serveur DLL est chargé dans un processus de substitution dans les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ad6a-104">A DLL server will be loaded into a surrogate process under the following conditions:</span></span>

-   <span data-ttu-id="0ad6a-105">Il doit y avoir une valeur AppID spécifiée sous la clé CLSID dans le registre, et une clé [AppID](appid-key.md) correspondante.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-105">There must be an AppID value specified under the CLSID key in the registry, and a corresponding [AppID](appid-key.md) key.</span></span>
-   <span data-ttu-id="0ad6a-106">Dans un appel d’activation, le bit du [**\_ \_ serveur local CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) est défini et la clé CLSID ne spécifie pas [LocalServer32](localserver32.md), [LocalServer](localserver.md)ou [LocalService](localservice.md).</span><span class="sxs-lookup"><span data-stu-id="0ad6a-106">In an activation call, the [**CLSCTX\_LOCAL\_SERVER**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx) bit is set and the CLSID key does not specify [LocalServer32](localserver32.md), [LocalServer](localserver.md), or [LocalService](localservice.md).</span></span> <span data-ttu-id="0ad6a-107">Si d’autres bits **CLSCTX** sont définis, l' [**algorithme de traitement**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)pour les indicateurs d’exécution in-process, local ou distant est suivi.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-107">If other **CLSCTX** bits are set, the [**processing algorithm**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)for the in-process, local, or remote execution flags is followed.</span></span>
-   <span data-ttu-id="0ad6a-108">La clé CLSID contient la sous-clé [InprocServer32](inprocserver32.md) .</span><span class="sxs-lookup"><span data-stu-id="0ad6a-108">The CLSID key contains the [InprocServer32](inprocserver32.md) subkey.</span></span>
-   <span data-ttu-id="0ad6a-109">La DLL proxy/stub spécifiée dans la clé **InprocServer32** existe.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-109">The proxy/stub DLL specified in the **InprocServer32** key exists.</span></span>
-   <span data-ttu-id="0ad6a-110">La valeur [DllSurrogate](dllsurrogate.md) existe sous la clé **AppID** .</span><span class="sxs-lookup"><span data-stu-id="0ad6a-110">The [DllSurrogate](dllsurrogate.md) value exists under the **AppID** key.</span></span>

<span data-ttu-id="0ad6a-111">S’il existe une valeur **LocalServer**, **LocalServer32** ou **LocalService** indiquant l’existence d’un fichier exe, le service ou le serveur exe est toujours lancé en priorité pour le chargement d’un serveur dll dans un processus de substitution.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-111">If there is a **LocalServer**, **LocalServer32**, or **LocalService**, indicating the existence of an EXE, the EXE server or service will always be launched in preference to loading a DLL server into a surrogate process.</span></span>

<span data-ttu-id="0ad6a-112">La valeur nommée **DllSurrogate** doit être spécifiée pour que l’activation de substitution se produise.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-112">The **DllSurrogate** named-value must be specified for surrogate activation to occur.</span></span> <span data-ttu-id="0ad6a-113">L’activation fait référence aux appels à l’une des fonctions d’activation suivantes :</span><span class="sxs-lookup"><span data-stu-id="0ad6a-113">Activation refers to calls to any of the following activation functions:</span></span>

-   [<span data-ttu-id="0ad6a-114">**CoGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="0ad6a-114">**CoGetClassObject**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject)
-   [<span data-ttu-id="0ad6a-115">**CoCreateInstanceEx**</span><span class="sxs-lookup"><span data-stu-id="0ad6a-115">**CoCreateInstanceEx**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstanceex)
-   [<span data-ttu-id="0ad6a-116">**CoGetInstanceFromFile**</span><span class="sxs-lookup"><span data-stu-id="0ad6a-116">**CoGetInstanceFromFile**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromfile)
-   [<span data-ttu-id="0ad6a-117">**CoGetInstanceFromIStorage**</span><span class="sxs-lookup"><span data-stu-id="0ad6a-117">**CoGetInstanceFromIStorage**</span></span>](/windows/desktop/api/Objbase/nf-objbase-cogetinstancefromistorage)
-   [<span data-ttu-id="0ad6a-118">**IMoniker :: BindToObject**</span><span class="sxs-lookup"><span data-stu-id="0ad6a-118">**IMoniker::BindToObject**</span></span>](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject)

<span data-ttu-id="0ad6a-119">Pour lancer une instance du substitut fourni par le système, définissez la valeur de **DllSurrogate** sur une chaîne vide ou sur **null**.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-119">To launch an instance of the system-supplied surrogate, set the value of **DllSurrogate** either to an empty string or to **NULL**.</span></span> <span data-ttu-id="0ad6a-120">Pour spécifier le lancement d’un substitut personnalisé, définissez la valeur sur le chemin d’accès du substitut.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-120">To specify the launch of a custom surrogate, set the value to the path of the surrogate.</span></span>

<span data-ttu-id="0ad6a-121">Si [RemoteServerName](remoteservername.md) et **DllSurrogate** sont tous les deux spécifiés pour le même AppID, la valeur **RemoteServerName** est ignorée et la valeur **DllSurrogate** provoque une activation sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-121">If both [RemoteServerName](remoteservername.md) and **DllSurrogate** are specified for the same AppID, the **RemoteServerName** value is ignored and the **DllSurrogate** value causes an activation on the local computer.</span></span> <span data-ttu-id="0ad6a-122">Pour l’activation de substitution à distance, spécifiez **RemoteServerName** mais pas **DllSurrogate** sur le client, puis spécifiez **DllSurrogate** sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-122">For remote surrogate activation, specify **RemoteServerName** but not **DllSurrogate** on the client, and specify **DllSurrogate** on the server.</span></span>

<span data-ttu-id="0ad6a-123">Un serveur DLL conçu pour s’exécuter toujours seul dans son propre processus de substitution est mieux configuré avec un AppID égal à son CLSID.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-123">A DLL server that is designed to always run alone in its own surrogate process is best configured with an AppID equal its CLSID.</span></span> <span data-ttu-id="0ad6a-124">Sous **AppID**, il vous suffit de spécifier une valeur nommée **DllSurrogate** avec une valeur de chaîne vide.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-124">Under **AppID**, simply specify a **DllSurrogate** named-value with an empty string value.</span></span>

<span data-ttu-id="0ad6a-125">Il est préférable de configurer un serveur de DLL conçu pour s’exécuter seul dans son propre processus de substitution et pour traiter plusieurs clients sur un réseau avec une valeur [runas](runas.md) spécifiée sous la clé de Registre **AppID** .</span><span class="sxs-lookup"><span data-stu-id="0ad6a-125">It is best to configure a DLL server that is designed to run alone in its own surrogate process and to service multiple clients across a network with a [RunAs](runas.md) value specified under the **AppID** registry key.</span></span> <span data-ttu-id="0ad6a-126">Si le **runas** spécifie « utilisateur interactif » ou une identité d’utilisateur spécifique dépend de l’interface utilisateur, de la sécurité et de la configuration requise du serveur.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-126">Whether the **RunAs** specifies "Interactive User" or a specific user identity depends upon the user interface, security, and other server requirements.</span></span> <span data-ttu-id="0ad6a-127">Lorsqu’une valeur **runas** est spécifiée, une seule instance du serveur est chargée pour le service de tous les clients, quelle que soit l’identité du client.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-127">When a **RunAs** value is specified, only one instance of the server is loaded to service all of the clients, regardless of the identity of the client.</span></span> <span data-ttu-id="0ad6a-128">En revanche, ne configurez pas le serveur avec **runas** si l’intention est de faire en sorte qu’une instance du serveur dll s’exécute en substitution pour traiter chaque identité de client distant.</span><span class="sxs-lookup"><span data-stu-id="0ad6a-128">On the other hand, do not configure the server with **RunAs** if the intention is to have one instance of the DLL server running in surrogate to service each remote client identity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ad6a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0ad6a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ad6a-130">Configuration requise du serveur DLL</span><span class="sxs-lookup"><span data-stu-id="0ad6a-130">DLL Server Requirements</span></span>](dll-server-requirements.md)
</dt> <dt>

[<span data-ttu-id="0ad6a-131">Partage de substitution</span><span class="sxs-lookup"><span data-stu-id="0ad6a-131">Surrogate Sharing</span></span>](surrogate-sharing.md)
</dt> </dl>

 

 