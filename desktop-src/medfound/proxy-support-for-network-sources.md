---
description: Prise en charge du proxy pour les sources réseau
ms.assetid: e739746d-2a09-4237-a7c1-0aed4e4516d7
title: Prise en charge du proxy pour les sources réseau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97bc1172c072a54f9f76cbcd3a297a972efbde29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519582"
---
# <a name="proxy-support-for-network-sources"></a><span data-ttu-id="20ada-103">Prise en charge du proxy pour les sources réseau</span><span class="sxs-lookup"><span data-stu-id="20ada-103">Proxy Support for Network Sources</span></span>

<span data-ttu-id="20ada-104">Un serveur proxy est un serveur intermédiaire entre votre intranet et Internet, qui achemine les demandes de l’application cliente vers le serveur multimédia et récupère les fichiers à partir du serveur multimédia.</span><span class="sxs-lookup"><span data-stu-id="20ada-104">A proxy server is an intermediate server between your intranet and the Internet, which routes requests from the client application to the media server and retrieves files from the media server.</span></span>

<span data-ttu-id="20ada-105">Media Foundation crée implicitement un objet *localisateur de proxy* quand une application cliente tente d’accéder à une URL source.</span><span class="sxs-lookup"><span data-stu-id="20ada-105">Media Foundation implicitly creates a *proxy locator* object when a client application tries to access a source URL.</span></span> <span data-ttu-id="20ada-106">L’objet localisateur de proxy expose l’interface [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) .</span><span class="sxs-lookup"><span data-stu-id="20ada-106">The proxy locator object exposes the [**IMFNetProxyLocator**](/windows/desktop/api/mfidl/nn-mfidl-imfnetproxylocator) interface.</span></span> <span data-ttu-id="20ada-107">Pendant la résolution de la source, Media Foundation vérifie la Banque de propriétés transmise à la méthode du programme de résolution source.</span><span class="sxs-lookup"><span data-stu-id="20ada-107">During source resolution, Media Foundation checks the property store passed to the source resolver method.</span></span>

<span data-ttu-id="20ada-108">Si la Banque de propriétés contient la propriété [MFNETSOURCE \_ PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) définie sur un objet de fabrique du localisateur de proxy implémenté par l’application, elle appelle la méthode [**IMFNetProxyLocatorFactory :: CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) pour créer un localisateur de proxy avec des paramètres de configuration personnalisés.</span><span class="sxs-lookup"><span data-stu-id="20ada-108">If the property store contains the [MFNETSOURCE\_PROXYLOCATORFACTORY](mfnetsource-proxylocatorfactory-property.md) property set to a proxy locator factory object implemented by the application then, it invokes the [**IMFNetProxyLocatorFactory::CreateProxyLocator**](/windows/desktop/api/mfidl/nf-mfidl-imfnetproxylocatorfactory-createproxylocator) method to create a proxy locator with custom configuration settings.</span></span>

<span data-ttu-id="20ada-109">Si la Banque de propriétés n’est pas définie, Media Foundation crée le localisateur de proxy avec la configuration par défaut.</span><span class="sxs-lookup"><span data-stu-id="20ada-109">If the property store is not set, then Media Foundation creates the proxy locator with default configuration.</span></span> <span data-ttu-id="20ada-110">Ces paramètres sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="20ada-110">These settings are as follows:</span></span>

-   <span data-ttu-id="20ada-111">Si la stratégie de l’utilisateur est définie, le localisateur de proxy utilise les paramètres spécifiés dans le registre.</span><span class="sxs-lookup"><span data-stu-id="20ada-111">If user policy is set, then the proxy locator uses settings specified in the registry.</span></span>

-   <span data-ttu-id="20ada-112">Pour HTTP, le localisateur de proxy utilise les paramètres du proxy du navigateur.</span><span class="sxs-lookup"><span data-stu-id="20ada-112">For HTTP, the proxy locator uses browser proxy settings.</span></span>

-   <span data-ttu-id="20ada-113">Pour RTSP, le localisateur de proxy est configuré pour ignorer les serveurs proxy lors de la connexion au serveur multimédia.</span><span class="sxs-lookup"><span data-stu-id="20ada-113">For RTSP, the proxy locator is configured to bypass proxy servers when connecting to the media server.</span></span>

<span data-ttu-id="20ada-114">Cette configuration par défaut peut être modifiée par l’application.</span><span class="sxs-lookup"><span data-stu-id="20ada-114">This default configuration can be changed by the application.</span></span> <span data-ttu-id="20ada-115">Les rubriques suivantes contiennent des informations sur les paramètres de configuration d’un localisateur de proxy :</span><span class="sxs-lookup"><span data-stu-id="20ada-115">The following topics contain information about the configuration settings for a proxy locator:</span></span>

-   [<span data-ttu-id="20ada-116">Paramètres de configuration du localisateur de proxy</span><span class="sxs-lookup"><span data-stu-id="20ada-116">Proxy Locator Configuration Settings</span></span>](proxy-locator-configuration-settings.md)

-   [<span data-ttu-id="20ada-117">Comment configurer le localisateur de proxy</span><span class="sxs-lookup"><span data-stu-id="20ada-117">How to Configure the Proxy Locator</span></span>](how-to-configure-the-proxy-locator.md)

<span data-ttu-id="20ada-118">Media Foundation Initialise le localisateur de proxy pour l’URL source spécifiée pour le programme de [résolution source](source-resolver.md).</span><span class="sxs-lookup"><span data-stu-id="20ada-118">Media Foundation initializes the proxy locator for the source URL specified to the [Source Resolver](source-resolver.md).</span></span> <span data-ttu-id="20ada-119">Le localisateur de proxy détecte un serveur proxy à utiliser en fonction des paramètres de configuration.</span><span class="sxs-lookup"><span data-stu-id="20ada-119">The proxy locator detects a proxy server to use based on configuration settings.</span></span> <span data-ttu-id="20ada-120">Lorsque le localisateur de proxy tente de définir un serveur proxy, il enregistre le résultat de la réussite ou de l’échec dans le registre.</span><span class="sxs-lookup"><span data-stu-id="20ada-120">When the proxy locator attempts the set a proxy server, it records the success or failure result in the registry.</span></span> <span data-ttu-id="20ada-121">Cette valeur est vérifiée lors du prochain processus de détection de proxy.</span><span class="sxs-lookup"><span data-stu-id="20ada-121">This value is checked during the next proxy detection process.</span></span> <span data-ttu-id="20ada-122">Si un certain serveur proxy est connu pour avoir provoqué des échecs par le passé, le localisateur de proxy l’ignore.</span><span class="sxs-lookup"><span data-stu-id="20ada-122">If a certain proxy server is known to have caused failures in the past, the proxy locator skips it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="20ada-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="20ada-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20ada-124">Attributs et propriétés</span><span class="sxs-lookup"><span data-stu-id="20ada-124">Attributes and Properties</span></span>](attributes-and-properties.md)
</dt> <dt>

[<span data-ttu-id="20ada-125">Mise en réseau dans Media Foundation</span><span class="sxs-lookup"><span data-stu-id="20ada-125">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 



