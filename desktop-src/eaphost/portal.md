---
title: Hôte de protocole EAP (Extensible Authentication Protocol)
description: En savoir plus sur l’hôte EAP (Extensible Authentication Protocol). Consultez Configuration requise pour l’exécution et afficher des ressources supplémentaires disponibles.
ms.assetid: caaef367-2952-44fc-ac4c-f0db6387850e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f007435c43969ad0f195b0a6a1e697ab817d9c4
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/18/2020
ms.locfileid: "104102593"
---
# <a name="extensible-authentication-protocol-host"></a><span data-ttu-id="5cc0a-104">Hôte de protocole EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="5cc0a-104">Extensible Authentication Protocol Host</span></span>

## <a name="purpose"></a><span data-ttu-id="5cc0a-105">Objectif</span><span class="sxs-lookup"><span data-stu-id="5cc0a-105">Purpose</span></span>


<span data-ttu-id="5cc0a-106">EAPHost est un composant de mise en réseau Microsoft Windows qui fournit une infrastructure EAP (Extensible Authentication Protocol) pour l’authentification des implémentations de protocole « demandeur », telles que [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) et PPP ( [point-to-point](https://go.microsoft.com/fwlink/p/?linkid=83919) ).</span><span class="sxs-lookup"><span data-stu-id="5cc0a-106">EAPHost is a Microsoft Windows Networking component that provides an Extensible Authentication Protocol (EAP) infrastructure for the authentication of "supplicant" protocol implementations such as [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) and [Point-to-Point](https://go.microsoft.com/fwlink/p/?linkid=83919) (PPP).</span></span> <span data-ttu-id="5cc0a-107">Il permet également l’authentification avec des technologies « authentificateur », telles que le serveur NPS (Network Policy Server) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5cc0a-107">It also allows for authentication with "authenticator" technologies such as the Microsoft network policy server (NPS).</span></span> <span data-ttu-id="5cc0a-108">Contrairement au serveur IAS précédent ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS prend en charge la [protection d’accès réseau](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span><span class="sxs-lookup"><span data-stu-id="5cc0a-108">Unlike the previous IAS Server ([RADIUS](/windows/desktop/Nps/ias-about-internet-authentication-service)), NPS supports [Network Access Protection](/windows/desktop/NAP/network-access-protection-start-page) (NAP).</span></span>


<span data-ttu-id="5cc0a-109">Les API EAPHost permettent aux applications de s’authentifier à l’aide du service EAPHost et fournissent un modèle pour le développement de méthodes d’authentification conformes pour une utilisation avec EAPHost.</span><span class="sxs-lookup"><span data-stu-id="5cc0a-109">The EAPHost APIs enable applications to authenticate using the EAPHost service, and provide a template for the development of conformant authentication methods for use with EAPHost.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5cc0a-110">Conditions d’exécution</span><span class="sxs-lookup"><span data-stu-id="5cc0a-110">Run-time requirements</span></span>

<span data-ttu-id="5cc0a-111">Les API EAPHost sont uniquement prises en charge dans Windows Vista et les systèmes d’exploitation ultérieurs.</span><span class="sxs-lookup"><span data-stu-id="5cc0a-111">The EAPHost APIs are supported only in Windows Vista and later operating systems.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5cc0a-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5cc0a-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5cc0a-113">À propos d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="5cc0a-113">About EAPHost</span></span>](about-eap-host.md)
</dt> <dt>

[<span data-ttu-id="5cc0a-114">Utilisation d’EAPHost</span><span class="sxs-lookup"><span data-stu-id="5cc0a-114">Using EAPHost</span></span>](using-eap-host.md)
</dt> <dt>

[<span data-ttu-id="5cc0a-115">Informations de référence sur l’API EAPHost</span><span class="sxs-lookup"><span data-stu-id="5cc0a-115">EAPHost API Reference</span></span>](eaphost-api-reference.md)
</dt> </dl>

 

 