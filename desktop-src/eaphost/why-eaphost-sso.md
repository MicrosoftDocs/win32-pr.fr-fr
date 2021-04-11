---
title: Vue d’ensemble du scénario EAPHost SSO
description: Contient deux scénarios qui illustrent les avantages d’un demandeur pour lequel l’authentification unique (SSO) est activée.
ms.assetid: 2a5cbcae-74fe-4241-9e20-ec1ec5d9ed8a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975310489758e299d1100584551296476c4690ca
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/26/2019
ms.locfileid: "104101125"
---
# <a name="sso-eaphost-scenario-overview"></a><span data-ttu-id="296fb-103">Vue d’ensemble du scénario EAPHost SSO</span><span class="sxs-lookup"><span data-stu-id="296fb-103">SSO EAPHost Scenario Overview</span></span>

<span data-ttu-id="296fb-104">La rubrique suivante contient deux scénarios qui illustrent les avantages d’un demandeur pour lequel l’authentification unique (SSO) est activée.</span><span class="sxs-lookup"><span data-stu-id="296fb-104">The following topic contains two scenarios that demonstrate the advantages of a Single-Sign-On (SSO) enabled supplicant.</span></span>

## <a name="about-the-scenarios"></a><span data-ttu-id="296fb-105">À propos des scénarios</span><span class="sxs-lookup"><span data-stu-id="296fb-105">About the Scenarios</span></span>

<span data-ttu-id="296fb-106">L’authentification unique fournit des fonctionnalités permettant de conserver des informations d’identification utilisateur supplémentaires qui sont habituellement stockées dans l’objet BLOB d’utilisateur EAP.</span><span class="sxs-lookup"><span data-stu-id="296fb-106">SSO provides functionality to retain additional user credential information than is traditionally stored in the EAP user BLOB.</span></span> <span data-ttu-id="296fb-107">Contrairement à d’autres processus d’informations d’identification, les demandeurs SSO peuvent résoudre les situations de connexion telles que l’itinérance AP et la modification du mot de passe sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296fb-107">Unlike other credential processes, SSO-enabled supplicants can resolve login situations like AP roaming, and password change without user intervention.</span></span>

## <a name="sso-eap-tls-pin-caching-behavior"></a><span data-ttu-id="296fb-108">Comportement de mise en cache du code confidentiel EAP-TLS SSO</span><span class="sxs-lookup"><span data-stu-id="296fb-108">SSO EAP-TLS PIN Caching Behavior</span></span>

<span data-ttu-id="296fb-109">Un demandeur peut tenter l’authentification réseau à l’aide d’une méthode EAP basée sur une carte à puce, telle que EAP-TLS (Extensible Authentication Protocol Transport Layer Security).</span><span class="sxs-lookup"><span data-stu-id="296fb-109">A supplicant can attempt network authentication using a smartcard-based EAP method such as Extensible Authentication Protocol Transport Layer Security (EAP-TLS).</span></span> <span data-ttu-id="296fb-110">Dans ce scénario et dans des scénarios similaires, le demandeur obtient le code confidentiel de la carte à puce auprès de l’utilisateur et récupère un certificat d’utilisateur pour l’authentification réseau, suivi d’un appel à WinLogin sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="296fb-110">In this and similar scenarios, the supplicant obtains the smartcard PIN from the user and retrieves a user certificate for network authentication followed by a call to WinLogin on the local computer.</span></span> <span data-ttu-id="296fb-111">Une fois l’authentification réussie, le demandeur met en cache l’objet BLOB de l’utilisateur et ne stocke pas les informations de code confidentiel utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296fb-111">After successful authentication the supplicant caches the user BLOB, and does not store user PIN information.</span></span>

<span data-ttu-id="296fb-112">Lorsque l’utilisateur se déplace vers un autre emplacement, la reprise de session et une nouvelle authentification doivent avoir lieu.</span><span class="sxs-lookup"><span data-stu-id="296fb-112">When the user roams to a different location session resumption and re-authentication must occur.</span></span> <span data-ttu-id="296fb-113">Étant donné que le certificat ne peut pas être stocké avant l’ouverture de session, l’authentification de l’utilisateur échoue et le demandeur vide l’objet BLOB de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296fb-113">Since the certificate cannot be stored pre-logon, the user authentication will fail and the supplicant flushes the user BLOB.</span></span> <span data-ttu-id="296fb-114">À ce stade, le code PIN de l’utilisateur est requis pour récupérer le certificat de l’utilisateur à partir de la carte à puce pour l’authentification réseau.</span><span class="sxs-lookup"><span data-stu-id="296fb-114">At this point the user PIN is required to retrieve the user certificate from the smartcard for network authentication.</span></span> <span data-ttu-id="296fb-115">Étant donné que l’authentification unique met en cache le code confidentiel, le certificat peut être récupéré sans intervention de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296fb-115">Because SSO caches the PIN, the certificate can be retrieved without user intervention.</span></span> <span data-ttu-id="296fb-116">Sans l’authentification unique, EAP-TLS devrait à nouveau déclencher une interface utilisateur de collection de codes confidentiels.</span><span class="sxs-lookup"><span data-stu-id="296fb-116">Without SSO, EAP-TLS would have to raise a PIN collection UI again.</span></span>

<span data-ttu-id="296fb-117">Pour une approche étape par étape, consultez la page [comportement de la mise en cache du code confidentiel EAP-TLS](sso-eap-tls-pin-caching-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="296fb-117">For a step-by-step approach, see [SSO EAP-TLS PIN Caching Behavior](sso-eap-tls-pin-caching-behavior-.md).</span></span>

## <a name="sso-password-change-behavior"></a><span data-ttu-id="296fb-118">Comportement de modification du mot de passe SSO</span><span class="sxs-lookup"><span data-stu-id="296fb-118">SSO Password Change Behavior</span></span>

<span data-ttu-id="296fb-119">Un demandeur peut tenter une authentification réseau à l’aide d’une méthode EAP basée sur un mot de passe telle que MS-CHAPv2 (Microsoft Challenge Handshake Authentication Protocol version 2,0), configurée pour utiliser les informations d’identification WinLogin.</span><span class="sxs-lookup"><span data-stu-id="296fb-119">A supplicant can attempt network authentication using a password-based EAP method such as Microsoft Challenge Handshake Authentication Protocol version 2.0 (MS-CHAPv2), configured to use WinLogin credentials.</span></span> <span data-ttu-id="296fb-120">Dans ce scénario, le demandeur collecte les informations d’identification de l’utilisateur une seule fois et les fournit à EAPHost pour l’authentification réseau.</span><span class="sxs-lookup"><span data-stu-id="296fb-120">In this scenario, the supplicant collects user credentials once and provides them to EAPHost for network authentication.</span></span> <span data-ttu-id="296fb-121">Une fois l’authentification réseau réussie, le demandeur utilise le même ensemble d’informations d’identification pour WinLogin.</span><span class="sxs-lookup"><span data-stu-id="296fb-121">After successful network authentication the supplicant uses the same set of credentials for WinLogin.</span></span>

<span data-ttu-id="296fb-122">Toutefois, si des informations d’identification telles que le mot de passe de l’utilisateur ont été modifiées pendant l’authentification réseau sans demandeur SSO, l’appel WinLogin suivant entraîne un échec.</span><span class="sxs-lookup"><span data-stu-id="296fb-122">However, if credentials such as the user password were changed during network authentication without an SSO-enabled supplicant, the subsequent WinLogin call will result in failure.</span></span> <span data-ttu-id="296fb-123">L’authentification unique conserve les nouvelles informations d’identification et autorise un WinLogin sans intervention supplémentaire de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="296fb-123">SSO retains the new credentials and allows a successful WinLogin without additional user intervention.</span></span>

<span data-ttu-id="296fb-124">Pour une approche pas à pas, consultez comportement de [modification du mot de passe SSO](sso-password-change-behavior-.md).</span><span class="sxs-lookup"><span data-stu-id="296fb-124">For a step-by-step approach, see [SSO Password Change Behavior](sso-password-change-behavior-.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="296fb-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="296fb-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="296fb-126">SSO et PLAP</span><span class="sxs-lookup"><span data-stu-id="296fb-126">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

 




