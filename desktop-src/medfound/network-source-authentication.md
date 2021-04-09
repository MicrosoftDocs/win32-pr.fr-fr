---
description: Authentification de la source réseau
ms.assetid: bffc33ec-0fb0-4bbe-9bac-583b9d4e1153
title: Authentification de la source réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09c38968fccf501f49ac7666a066b88528b237bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104034157"
---
# <a name="network-source-authentication"></a><span data-ttu-id="b56d8-103">Authentification de la source réseau</span><span class="sxs-lookup"><span data-stu-id="b56d8-103">Network Source Authentication</span></span>

<span data-ttu-id="b56d8-104">Certains hôtes de média peuvent nécessiter des informations d’identification de l’utilisateur des applications clientes avant d’autoriser l’accès au média.</span><span class="sxs-lookup"><span data-stu-id="b56d8-104">Certain media hosts may require user credentials from client applications before allowing access to the media.</span></span> <span data-ttu-id="b56d8-105">Les informations d’identification de l’utilisateur incluent l’identification et la preuve d’identification, telles que le nom d’utilisateur et le mot de passe, qui sont utilisées par le serveur multimédia pour accorder l’accès à la source réseau qu’il héberge.</span><span class="sxs-lookup"><span data-stu-id="b56d8-105">User credentials include identification and proof of identification, such as user name and password, which are used by the media server to grant access to the network source it hosts.</span></span> <span data-ttu-id="b56d8-106">La source réseau peut fournir une authentification NTLM, Digest ou de base.</span><span class="sxs-lookup"><span data-stu-id="b56d8-106">The network source can provide NTLM, Digest, or Basic authentication.</span></span>

<span data-ttu-id="b56d8-107">Les applications basées sur Media Foundation peuvent stocker les informations d’identification de l’utilisateur pour une URL spécifique dans un objet *d’informations d’identification* qui expose l’interface [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) .</span><span class="sxs-lookup"><span data-stu-id="b56d8-107">Applications based on Media Foundation can store user credentials for a specific URL in a *credential* object that exposes the [**IMFNetCredential**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredential) interface.</span></span> <span data-ttu-id="b56d8-108">L’objet Credential stocke les informations d’identification chiffrées et fournit des méthodes pour retourner des informations telles que le nom d’utilisateur, le mot de passe et le domaine.</span><span class="sxs-lookup"><span data-stu-id="b56d8-108">The credential object stores encrypted credentials and provides methods to return information such as user name, password, and domain.</span></span>

<span data-ttu-id="b56d8-109">Les objets d’informations d’identification sont créés et conservés dans un cache.</span><span class="sxs-lookup"><span data-stu-id="b56d8-109">The credential objects are created and maintained in a cache.</span></span> <span data-ttu-id="b56d8-110">L’objet de *cache des informations d’identification* , exposé par l’interface [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) fournit des méthodes pour récupérer les objets d’informations d’identification à partir du cache des informations d’identification.</span><span class="sxs-lookup"><span data-stu-id="b56d8-110">The *credential cache* object, exposed by the [**IMFNetCredentialCache**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialcache) interface provides methods for retrieving the credential objects from the credential cache.</span></span>

<span data-ttu-id="b56d8-111">Une application qui prend en charge l’authentification doit implémenter l’interface [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) .</span><span class="sxs-lookup"><span data-stu-id="b56d8-111">An application that supports authentication must implement the [**IMFNetCredentialManager**](/windows/desktop/api/mfidl/nn-mfidl-imfnetcredentialmanager) interface.</span></span> <span data-ttu-id="b56d8-112">Media Foundation ne fournit pas d’implémentation par défaut de cette interface.</span><span class="sxs-lookup"><span data-stu-id="b56d8-112">Media Foundation does not provide a default implementation of this interface.</span></span> <span data-ttu-id="b56d8-113">Le gestionnaire d’informations d’identification est responsable de la collecte des informations d’identification requises pour une URL à partir de l’entrée de l’utilisateur ou de la lecture à partir du stockage persistant.</span><span class="sxs-lookup"><span data-stu-id="b56d8-113">The credential manager is responsible for gathering the required credentials for a URL from user input or reading from persisted storage.</span></span>

<span data-ttu-id="b56d8-114">Cette section contient les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="b56d8-114">This section contains the following topics:</span></span>

-   [<span data-ttu-id="b56d8-115">Définition d’un gestionnaire d’informations d’identification</span><span class="sxs-lookup"><span data-stu-id="b56d8-115">Setting a Credential Manager</span></span>](setting-a-credential-manager.md)
-   [<span data-ttu-id="b56d8-116">Utilisation du cache des informations d’identification</span><span class="sxs-lookup"><span data-stu-id="b56d8-116">Using the Credential Cache</span></span>](using-the-credential-cache.md)
-   [<span data-ttu-id="b56d8-117">Implémentation de IMFNetCredentialManager</span><span class="sxs-lookup"><span data-stu-id="b56d8-117">Implementing IMFNetCredentialManager</span></span>](implementing-imfnetcredentialmanager.md)

## <a name="related-topics"></a><span data-ttu-id="b56d8-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b56d8-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56d8-119">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b56d8-119">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



