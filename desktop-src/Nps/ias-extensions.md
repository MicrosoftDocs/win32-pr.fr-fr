---
title: Extensions du serveur NPS (Network Policy Server)
description: L’API extensions NPS permet aux développeurs de logiciels d’écrire des dll d’extension qui peuvent être utilisées pour l’authentification, l’autorisation et la gestion des comptes. L’API extensions NPS prend en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).
ms.assetid: f459025f-fe5e-4ffa-a651-c70a4f8234ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd6f9bd0be7479726110b41d6060a7e5c836bb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941218"
---
# <a name="network-policy-server-extensions"></a><span data-ttu-id="b68d2-104">Extensions du serveur NPS (Network Policy Server)</span><span class="sxs-lookup"><span data-stu-id="b68d2-104">Network Policy Server Extensions</span></span>

> [!Note]  
> <span data-ttu-id="b68d2-105">Le service d’authentification Internet (IAS) a été renommé serveur NPS (Network Policy Server) à partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="b68d2-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="b68d2-106">Le contenu de cette rubrique s’applique à IAS et à NPS.</span><span class="sxs-lookup"><span data-stu-id="b68d2-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="b68d2-107">Dans le texte, NPS est utilisé pour faire référence à toutes les versions du service, y compris les versions initialement appelées IAS.</span><span class="sxs-lookup"><span data-stu-id="b68d2-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="b68d2-108">L’API extensions NPS permet aux développeurs de logiciels d’écrire des dll d’extension qui peuvent être utilisées pour l’authentification, l’autorisation et la gestion des comptes.</span><span class="sxs-lookup"><span data-stu-id="b68d2-108">The NPS Extensions API enables software developers to write extension DLLs that can be used for authentication, authorization, and accounting.</span></span> <span data-ttu-id="b68d2-109">L’API extensions NPS prend en charge le protocole protocole RADIUS (Remote Authentication Dial-In User Service) (RADIUS).</span><span class="sxs-lookup"><span data-stu-id="b68d2-109">NPS Extensions API supports the Remote Authentication Dial-In User Service (RADIUS) protocol.</span></span>

<span data-ttu-id="b68d2-110">Les dll d’extension implémentées à l’aide de l’API d’extensions NPS peuvent fournir un contrôle et une gestion de session améliorés.</span><span class="sxs-lookup"><span data-stu-id="b68d2-110">The extension DLLs implemented using the NPS Extensions API can provide enhanced session control and accounting.</span></span> <span data-ttu-id="b68d2-111">Ces dll peuvent être utilisées dans des scénarios tels que le contrôle du nombre de sessions réseau de l’utilisateur final, l’utilisation d’un serveur d’État et la connexion aux bases de données d’authentification de domaine et aux services de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="b68d2-111">These DLLs can be used for scenarios such as controlling the number of end-user network sessions, using a state server, and connecting to domain authentication databases and Active Directory services.</span></span> <span data-ttu-id="b68d2-112">Les dll d’extension peuvent étendre les autorisations d’accès à distance fournies par NPS en ajoutant leurs propres autorisations lors de l’envoi d’une réponse d’acceptation à un client d’authentification.</span><span class="sxs-lookup"><span data-stu-id="b68d2-112">The extension DLLs can expand the remote access authorizations provided by NPS by adding their own authorizations when sending an Accept response back to an authenticating client.</span></span>

<span data-ttu-id="b68d2-113">L’API extensions NPS s’applique dans tout environnement informatique où elle améliore l’efficacité pour authentifier les utilisateurs distants via un serveur distant.</span><span class="sxs-lookup"><span data-stu-id="b68d2-113">NPS Extensions API is applicable in any computing environment where it would improve efficiency to authenticate dial-in users through a remote server.</span></span> <span data-ttu-id="b68d2-114">Cette technologie est particulièrement utile pour les fournisseurs de services Internet (ISP).</span><span class="sxs-lookup"><span data-stu-id="b68d2-114">This technology is especially useful for Internet Service Providers (ISPs).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b68d2-115">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="b68d2-115">In This Section</span></span>

[<span data-ttu-id="b68d2-116">Vue d’ensemble</span><span class="sxs-lookup"><span data-stu-id="b68d2-116">Overview</span></span>](/windows/desktop/Nps/ias-about-internet-authentication-service)

<span data-ttu-id="b68d2-117">Informations générales sur RADIUS et l’API des extensions NPS.</span><span class="sxs-lookup"><span data-stu-id="b68d2-117">General information about RADIUS and the NPS Extensions API.</span></span>

[<span data-ttu-id="b68d2-118">À</span><span class="sxs-lookup"><span data-stu-id="b68d2-118">Using</span></span>](/windows/desktop/Nps/ias-using-internet-authentication-service)

<span data-ttu-id="b68d2-119">Exemple de code illustrant l’utilisation de l’API d’extensions NPS.</span><span class="sxs-lookup"><span data-stu-id="b68d2-119">Sample code that demonstrates how to use the NPS Extensions API.</span></span>

[<span data-ttu-id="b68d2-120">Référence</span><span class="sxs-lookup"><span data-stu-id="b68d2-120">Reference</span></span>](/windows/desktop/Nps/ias-internet-authentication-service-reference)

<span data-ttu-id="b68d2-121">Documentation des types, fonctions et structures énumérés qui composent l’API des extensions NPS.</span><span class="sxs-lookup"><span data-stu-id="b68d2-121">Documentation of enumerated types, functions, and structures that compose the NPS Extensions API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b68d2-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b68d2-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b68d2-123">Serveur de stratégie réseau (service d’authentification Internet)</span><span class="sxs-lookup"><span data-stu-id="b68d2-123">Network Policy Server (Internet Authentication Service)</span></span>](portal.md)
</dt> <dt>

[<span data-ttu-id="b68d2-124">Protocole EAP (Extensible Authentication Protocol)</span><span class="sxs-lookup"><span data-stu-id="b68d2-124">Extensible Authentication Protocol (EAP)</span></span>](../eap/eap-start-page.md)
</dt> </dl>

 

 