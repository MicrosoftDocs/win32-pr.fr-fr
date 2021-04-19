---
description: L’écriture d’un fournisseur sécurisé requiert la prise en compte de l’hébergement du fournisseur, de la façon dont le fournisseur gère l’emprunt d’identité et de la vérification des droits d’accès aux données par les utilisateurs.
ms.assetid: 9a8b7730-cbb8-48fa-8a8f-8e551f00d20b
ms.tgt_platform: multiple
title: Sécurisation de votre fournisseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b6b8fef1e90f09bc09488c058240b7fd1a88ebd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534169"
---
# <a name="securing-your-provider"></a><span data-ttu-id="e148d-103">Sécurisation de votre fournisseur</span><span class="sxs-lookup"><span data-stu-id="e148d-103">Securing Your Provider</span></span>

<span data-ttu-id="e148d-104">L’écriture d’un fournisseur sécurisé requiert la prise en compte de l’hébergement du fournisseur, de la façon dont le fournisseur gère l’emprunt d’identité et de la vérification des droits d’accès aux données par les utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="e148d-104">Writing a secure provider requires considering how the provider is hosted, how the provider handles impersonation, and ensuring that users are checked for access rights to data.</span></span> <span data-ttu-id="e148d-105">Vous pouvez sécuriser les données dans votre espace de noms de fournisseur en exigeant l’authentification chiffrée des données avant leur envoi sur un réseau.</span><span class="sxs-lookup"><span data-stu-id="e148d-105">You can secure the data in your provider namespace by requiring that data be encrypted authentication before sending it over a network.</span></span> <span data-ttu-id="e148d-106">Pour plus d’informations, consultez [la page exiger une connexion chiffrée à un espace de noms](requiring-an-encrypted-connection-to-a-namespace.md).</span><span class="sxs-lookup"><span data-stu-id="e148d-106">For more information, see [Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md).</span></span>

<span data-ttu-id="e148d-107">Si un utilisateur dispose d’un accès en **\_ écriture complet** dans n’importe quel espace de noms, l’utilisateur peut créer des abonnements à plusieurs espaces de noms pour les données d’un espace de noms dans lequel l’utilisateur est limité.</span><span class="sxs-lookup"><span data-stu-id="e148d-107">If a user has **FULL\_WRITE** access in any namespace, then the user can create cross-namespace subscriptions for data in a namespace in which the user is restricted.</span></span> <span data-ttu-id="e148d-108">Étant donné qu’un fournisseur peut être chargé dans n’importe quel espace de noms et s’exécuter dans n’importe quel contexte de sécurité, le fournisseur doit effectuer ses propres contrôles d’accès pour s’assurer que seuls les utilisateurs autorisés sont autorisés à accéder aux données ou à exécuter des méthodes.</span><span class="sxs-lookup"><span data-stu-id="e148d-108">Because a provider can be loaded into any namespace and be executing in any security context, the provider should perform its own access checks to ensure that only authorized users are allowed access to data or to execute methods.</span></span> <span data-ttu-id="e148d-109">Pour plus d’informations, consultez [exécution de vérifications d’accès](performing-access-checks.md).</span><span class="sxs-lookup"><span data-stu-id="e148d-109">For more information, see [Performing Access Checks](performing-access-checks.md).</span></span>

<span data-ttu-id="e148d-110">Les rubriques suivantes traitent de la sécurité du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="e148d-110">The following topics discuss provider security:</span></span>

-   [<span data-ttu-id="e148d-111">Hébergement et sécurité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="e148d-111">Provider Hosting and Security</span></span>](provider-hosting-and-security.md)
-   [<span data-ttu-id="e148d-112">Exécution des vérifications d’accès</span><span class="sxs-lookup"><span data-stu-id="e148d-112">Performing Access Checks</span></span>](performing-access-checks.md)
-   [<span data-ttu-id="e148d-113">Clés de Registre pour le contrôle de la sécurité du fournisseur</span><span class="sxs-lookup"><span data-stu-id="e148d-113">Registry Keys for Controlling Provider Security</span></span>](registry-keys-for-controlling-provider-security-.md)
-   [<span data-ttu-id="e148d-114">Accès aux espaces de noms WMI</span><span class="sxs-lookup"><span data-stu-id="e148d-114">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
-   [<span data-ttu-id="e148d-115">Emprunt de l’identité d’un client</span><span class="sxs-lookup"><span data-stu-id="e148d-115">Impersonating a Client</span></span>](impersonating-a-client.md)

<span data-ttu-id="e148d-116">Les rubriques suivantes expliquent comment les clients et les scripts interagissent avec la sécurité du fournisseur :</span><span class="sxs-lookup"><span data-stu-id="e148d-116">The following topics discuss how clients and scripts interact with provider security:</span></span>

-   [<span data-ttu-id="e148d-117">Configuration de l’authentification dans WMI</span><span class="sxs-lookup"><span data-stu-id="e148d-117">Setting Authentication in WMI</span></span>](setting-authentication-in-wmi.md)
-   [<span data-ttu-id="e148d-118">Connexion entre différents systèmes d’exploitation</span><span class="sxs-lookup"><span data-stu-id="e148d-118">Connecting Between Different Operating Systems</span></span>](/windows/desktop/WmiSdk/troubleshooting-a-remote-wmi-connection)
-   [<span data-ttu-id="e148d-119">Définition du niveau de sécurité de processus par défaut à l’aide de VBScript</span><span class="sxs-lookup"><span data-stu-id="e148d-119">Setting the Default Process Security Level Using VBScript</span></span>](setting-the-default-process-security-level-using-vbscript.md)
-   [<span data-ttu-id="e148d-120">Définition de la sécurité des processus d’application cliente</span><span class="sxs-lookup"><span data-stu-id="e148d-120">Setting Client Application Process Security</span></span>](setting-client-application-process-security.md)

## <a name="related-topics"></a><span data-ttu-id="e148d-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e148d-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e148d-122">Maintenance de la sécurité WMI</span><span class="sxs-lookup"><span data-stu-id="e148d-122">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="e148d-123">Utilisation de WMI</span><span class="sxs-lookup"><span data-stu-id="e148d-123">Using WMI</span></span>](using-wmi.md)
</dt> </dl>

 

 
