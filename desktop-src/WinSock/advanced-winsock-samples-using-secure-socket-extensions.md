---
description: Exemples de Winsock avancés utilisant Secure Socket extensions
ms.assetid: 9c429363-f9bb-4394-89be-f87507f5cbdd
title: Exemples de Winsock avancés utilisant Secure Socket extensions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6701809ad97c7d39acf1f0eae646e7555e5c967f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951179"
---
# <a name="advanced-winsock-samples-using-secure-socket-extensions"></a><span data-ttu-id="db802-103">Exemples de Winsock avancés utilisant Secure Socket extensions</span><span class="sxs-lookup"><span data-stu-id="db802-103">Advanced Winsock Samples Using Secure Socket Extensions</span></span>

## <a name="secure-tcp-client-and-server-sample"></a><span data-ttu-id="db802-104">Exemple de serveur et de client TCP sécurisé</span><span class="sxs-lookup"><span data-stu-id="db802-104">Secure TCP Client and Server Sample</span></span>

<span data-ttu-id="db802-105">Un exemple Winsock plus avancé qui illustre l’utilisation d’extensions de sockets sécurisées est inclus dans le kit de développement logiciel (SDK) Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="db802-105">A more advanced Winsock sample that demonstrates the use of secure socket extensions is included with the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="db802-106">L’exemple comprend un client et un serveur TCP qui se connectent en toute sécurité à l’aide de Winsock et des extensions de socket sécurisé.</span><span class="sxs-lookup"><span data-stu-id="db802-106">The sample includes a TCP client and server that connect securely using the Winsock and the secure socket extensions.</span></span>

<span data-ttu-id="db802-107">Par défaut, le code source de l’exemple Winsock est installé dans le répertoire suivant :</span><span class="sxs-lookup"><span data-stu-id="db802-107">By default, the Winsock sample source code is installed in the following directory:</span></span>

<span data-ttu-id="db802-108">*C : \\ Program Files \\ Microsoft SDK \\ \\ exemples Windows v \\ 6.0 \\ NetDs \\ Winsock*</span><span class="sxs-lookup"><span data-stu-id="db802-108">*C:\\Program Files\\Microsoft SDKs\\Windows\\v6.0\\Samples\\NetDs\\winsock*</span></span>

<span data-ttu-id="db802-109">Un exemple se trouve dans le dossier suivant :</span><span class="sxs-lookup"><span data-stu-id="db802-109">A sample is located under the following folder:</span></span>

<span data-ttu-id="db802-110">*securesocket*</span><span class="sxs-lookup"><span data-stu-id="db802-110">*securesocket*</span></span>

<span data-ttu-id="db802-111">L’exemple de code est divisé en plusieurs répertoires, comme décrit ci-dessous :</span><span class="sxs-lookup"><span data-stu-id="db802-111">The sample code is split into separate directories as described below:</span></span>

-   <span data-ttu-id="db802-112">stcpclient : le dossier qui contient le code client TCP sécurisé.</span><span class="sxs-lookup"><span data-stu-id="db802-112">stcpclient - the folder that contains the secure TCP client code.</span></span>
-   <span data-ttu-id="db802-113">stcpcommon : le dossier qui contient le code de bibliothèque commun qui est partagé entre le client et le serveur TCP sécurisés.</span><span class="sxs-lookup"><span data-stu-id="db802-113">stcpcommon - the folder that contains common library code that is shared between the secure TCP client and server.</span></span>
-   <span data-ttu-id="db802-114">stcpserver : le dossier qui contient le code du serveur TCP sécurisé.</span><span class="sxs-lookup"><span data-stu-id="db802-114">stcpserver - the folder that contains the secure TCP server code.</span></span>

<span data-ttu-id="db802-115">Notez que les exemples sont censés être exécutés sur deux ordinateurs différents exécutant Windows Vista ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="db802-115">It should be noted that the samples are meant to be run on two different computers running Windows Vista or later.</span></span> <span data-ttu-id="db802-116">En outre, les informations d’identification IPsec doivent être approvisionnées sur les deux ordinateurs pour que la connexion aboutisse, car l’exemple utilise IPsec pour sécuriser son trafic.</span><span class="sxs-lookup"><span data-stu-id="db802-116">Additionally, IPsec credentials must be provisioned on both the computers for the connection to succeed, because the sample uses IPsec for securing its traffic.</span></span> <span data-ttu-id="db802-117">Pour plus d’informations sur la configuration des informations d’identification IPsec, reportez-vous à la documentation relative à la [configuration IPSec](/windows/desktop/FWP/ipsec-configuration) .</span><span class="sxs-lookup"><span data-stu-id="db802-117">Please refer to the documentation on [IPsec Configuration](/windows/desktop/FWP/ipsec-configuration) for more information on setting up IPsec credentials.</span></span>

<span data-ttu-id="db802-118">La génération de l’exemple génère deux fichiers exécutables :</span><span class="sxs-lookup"><span data-stu-id="db802-118">Building the sample will generate two executable files:</span></span>

<span data-ttu-id="db802-119">*stcpclient.exe* et *stcpserver.exe*.</span><span class="sxs-lookup"><span data-stu-id="db802-119">*stcpclient.exe* and *stcpserver.exe*.</span></span>

<span data-ttu-id="db802-120">Copiez *stcpclient.exe* sur l’ordinateur A et copiez *stcpserver.exe* sur l’ordinateur B. Sur l’ordinateur B, démarrez le serveur TCP en exécutant la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="db802-120">Copy *stcpclient.exe* to computer A and copy *stcpserver.exe* to computer B. On computer B, start the TCP server by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="db802-121">**stcpserver.exe**</span><span class="sxs-lookup"><span data-stu-id="db802-121">**stcpserver.exe**</span></span>

<span data-ttu-id="db802-122">Exécutez la commande suivante pour obtenir d’autres options d’utilisation pour le serveur :</span><span class="sxs-lookup"><span data-stu-id="db802-122">Execute the following command for more usage options for the server:</span></span>

<span data-ttu-id="db802-123">**stcpserver.exe/ ?**</span><span class="sxs-lookup"><span data-stu-id="db802-123">**stcpserver.exe /?**</span></span>

<span data-ttu-id="db802-124">Ensuite, sur l’ordinateur A, démarrez le client TCP en exécutant la commande suivante dans une invite de commandes :</span><span class="sxs-lookup"><span data-stu-id="db802-124">Then on computer A, start the TCP client by executing the following in a Command Prompt:</span></span>

<span data-ttu-id="db802-125">**stcpclient.exe <nom complet DNS-for-machine-B>**</span><span class="sxs-lookup"><span data-stu-id="db802-125">**stcpclient.exe <fully-qualified-DNS-name-for-machine-B>**</span></span>

<span data-ttu-id="db802-126">À ce stade, la connexion doit être établie en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="db802-126">At this point the connection should get established securely.</span></span>

<span data-ttu-id="db802-127">Pour plus d’options d’utilisation pour le client, exécutez la commande suivante :</span><span class="sxs-lookup"><span data-stu-id="db802-127">Execute the following command for more usage options for the client:</span></span>

<span data-ttu-id="db802-128">**stcpclient.exe/ ?**</span><span class="sxs-lookup"><span data-stu-id="db802-128">**stcpclient.exe /?**</span></span>

## <a name="related-topics"></a><span data-ttu-id="db802-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db802-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db802-130">À propos de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="db802-130">About Windows Filtering Platform</span></span>](/windows/desktop/FWP/about-windows-filtering-platform)
</dt> <dt>

[<span data-ttu-id="db802-131">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="db802-131">Application Layer Enforcement (ALE)</span></span>](/windows/desktop/FWP/application-layer-enforcement--ale-)
</dt> <dt>

[<span data-ttu-id="db802-132">Configuration IPsec</span><span class="sxs-lookup"><span data-stu-id="db802-132">IPsec Configuration</span></span>](/windows/desktop/FWP/ipsec-configuration)
</dt> <dt>

[<span data-ttu-id="db802-133">Fonctions IPsec</span><span class="sxs-lookup"><span data-stu-id="db802-133">IPsec Functions</span></span>](/windows/desktop/FWP/fwp-ipsec-functions)
</dt> <dt>

[<span data-ttu-id="db802-134">Utilisation des extensions de socket sécurisé</span><span class="sxs-lookup"><span data-stu-id="db802-134">Using Secure Socket Extensions</span></span>](using-secure-socket-extensions.md)
</dt> <dt>

[<span data-ttu-id="db802-135">interface du fournisseur de la prise en charge de la sécurité (Security Support Provider Interface ou SSPI)</span><span class="sxs-lookup"><span data-stu-id="db802-135">Security Support Provider Interface (SSPI)</span></span>](/windows/desktop/Rpc/security-support-provider-interface-sspi-)
</dt> <dt>

[<span data-ttu-id="db802-136">Plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="db802-136">Windows Filtering Platform</span></span>](/windows/desktop/FWP/windows-filtering-platform-start-page)
</dt> <dt>

[<span data-ttu-id="db802-137">Fonctions de l’API de la plateforme de filtrage Windows</span><span class="sxs-lookup"><span data-stu-id="db802-137">Windows Filtering Platform API Functions</span></span>](/windows/desktop/FWP/fwp-functions)
</dt> <dt>

[<span data-ttu-id="db802-138">Extensions Winsock Secure Socket</span><span class="sxs-lookup"><span data-stu-id="db802-138">Winsock Secure Socket Extensions</span></span>](winsock-secure-socket-extensions.md)
</dt> </dl>

 

 
