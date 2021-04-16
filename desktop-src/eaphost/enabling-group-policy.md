---
title: Activation de stratégie de groupe
description: Découvrez comment configurer le demandeur en activant la stratégie de groupe. Consultez éléments à prendre en considération pour les demandeurs et afficher les ressources disponibles supplémentaires.
ms.assetid: ac04b83b-1322-41d4-85e0-93687f10a7f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7b57e736bf078068156f6aff10d294621749a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382900"
---
# <a name="enabling-group-policy"></a><span data-ttu-id="45b1c-104">Activation de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="45b1c-104">Enabling Group Policy</span></span>

<span data-ttu-id="45b1c-105">Cette rubrique explique comment configurer le demandeur en activant la stratégie de groupe.</span><span class="sxs-lookup"><span data-stu-id="45b1c-105">This topic explains how to configure the supplicant by enabling group policy.</span></span> <span data-ttu-id="45b1c-106">Les demandeurs EAPHost peuvent participer à la stratégie de groupe pour permettre à un administrateur réseau de configurer de manière centralisée leurs ordinateurs réseau.</span><span class="sxs-lookup"><span data-stu-id="45b1c-106">EAPHost supplicants can participate in group policy to allow a network administrator to centrally configure their network machines.</span></span>

<span data-ttu-id="45b1c-107">La méthode et le mécanisme précis par lesquels le demandeur choisit de participer à la stratégie de groupe sont à la discrétion du demandeur.</span><span class="sxs-lookup"><span data-stu-id="45b1c-107">The precise method and mechanism by which the supplicant chooses to participate in group policy is at the discretion of the supplicant.</span></span> <span data-ttu-id="45b1c-108">Des exemples de mécanismes pour la participation à la stratégie de groupe incluent les extensions côté client/serveur, le modèle d’administration, etc.</span><span class="sxs-lookup"><span data-stu-id="45b1c-108">Examples of mechanisms for group policy participation include client/server-side extensions, administrative template, and so forth.</span></span>

## <a name="considerations-when-enabling-group-policy"></a><span data-ttu-id="45b1c-109">Considérations relatives à l’activation de stratégie de groupe</span><span class="sxs-lookup"><span data-stu-id="45b1c-109">Considerations When Enabling Group Policy</span></span>

<span data-ttu-id="45b1c-110">Voici les éléments à prendre en considération pour les demandeurs en ce qui concerne la stratégie de groupe et le protocole EAP.</span><span class="sxs-lookup"><span data-stu-id="45b1c-110">These are the considerations for supplicants with respect to group policy and EAP.</span></span>

1.  <span data-ttu-id="45b1c-111">La configuration EAP doit toujours être stockée au format XML chaque fois que cela est possible et pas au format binaire.</span><span class="sxs-lookup"><span data-stu-id="45b1c-111">EAP configuration should always be stored as XML whenever possible and not in the binary format.</span></span> <span data-ttu-id="45b1c-112">La stratégie de groupe peut être appliquée à n’importe quel ordinateur du domaine, et la configuration de la méthode EAP et les données utilisateur ne sont pas nécessairement portables entre les architectures de processeur 32 bits et 64 bits.</span><span class="sxs-lookup"><span data-stu-id="45b1c-112">Group policy may be applied to any machine in the domain, and EAP method configuration and user data are not guaranteed to be portable between 32-bit and 64-bit processor architectures.</span></span> <span data-ttu-id="45b1c-113">XML résout les problèmes de limite d’architecture de processeur, car le demandeur convertit localement le XML indépendant de l’architecture du processeur en représentation binaire de la configuration au moment de l’authentification.</span><span class="sxs-lookup"><span data-stu-id="45b1c-113">XML resolves the processor architecture boundary issues as the supplicant locally converts the processor-architecture independent XML to the binary representation of the configuration at authentication time.</span></span>

    <span data-ttu-id="45b1c-114">Pour plus d'informations, consultez les rubriques ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="45b1c-114">For more information, see the following topics.</span></span>

    -   [<span data-ttu-id="45b1c-115">Forum aux questions (FAQ)</span><span class="sxs-lookup"><span data-stu-id="45b1c-115">General Frequently Asked Questions</span></span>](general-frequently-asked-questions.md)
    -   <span data-ttu-id="45b1c-116">[Forum aux questions sur la méthode EAP](eap-method-frequently-asked-questions.md).</span><span class="sxs-lookup"><span data-stu-id="45b1c-116">[EAP Method Frequently Asked Questions](eap-method-frequently-asked-questions.md).</span></span>
    -   [<span data-ttu-id="45b1c-117">**EapHostPeerConfigXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="45b1c-117">**EapHostPeerConfigXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerconfigxml2blob)
    -   [<span data-ttu-id="45b1c-118">**EapHostPeerCredentialsXml2Blob**</span><span class="sxs-lookup"><span data-stu-id="45b1c-118">**EapHostPeerCredentialsXml2Blob**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeercredentialsxml2blob)

2.  <span data-ttu-id="45b1c-119">Si une extension côté serveur de la stratégie de groupe est utilisée, l’extension appelle généralement [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) pour déterminer les méthodes disponibles et pour générer la configuration EAP appropriée pour cette stratégie.</span><span class="sxs-lookup"><span data-stu-id="45b1c-119">If a group policy server-side extension is used, the extension will call [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) typically to determine available methods and to generate appropriate EAP configuration for that policy.</span></span> <span data-ttu-id="45b1c-120">La stratégie est ensuite envoyée aux clients réseau appropriés sur lesquels la stratégie est appliquée.</span><span class="sxs-lookup"><span data-stu-id="45b1c-120">The policy is then pushed out to appropriate network clients where the policy is applied.</span></span>

## <a name="related-topics"></a><span data-ttu-id="45b1c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="45b1c-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="45b1c-122">Configuration de l’interface utilisateur de la méthode EAP</span><span class="sxs-lookup"><span data-stu-id="45b1c-122">Configuring the EAP Method User Interface</span></span>](configuring-the-eap-method-user-interface.md)
</dt> <dt>

[<span data-ttu-id="45b1c-123">Implémentation de la prise en charge de In-Band NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="45b1c-123">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="45b1c-124">Implémentation de la prise en charge NAP pour les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="45b1c-124">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="45b1c-125">Transfert de données entre le demandeur et les méthodes EAP</span><span class="sxs-lookup"><span data-stu-id="45b1c-125">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="45b1c-126">Demandeurs EAPHost</span><span class="sxs-lookup"><span data-stu-id="45b1c-126">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




