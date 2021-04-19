---
title: À propos des extensions NPS
description: Cette section décrit comment implémenter des dll pour étendre les fonctionnalités du serveur NPS. Il décrit l’interaction entre NPS et les dll, et présente des considérations de conception concernant les dll.
ms.assetid: 3d4d8d22-4cd3-48e0-b4a4-dfa0a0b7b87f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05878a5243774046c1ca052052d59be9378483d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106513729"
---
# <a name="about-nps-extensions"></a><span data-ttu-id="d917a-104">À propos des extensions NPS</span><span class="sxs-lookup"><span data-stu-id="d917a-104">About NPS Extensions</span></span>

> [!Note]  
> <span data-ttu-id="d917a-105">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="d917a-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="d917a-106">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="d917a-107">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="d917a-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="d917a-108">Cette section décrit comment implémenter des dll pour étendre les fonctionnalités du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-108">This section describes how to implement DLLs to extend the functionality of NPS.</span></span> <span data-ttu-id="d917a-109">Il décrit l’interaction entre NPS et les dll, et présente des considérations de conception concernant les dll.</span><span class="sxs-lookup"><span data-stu-id="d917a-109">It describes the interaction between NPS and the DLLs, and presents some design considerations regarding the DLLs.</span></span>

<span data-ttu-id="d917a-110">NPS fournit deux points d’extension, un pour l’authentification et l’autre pour l’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d917a-110">NPS provides two extension points, one for authentication and the other for authorization.</span></span> <span data-ttu-id="d917a-111">L’authentification fait référence à la vérification de l’identité de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d917a-111">Authentication refers to verifying the identity of the user.</span></span> <span data-ttu-id="d917a-112">L’autorisation fait référence à la détermination des services que le réseau doit fournir à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d917a-112">Authorization refers to determining what services the network should provide to the user.</span></span> <span data-ttu-id="d917a-113">Les deux points d’extension correspondent aux DLL d’extension d’authentification et aux DLL d’extension d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d917a-113">The two extension points correspond to Authentication Extension DLLs and Authorization Extension DLLs.</span></span> <span data-ttu-id="d917a-114">Chaque point d’extension peut prendre en charge plusieurs dll.</span><span class="sxs-lookup"><span data-stu-id="d917a-114">Each extension point can support multiple DLLs.</span></span>

<span data-ttu-id="d917a-115">NPS fournit des services d’authentification et d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="d917a-115">NPS provides both authentication and authorization services.</span></span> <span data-ttu-id="d917a-116">Les dll d’extension d’authentification sont appelées par NPS avant l’authentification et l’autorisation intégrées du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-116">Authentication Extension DLLs are called by NPS prior to the built-in NPS authentication and authorization.</span></span> <span data-ttu-id="d917a-117">Les dll d’extension d’autorisation sont appelées après l’authentification et l’autorisation du serveur NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-117">Authorization Extension DLLs are called after NPS authentication and authorization.</span></span>

<span data-ttu-id="d917a-118">Le diagramme suivant illustre le déroulement des paquets via un serveur RADIUS NPS développé à l’aide de DLL d’extension.</span><span class="sxs-lookup"><span data-stu-id="d917a-118">The following diagram illustrates the flow of packets through an NPS RADIUS server that is expanded using Extension DLLs.</span></span>

![processus d’authentification et d’autorisation du serveur NPS](images/ias03.png)

<span data-ttu-id="d917a-120">Si une DLL d’extension d’authentification retourne ACCEPT, le paquet ignore l’authentification NPS et passe directement à l’autorisation NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-120">If an Authentication Extension DLL returns ACCEPT, the packet skips the NPS authentication and goes directly to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="d917a-121">Lorsque plusieurs DLL d’extension d’authentification sont présentes, le reste des dll d’extension peut également être ignoré.</span><span class="sxs-lookup"><span data-stu-id="d917a-121">When multiple Authentication Extension DLLs are present, the rest of the Extension DLLs might be skipped as well.</span></span> <span data-ttu-id="d917a-122">Pour plus d’informations, consultez [Configuration des dll d’extension](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) .</span><span class="sxs-lookup"><span data-stu-id="d917a-122">See [Setting Up the Extension DLLs](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls) for more information.</span></span>

 

<span data-ttu-id="d917a-123">Si une DLL d’extension d’authentification retourne CONTINUE, le paquet passe à l’authentification NPS, puis à l’autorisation NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-123">If an Authentication Extension DLL returns CONTINUE, the packet goes to NPS authentication, and then to NPS authorization.</span></span>

> [!Note]  
> <span data-ttu-id="d917a-124">Lorsque plusieurs DLL d’extension d’authentification sont présentes, le reste des dll d’extension d’authentification est appelé avant l’authentification NPS.</span><span class="sxs-lookup"><span data-stu-id="d917a-124">When multiple Authentication Extension DLLs are present, the rest of the Authentication Extension DLLs are invoked before NPS authentication.</span></span>

 

<span data-ttu-id="d917a-125">Les rubriques suivantes décrivent plus en détail les dll d’extension :</span><span class="sxs-lookup"><span data-stu-id="d917a-125">The following topics describe the Extension DLLs in more detail:</span></span>

-   [<span data-ttu-id="d917a-126">Configuration des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="d917a-126">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
-   [<span data-ttu-id="d917a-127">Appel des dll d’extension</span><span class="sxs-lookup"><span data-stu-id="d917a-127">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
-   [<span data-ttu-id="d917a-128">Attributs d’identification utilisateur</span><span class="sxs-lookup"><span data-stu-id="d917a-128">User Identification Attributes</span></span>](/windows/desktop/Nps/ias-user-identification-attributes)

 

 