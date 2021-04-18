---
title: CSecureChannelClient, classe
description: CSecureChannelClient, classe
ms.assetid: f02220b8-0d1c-416c-97ea-e5e7455fcbba
keywords:
- Gestionnaire de périphériques Windows Media, classe CSecureChannelClient
- Gestionnaire de périphériques, classe CSecureChannelClient
- applications de bureau, classe CSecureChannelClient
- Référence de programmation, classe CSecureChannelClient
- référence pour Windows Media Gestionnaire de périphériques, classe CSecureChannelClient
- CSecureChannelClient, classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59a886ba45648b2ba0356e9d7f246c2de912cedd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512319"
---
# <a name="csecurechannelclient-class"></a><span data-ttu-id="f79be-109">CSecureChannelClient, classe</span><span class="sxs-lookup"><span data-stu-id="f79be-109">CSecureChannelClient Class</span></span>

<span data-ttu-id="f79be-110">La classe **CSecureChannelClient** est une classe d’assistance (et non une interface) qui permet aux applications de s’authentifier, de chiffrer et de déchiffrer des données et de créer des Mac.</span><span class="sxs-lookup"><span data-stu-id="f79be-110">The **CSecureChannelClient** class is a helper class (not an interface) that enables applications to authenticate themselves, encrypt and decrypt data, and create MACs.</span></span>

<span data-ttu-id="f79be-111">La classe **CSecureChannelClient** expose les méthodes suivantes.</span><span class="sxs-lookup"><span data-stu-id="f79be-111">The **CSecureChannelClient** class exposes the following methods.</span></span>



| <span data-ttu-id="f79be-112">Méthode</span><span class="sxs-lookup"><span data-stu-id="f79be-112">Method</span></span>                                                            | <span data-ttu-id="f79be-113">Description</span><span class="sxs-lookup"><span data-stu-id="f79be-113">Description</span></span>                                                                                                               |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f79be-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f79be-114">[**Authenticate**](/previous-versions/ms983906(v=msdn.10))</span></span>         | <span data-ttu-id="f79be-115">Déclenche l’échange de certificats entre les composants pour établir l’approbation.</span><span class="sxs-lookup"><span data-stu-id="f79be-115">Triggers the exchange of certificates between components to establish trust.</span></span>                                              |
| <span data-ttu-id="f79be-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-116">[**DecryptParam**](/previous-versions/bb231586(v=vs.85))</span></span>         | <span data-ttu-id="f79be-117">Déchiffre les données reçues par le biais d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f79be-117">Decrypts data received through a parameter.</span></span>                                                                               |
| <span data-ttu-id="f79be-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-118">[**EncryptParam**](/previous-versions/bb231587(v=vs.85))</span></span>         | <span data-ttu-id="f79be-119">Chiffre les données envoyées par le biais d’un paramètre.</span><span class="sxs-lookup"><span data-stu-id="f79be-119">Encrypts data being sent out through a parameter.</span></span>                                                                         |
| <span data-ttu-id="f79be-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f79be-120">[**fIsAuthenticated**](/previous-versions/ms868497(v=msdn.10))</span></span> | <span data-ttu-id="f79be-121">Vérifie qu’un canal d’authentification sécurisé a été établi avec succès.</span><span class="sxs-lookup"><span data-stu-id="f79be-121">Verifies that a secure authentication channel has been successfully established.</span></span> <span data-ttu-id="f79be-122">Cette méthode n’est pas utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="f79be-122">This method is not used by applications.</span></span> |
| <span data-ttu-id="f79be-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f79be-123">[**GetAppSec**](/previous-versions/ms868498(v=msdn.10))</span></span>               | <span data-ttu-id="f79be-124">Récupère les niveaux de sécurité de l’application des composants locaux et distants.</span><span class="sxs-lookup"><span data-stu-id="f79be-124">Retrieves the application security levels of the local and remote components.</span></span>                                             |
| <span data-ttu-id="f79be-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-125">[**GetSessionKey**](/previous-versions/bb231590(v=vs.85))</span></span>       | <span data-ttu-id="f79be-126">Récupère la clé de session active.</span><span class="sxs-lookup"><span data-stu-id="f79be-126">Retrieves the current session key.</span></span> <span data-ttu-id="f79be-127">Cette méthode n’est pas utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="f79be-127">This method is not used by applications.</span></span>                                               |
| <span data-ttu-id="f79be-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-128">[**MACFinal**](/previous-versions/bb231591(v=vs.85))</span></span>                 | <span data-ttu-id="f79be-129">Libère le canal de code d’authentification de message (MAC) et récupère une valeur MAC finale.</span><span class="sxs-lookup"><span data-stu-id="f79be-129">Releases the message authentication code (MAC) channel and retrieves a final MAC value.</span></span>                                   |
| <span data-ttu-id="f79be-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-130">[**MACInit**](/previous-versions/bb231592(v=vs.85))</span></span>                   | <span data-ttu-id="f79be-131">Acquiert un canal MAC (Message Authentication Code).</span><span class="sxs-lookup"><span data-stu-id="f79be-131">Acquires a message authentication code (MAC) channel.</span></span>                                                                     |
| <span data-ttu-id="f79be-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-132">[**MACUpdate**](/previous-versions/bb231593(v=vs.85))</span></span>               | <span data-ttu-id="f79be-133">Ajoute une valeur à un code d’authentification de message (MAC).</span><span class="sxs-lookup"><span data-stu-id="f79be-133">Adds a value to a message authentication code (MAC).</span></span>                                                                      |
| <span data-ttu-id="f79be-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f79be-134">[**SetCertificate**](/previous-versions/ms868504(v=msdn.10))</span></span>     | <span data-ttu-id="f79be-135">Spécifie le certificat et la clé privée du client de canal authentifié (SAC) sécurisé.</span><span class="sxs-lookup"><span data-stu-id="f79be-135">Specifies the certificate and private key of the secure authenticated channel (SAC) client.</span></span>                               |
| <span data-ttu-id="f79be-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f79be-136">[**SetInterface**](/previous-versions/bb231595(v=vs.85))</span></span>         | <span data-ttu-id="f79be-137">Sélectionne l’interface utilisée pour sécuriser les communications de canal authentifié (SAC).</span><span class="sxs-lookup"><span data-stu-id="f79be-137">Selects the interface used for secure authenticated channel (SAC) communications.</span></span>                                         |
| <span data-ttu-id="f79be-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f79be-138">[**SetSessionKey**](/previous-versions/ms868506(v=msdn.10))</span></span>       | <span data-ttu-id="f79be-139">Définit la clé de session utilisée pour communiquer avec un autre composant.</span><span class="sxs-lookup"><span data-stu-id="f79be-139">Sets the session key that is used to communicate with another component.</span></span> <span data-ttu-id="f79be-140">Cette méthode n’est pas utilisée par les applications.</span><span class="sxs-lookup"><span data-stu-id="f79be-140">This method is not used by applications.</span></span>         |



 

## <a name="related-topics"></a><span data-ttu-id="f79be-141">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f79be-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f79be-142">**CSecureChannelServer, classe**</span><span class="sxs-lookup"><span data-stu-id="f79be-142">**CSecureChannelServer Class**</span></span>](csecurechannelserver-class.md)
</dt> <dt>

[<span data-ttu-id="f79be-143">**Interface IComponentAuthenticate**</span><span class="sxs-lookup"><span data-stu-id="f79be-143">**IComponentAuthenticate Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-icomponentauthenticate)
</dt> <dt>

[<span data-ttu-id="f79be-144">**Interfaces pour les applications**</span><span class="sxs-lookup"><span data-stu-id="f79be-144">**Interfaces for Applications**</span></span>](interfaces-for-applications.md)
</dt> </dl>

 

 