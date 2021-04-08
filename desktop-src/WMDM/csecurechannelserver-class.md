---
title: CSecureChannelServer, classe
description: CSecureChannelServer, classe
ms.assetid: e6e1463a-5a26-4b83-85e0-a639d384a199
keywords:
- Gestionnaire de périphériques Windows Media, classe CSecureChannelServer
- Gestionnaire de périphériques, classe CSecureChannelServer
- fournisseurs de services, classe CSecureChannelServer
- Référence de programmation, classe CSecureChannelServer
- référence pour Windows Media Gestionnaire de périphériques, classe CSecureChannelServer
- CSecureChannelServer, classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99efdd4d4fa245000d27b5874439375d968591e5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727877"
---
# <a name="csecurechannelserver-class"></a><span data-ttu-id="1d0cc-109">CSecureChannelServer, classe</span><span class="sxs-lookup"><span data-stu-id="1d0cc-109">CSecureChannelServer Class</span></span>

<span data-ttu-id="1d0cc-110">La classe **CSecureChannelServer** est une classe d’assistance (pas une interface) qui permet à un fournisseur de services ou à un fournisseur de contenu sécurisé d’authentifier une application à l’aide de l’interface [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) , de chiffrer et de déchiffrer des données et de créer des signatures Mac.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-110">The **CSecureChannelServer** class is a helper class (not an interface) that enables a service provider or secure content provider to authenticate an application using the [**IComponentAuthenticate**](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate) interface, to encrypt and decrypt data, and to create MAC signatures.</span></span> <span data-ttu-id="1d0cc-111">Le processus d’authentification nécessite que l’application crée un objet **CSecureChannelClient** et que le fournisseur de services crée un objet **CSecureChannelServer** .</span><span class="sxs-lookup"><span data-stu-id="1d0cc-111">The authentication process requires that the application create a **CSecureChannelClient** object and that the service provider create a **CSecureChannelServer** object.</span></span> <span data-ttu-id="1d0cc-112">Les classes **CSecureChannelClient** et **CSecureChannelServer** sont déclarées dans la bibliothèque de liens statiques, Mssachlp. lib.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-112">The **CSecureChannelClient** and **CSecureChannelServer** classes are declared in the static link library, Mssachlp.lib.</span></span> <span data-ttu-id="1d0cc-113">Toutes les méthodes des interfaces du fournisseur de Gestionnaire de périphériques, du fournisseur de services et du fournisseur de contenu sécurisé de Windows Media peuvent retourner WMDM \_ E \_ NOTCERTIFIED pour indiquer que l’appelant ne s’est pas correctement authentifié.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-113">All methods of Windows Media Device Manager, service provider, and secure content provider interfaces can return WMDM\_E\_NOTCERTIFIED to indicate that the caller has not authenticated successfully.</span></span>

<span data-ttu-id="1d0cc-114">La classe **CSecureChannelServer** expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-114">The **CSecureChannelServer** class exposes the following methods.</span></span>



| <span data-ttu-id="1d0cc-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="1d0cc-115">Method</span></span>                                                            | <span data-ttu-id="1d0cc-116">Description</span><span class="sxs-lookup"><span data-stu-id="1d0cc-116">Description</span></span>                                                                                 |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d0cc-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-117">[**DecryptParam**](/previous-versions/bb231598(v=vs.85))</span></span>         | <span data-ttu-id="1d0cc-118">Déchiffre les données contenues dans un paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-118">Decrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="1d0cc-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-119">[**EncryptParam**](/previous-versions/ms868509(v=msdn.10))</span></span>         | <span data-ttu-id="1d0cc-120">Chiffre les données contenues dans un paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-120">Encrypts the data contained in a parameter.</span></span>                                                 |
| <span data-ttu-id="1d0cc-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-121">[**fIsAuthenticated**](/previous-versions/bb231600(v=vs.85))</span></span> | <span data-ttu-id="1d0cc-122">Vérifie qu’un canal d’authentification sécurisé a été établi avec succès.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-122">Verifies that a secure authentication channel has been successfully established.</span></span>            |
| <span data-ttu-id="1d0cc-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-123">[**GetAppSec**](/previous-versions/bb231601(v=vs.85))</span></span>               | <span data-ttu-id="1d0cc-124">Récupère les niveaux de sécurité de l’application des composants locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-124">Retrieves the application security levels of the local and remote components.</span></span>               |
| <span data-ttu-id="1d0cc-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-125">[**GetSessionKey**](/previous-versions/bb231602(v=vs.85))</span></span>       | <span data-ttu-id="1d0cc-126">Récupère la clé de session active.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-126">Retrieves the current session key.</span></span>                                                          |
| <span data-ttu-id="1d0cc-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-127">[**MACFinal**](/previous-versions/ms868513(v=msdn.10))</span></span>                 | <span data-ttu-id="1d0cc-128">Libère le canal de code d’authentification de message (MAC) et récupère une valeur MAC finale.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-128">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>     |
| <span data-ttu-id="1d0cc-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-129">[**MACInit**](/previous-versions/ms868514(v=msdn.10))</span></span>                   | <span data-ttu-id="1d0cc-130">Acquiert un canal MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="1d0cc-130">Acquires a message authentication code (MAC) channel.</span></span>                                       |
| <span data-ttu-id="1d0cc-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-131">[**MACUpdate**](/previous-versions/ms868515(v=msdn.10))</span></span>               | <span data-ttu-id="1d0cc-132">Met à jour la valeur du code d’authentification de message (MAC) avec une valeur de paramètre.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-132">Updates the message authentication code (MAC) value with a parameter value.</span></span>                 |
| <span data-ttu-id="1d0cc-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-133">[**SACAuth**](/previous-versions/ms868516(v=msdn.10))</span></span>                   | <span data-ttu-id="1d0cc-134">Établit un canal authentifié sécurisé entre les composants.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-134">Establishes a secure authenticated channel between components.</span></span>                              |
| <span data-ttu-id="1d0cc-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-135">[**SACGetProtocols**](/previous-versions/ms868517(v=msdn.10))</span></span>   | <span data-ttu-id="1d0cc-136">Signale les protocoles pris en charge par un composant.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-136">Reports the protocols supported by a component.</span></span>                                             |
| <span data-ttu-id="1d0cc-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-137">[**SetCertificate**](/previous-versions/ms868518(v=msdn.10))</span></span>     | <span data-ttu-id="1d0cc-138">Spécifie le certificat et la clé privée du serveur de canal authentifié (SAC) sécurisé.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-138">Specifies the certificate and private key of the secure authenticated channel (SAC) server.</span></span> |
| <span data-ttu-id="1d0cc-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="1d0cc-139">[**SetSessionKey**](/previous-versions/ms868519(v=msdn.10))</span></span>       | <span data-ttu-id="1d0cc-140">Définit la clé de session utilisée pour communiquer avec un autre composant.</span><span class="sxs-lookup"><span data-stu-id="1d0cc-140">Sets the session key that is used to communicate with another component.</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="1d0cc-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d0cc-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d0cc-142">**CSecureChannelClient, classe**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-142">**CSecureChannelClient Class**</span></span>](csecurechannelclient-class.md)
</dt> <dt>

[<span data-ttu-id="1d0cc-143">**Interface IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="1d0cc-144">**Interfaces pour les fournisseurs de services**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-144">**Interfaces for Service Providers**</span></span>](interfaces-for-service-providers.md)
</dt> <dt>

[<span data-ttu-id="1d0cc-145">**Utilisation de canaux authentifiés sécurisés**</span><span class="sxs-lookup"><span data-stu-id="1d0cc-145">**Using Secure Authenticated Channels**</span></span>](using-secure-authenticated-channels.md)
</dt> </dl>

 

 