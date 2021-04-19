---
description: Le compte NetworkService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.
ms.assetid: f90d9346-10ed-4eba-bae2-9a1f1e6dc6b7
title: Compte NetworkService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c319518dbe925a146882014211d131c30420a282
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106537061"
---
# <a name="networkservice-account"></a><span data-ttu-id="08b5f-103">Compte NetworkService</span><span class="sxs-lookup"><span data-stu-id="08b5f-103">NetworkService Account</span></span>

<span data-ttu-id="08b5f-104">Le compte NetworkService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="08b5f-104">The NetworkService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="08b5f-105">Ce compte n’est pas reconnu par le sous-système de sécurité. vous ne pouvez donc pas spécifier son nom dans un appel à la fonction [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) .</span><span class="sxs-lookup"><span data-stu-id="08b5f-105">This account is not recognized by the security subsystem, so you cannot specify its name in a call to the [**LookupAccountName**](/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea) function.</span></span> <span data-ttu-id="08b5f-106">Il possède des privilèges minimum sur l’ordinateur local et agit en tant qu’ordinateur sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="08b5f-106">It has minimum privileges on the local computer and acts as the computer on the network.</span></span>

<span data-ttu-id="08b5f-107">Ce compte peut être spécifié dans un appel aux fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="08b5f-107">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="08b5f-108">Notez que ce compte n’a pas de mot de passe. par conséquent, les informations de mot de passe que vous fournissez dans cet appel sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="08b5f-108">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="08b5f-109">Tandis que le sous-système de sécurité localise ce nom de compte, le SCM ne prend pas en charge les noms localisés.</span><span class="sxs-lookup"><span data-stu-id="08b5f-109">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="08b5f-110">Par conséquent, vous recevrez un nom localisé pour ce compte à partir de la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mais le nom du compte doit être NT Authority \\ NetworkService quand vous appelez **CreateService** ou **ChangeServiceConfig**, indépendamment des paramètres régionaux, ou des résultats inattendus peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="08b5f-110">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\NetworkService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="08b5f-111">Un service qui s’exécute dans le contexte du compte NetworkService présente les informations d’identification de l’ordinateur aux serveurs distants.</span><span class="sxs-lookup"><span data-stu-id="08b5f-111">A service that runs in the context of the NetworkService account presents the computer's credentials to remote servers.</span></span> <span data-ttu-id="08b5f-112">Par défaut, le jeton distant contient des SID pour les groupes tout le monde et utilisateurs authentifiés.</span><span class="sxs-lookup"><span data-stu-id="08b5f-112">By default, the remote token contains SIDs for the Everyone and Authenticated Users groups.</span></span> <span data-ttu-id="08b5f-113">Le SID de l’utilisateur est créé à partir de la valeur **\_ \_ \_ RID du service réseau de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="08b5f-113">The user SID is created from the **SECURITY\_NETWORK\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="08b5f-114">Le compte NetworkService possède sa propre sous-clé sous la clé de Registre **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="08b5f-114">The NetworkService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="08b5f-115">Par conséquent, la clé de Registre **HKEY \_ Current \_ User** est associée au compte NetworkService.</span><span class="sxs-lookup"><span data-stu-id="08b5f-115">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the NetworkService account.</span></span>

<span data-ttu-id="08b5f-116">Le compte NetworkService dispose des privilèges suivants :</span><span class="sxs-lookup"><span data-stu-id="08b5f-116">The NetworkService account has the following privileges:</span></span>

-   <span data-ttu-id="08b5f-117">**Se \_ \_Nom de ASSIGNPRIMARYTOKEN** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-117">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="08b5f-118">**Se \_ \_Nom de l’audit** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-118">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="08b5f-119">**Se \_ MODIFIER \_ le \_ nom** de la notification (activé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-119">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="08b5f-120">**Se \_ CRÉER \_ un \_ nom global** (activé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-120">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="08b5f-121">**Se \_ \_Nom d’emprunt d’identité** (activé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-121">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="08b5f-122">**Se \_ AUGMENTER \_ le \_ nom du quota** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-122">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="08b5f-123">**Se \_ \_Nom** de l’arrêt (désactivé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-123">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="08b5f-124">**Se \_ Détacher le \_ nom** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="08b5f-124">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="08b5f-125">Tous les privilèges attribués aux utilisateurs et aux utilisateurs authentifiés</span><span class="sxs-lookup"><span data-stu-id="08b5f-125">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="08b5f-126">Pour plus d’informations, consultez [sécurité des services et droits d’accès](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="08b5f-126">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
