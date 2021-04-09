---
description: Lorsque vous définissez un niveau d’emprunt d’identité pour une application, vous déterminez le degré d’autorité que l’application accorde à d’autres applications pour utiliser son identité lorsqu’elle les appelle.
ms.assetid: 5b5b2c2d-dc3d-4edd-9e13-e6cb13022ceb
title: Définition d’un niveau d’emprunt d’identité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1075ac3b10380892cdfdf770543a2dcbb32d56c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110898"
---
# <a name="setting-an-impersonation-level"></a><span data-ttu-id="95aae-103">Définition d’un niveau d’emprunt d’identité</span><span class="sxs-lookup"><span data-stu-id="95aae-103">Setting an Impersonation Level</span></span>

<span data-ttu-id="95aae-104">Lorsque vous définissez un niveau d’emprunt d’identité pour une application, vous déterminez le degré d’autorité que l’application accorde à d’autres applications pour utiliser son identité lorsqu’elle les appelle.</span><span class="sxs-lookup"><span data-stu-id="95aae-104">When you set an impersonation level for an application, you determine what degree of authority the application grants other applications to use its identity when it calls them.</span></span> <span data-ttu-id="95aae-105">Vous pouvez définir cette valeur uniquement pour les applications serveur COM+ : les applications de bibliothèque s’exécutent sous l’identité du processus d’hébergement et utilisent le niveau d’emprunt d’identité qu’elles spécifient.</span><span class="sxs-lookup"><span data-stu-id="95aae-105">You can set this only for COM+ server applications—library applications run under the identity of the hosting process and use the impersonation level that it specifies.</span></span> <span data-ttu-id="95aae-106">Pour plus d’informations, consultez [niveaux d’emprunt d’identité](/windows/desktop/com/impersonation-levels).</span><span class="sxs-lookup"><span data-stu-id="95aae-106">For more detail, see [Impersonation Levels](/windows/desktop/com/impersonation-levels).</span></span>

<span data-ttu-id="95aae-107">**Pour sélectionner un niveau d’emprunt d’identité**</span><span class="sxs-lookup"><span data-stu-id="95aae-107">**To select an impersonation level**</span></span>

1.  <span data-ttu-id="95aae-108">Cliquez avec le bouton droit sur l’application COM+ pour laquelle vous configurez l’emprunt d’identité, puis cliquez sur **Propriétés**.</span><span class="sxs-lookup"><span data-stu-id="95aae-108">Right-click the COM+ application for which you are setting impersonation, and then click **Properties**.</span></span>

2.  <span data-ttu-id="95aae-109">Dans la boîte de dialogue Propriétés de l’application, cliquez sur l’onglet **sécurité** .</span><span class="sxs-lookup"><span data-stu-id="95aae-109">In the application properties dialog box, click the **Security** tab.</span></span>

3.  <span data-ttu-id="95aae-110">Dans la zone **niveau d’emprunt d’identité** , sélectionnez le niveau approprié.</span><span class="sxs-lookup"><span data-stu-id="95aae-110">In the **Impersonation level** box, select the appropriate level.</span></span> <span data-ttu-id="95aae-111">Les niveaux sont les suivants, triés d’accordant au moins la plus grande autorité :</span><span class="sxs-lookup"><span data-stu-id="95aae-111">The levels are as follows, ordered from granting least to greatest authority:</span></span>

    -   <span data-ttu-id="95aae-112">**Anonyme**.</span><span class="sxs-lookup"><span data-stu-id="95aae-112">**Anonymous**.</span></span> <span data-ttu-id="95aae-113">Le client est anonyme au serveur.</span><span class="sxs-lookup"><span data-stu-id="95aae-113">The client is anonymous to the server.</span></span> <span data-ttu-id="95aae-114">Le serveur peut emprunter l’identité du client, mais le jeton d’emprunt d’identité (informations d’identification locales) ne contient pas d’informations sur le client.</span><span class="sxs-lookup"><span data-stu-id="95aae-114">The server can impersonate the client, but the impersonation token (a local credential) does not contain any information about the client.</span></span>
    -   <span data-ttu-id="95aae-115">**Identifiez**.</span><span class="sxs-lookup"><span data-stu-id="95aae-115">**Identify**.</span></span> <span data-ttu-id="95aae-116">Le serveur peut obtenir l’identité du client et peut emprunter l’identité du client pour effectuer des vérifications de liste de contrôle d’accès.</span><span class="sxs-lookup"><span data-stu-id="95aae-116">The server can obtain the client's identity and can impersonate the client to do ACL checks.</span></span>
    -   <span data-ttu-id="95aae-117">**Emprunter l’identité**.</span><span class="sxs-lookup"><span data-stu-id="95aae-117">**Impersonate**.</span></span> <span data-ttu-id="95aae-118">Le serveur peut emprunter l’identité du client tout en agissant en son nom, bien qu’avec des restrictions.</span><span class="sxs-lookup"><span data-stu-id="95aae-118">The server can impersonate the client while acting on its behalf, although with restrictions.</span></span> <span data-ttu-id="95aae-119">Le serveur peut accéder aux ressources sur le même ordinateur que le client.</span><span class="sxs-lookup"><span data-stu-id="95aae-119">The server can access resources on the same computer as the client.</span></span> <span data-ttu-id="95aae-120">Si le serveur se trouve sur le même ordinateur que le client, il peut accéder aux ressources réseau en tant que client.</span><span class="sxs-lookup"><span data-stu-id="95aae-120">If the server is on the same computer as the client, it can access network resources as the client.</span></span> <span data-ttu-id="95aae-121">Si le serveur se trouve sur un ordinateur différent du client, il ne peut accéder qu’aux ressources qui se trouvent sur le même ordinateur que le serveur.</span><span class="sxs-lookup"><span data-stu-id="95aae-121">If the server is on a computer different from the client, it can access only resources that are on the same computer as the server.</span></span> <span data-ttu-id="95aae-122">Il s’agit du paramètre par défaut pour les applications serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="95aae-122">This is the default setting for COM+ server applications.</span></span>
    -   <span data-ttu-id="95aae-123">**Délégué**.</span><span class="sxs-lookup"><span data-stu-id="95aae-123">**Delegate**.</span></span> <span data-ttu-id="95aae-124">Le serveur peut emprunter l’identité du client tout en agissant en son nom, que ce soit sur le même ordinateur que le client.</span><span class="sxs-lookup"><span data-stu-id="95aae-124">The server can impersonate the client while acting on its behalf, whether on the same computer as the client.</span></span> <span data-ttu-id="95aae-125">Pendant l’emprunt d’identité, les informations d’identification du client (à la fois celles avec local et celles avec une validité réseau) peuvent être transmises à n’importe quel nombre d’ordinateurs.</span><span class="sxs-lookup"><span data-stu-id="95aae-125">During impersonation, the client's credentials (both those with local and those with network validity) can be passed to any number of machines.</span></span>

4.  <span data-ttu-id="95aae-126">Cliquez sur **OK**.</span><span class="sxs-lookup"><span data-stu-id="95aae-126">Click **OK**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="95aae-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="95aae-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95aae-128">Configuration de la sécurité de Role-Based</span><span class="sxs-lookup"><span data-stu-id="95aae-128">Configuring Role-Based Security</span></span>](configuring-role-based-security.md)
</dt> <dt>

[<span data-ttu-id="95aae-129">Configuration de la stratégie de restriction logicielle</span><span class="sxs-lookup"><span data-stu-id="95aae-129">Configuring the Software Restriction Policy</span></span>](configuring-the-software-restriction-policy.md)
</dt> <dt>

[<span data-ttu-id="95aae-130">Activation de l’authentification pour une application de bibliothèque</span><span class="sxs-lookup"><span data-stu-id="95aae-130">Enabling Authentication for a Library Application</span></span>](enabling-authentication-for-a-library-application.md)
</dt> <dt>

[<span data-ttu-id="95aae-131">Définition d’un niveau d’authentification pour une application serveur</span><span class="sxs-lookup"><span data-stu-id="95aae-131">Setting an Authentication Level for a Server Application</span></span>](setting-an-authentication-level-for-a-server-application.md)
</dt> </dl>

 

 
