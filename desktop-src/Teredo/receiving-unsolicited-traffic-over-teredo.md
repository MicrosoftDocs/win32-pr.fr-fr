---
title: Réception de trafic non sollicité sur Teredo
description: Teredo offre une connectivité globale à l’aide des fonctionnalités de traversée IPv6 et NAT.
ms.assetid: 0c03d1bb-15f8-4e77-9a96-e182b1d190ac
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a5c7ffe7b84cfa325b3ecd8c0858ad96445e629
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729044"
---
# <a name="receiving-unsolicited-traffic-over-teredo"></a><span data-ttu-id="d2360-103">Réception de trafic non sollicité sur Teredo</span><span class="sxs-lookup"><span data-stu-id="d2360-103">Receiving Unsolicited Traffic Over Teredo</span></span>

<span data-ttu-id="d2360-104">[Teredo](about-teredo.md) offre une connectivité globale à l’aide des fonctionnalités de traversée IPv6 et NAT.</span><span class="sxs-lookup"><span data-stu-id="d2360-104">[Teredo](about-teredo.md) provides global connectivity using IPv6 and NAT traversal capabilities.</span></span> <span data-ttu-id="d2360-105">Toutefois, de nombreuses applications, y compris pair à pair, requièrent Teredo pour recevoir le trafic non sollicité d’Internet.</span><span class="sxs-lookup"><span data-stu-id="d2360-105">However, many applications, including peer-to-peer, will require Teredo to receive unsolicited traffic from the Internet.</span></span> <span data-ttu-id="d2360-106">Une application peut être programmée pour recevoir le trafic via une interface IPv6 unique ou toutes les interfaces compatibles IPv6.</span><span class="sxs-lookup"><span data-stu-id="d2360-106">An application can be programmed to receive traffic over a single IPv6 interface or all IPv6-capable interfaces.</span></span> <span data-ttu-id="d2360-107">Cette documentation décrit la configuration requise pour les applications qui utilisent l’interface Teredo pour recevoir le trafic IPv6 non sollicité.</span><span class="sxs-lookup"><span data-stu-id="d2360-107">This documentation describes the requirements for applications that use the Teredo interface to receive unsolicited IPv6 traffic.</span></span>

<span data-ttu-id="d2360-108">Une application recevra le trafic non sollicité sur l’interface Teredo uniquement si l’application est inscrite auprès du [pare-feu Windows](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span><span class="sxs-lookup"><span data-stu-id="d2360-108">An application will receive unsolicited traffic over the Teredo interface only if the application is registered with [Windows Firewall](/previous-versions/windows/desktop/ics/windows-firewall-start-page).</span></span> <span data-ttu-id="d2360-109">Pour recevoir du trafic non sollicité, les conditions suivantes doivent être remplies :</span><span class="sxs-lookup"><span data-stu-id="d2360-109">In order to receive unsolicited traffic the following must occur:</span></span>

-   <span data-ttu-id="d2360-110">Les utilisateurs doivent être invités à utiliser la console MMC (Microsoft Management Console) pour activer l’option « traversée latérale » pour une application.</span><span class="sxs-lookup"><span data-stu-id="d2360-110">Users must be instructed to use of the Microsoft Management Console (MMC) to enable the "Edge Traversal" option for an application.</span></span> <span data-ttu-id="d2360-111">Cette option est disponible sous le pare-feu Windows Snap-In--> <application name> --> onglet « Avancé ». L’option « traversée latérale » doit être activée individuellement pour chaque application.</span><span class="sxs-lookup"><span data-stu-id="d2360-111">This option is available under Windows Firewall Snap-In --> <application name> --> "Advanced" tab. The "Edge Traversal" option must be enabled individually for each application.</span></span>

-   <span data-ttu-id="d2360-112">L’option « traversée latérale » est activée par l’application.</span><span class="sxs-lookup"><span data-stu-id="d2360-112">The "Edge Traversal" option is enabled by the application.</span></span> <span data-ttu-id="d2360-113">Il est possible pour les applications susceptibles de recevoir du trafic non sollicité de s’inscrire auprès du pare-feu Windows pour la « traversée latérale » et de recevoir le trafic non sollicité sur l’interface Teredo.</span><span class="sxs-lookup"><span data-stu-id="d2360-113">It is possible for applications capable of receiving unsolicited traffic to register with Windows Firewall for "Edge Traversal" and receive unsolicited traffic over the Teredo interface.</span></span> <span data-ttu-id="d2360-114">Pour ce faire, une application doit appeler l’API [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) avec l’option « traversée latérale » définie sur variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="d2360-114">To do this an application must call the [**INetFwPolicy2**](/previous-versions/windows/desktop/api/netfw/nn-netfw-inetfwpolicy2) API with the "Edge Traversal" option set to VARIANT\_TRUE.</span></span> <span data-ttu-id="d2360-115">Le consentement de l’utilisateur est requis pour cet appel d’API avant qu’une application soit autorisée à écouter le trafic.</span><span class="sxs-lookup"><span data-stu-id="d2360-115">User consent is required for this API call before an application is permitted to listen for the traffic.</span></span>

-   <span data-ttu-id="d2360-116">L’application définit l’option de socket de [ \_ \_ niveau de protection IPv6 IPv6](/windows/desktop/WinSock/ipv6-protection-level) sur le **niveau de protection non \_ \_ restreint** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span><span class="sxs-lookup"><span data-stu-id="d2360-116">The application sets the Winsock [IPV6\_PROTECTION\_LEVEL](/windows/desktop/WinSock/ipv6-protection-level) socket option to **PROTECTION\_LEVEL\_UNRESTRICTED** via [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span> <span data-ttu-id="d2360-117">Cela permettra à l’application de recevoir le trafic de traversée latérale.</span><span class="sxs-lookup"><span data-stu-id="d2360-117">This will allow the application to receive Edge Traversal traffic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d2360-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d2360-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2360-119">Réception du trafic sollicité sur Teredo</span><span class="sxs-lookup"><span data-stu-id="d2360-119">Receiving Solicited Traffic Over Teredo</span></span>](receiving-solicited-traffic-over-teredo.md)
</dt> </dl>

 

 