---
description: Le compte LocalService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.
ms.assetid: 5409e2fe-a349-4739-a481-f8a35fd3c9b4
title: Compte LocalService
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d67051b95d6e5d18179bb2dc69928e68edb0f3e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529866"
---
# <a name="localservice-account"></a><span data-ttu-id="5f5a0-103">Compte LocalService</span><span class="sxs-lookup"><span data-stu-id="5f5a0-103">LocalService Account</span></span>

<span data-ttu-id="5f5a0-104">Le compte LocalService est un compte local prédéfini utilisé par le gestionnaire de contrôle des services.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-104">The LocalService account is a predefined local account used by the service control manager.</span></span> <span data-ttu-id="5f5a0-105">Il possède des privilèges minimum sur l’ordinateur local et présente des informations d’identification anonymes sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-105">It has minimum privileges on the local computer and presents anonymous credentials on the network.</span></span>

<span data-ttu-id="5f5a0-106">Ce compte peut être spécifié dans un appel aux fonctions [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) et [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) .</span><span class="sxs-lookup"><span data-stu-id="5f5a0-106">This account can be specified in a call to the [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea) and [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga) functions.</span></span> <span data-ttu-id="5f5a0-107">Notez que ce compte n’a pas de mot de passe. par conséquent, les informations de mot de passe que vous fournissez dans cet appel sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-107">Note that this account does not have a password, so any password information that you provide in this call is ignored.</span></span> <span data-ttu-id="5f5a0-108">Tandis que le sous-système de sécurité localise ce nom de compte, le SCM ne prend pas en charge les noms localisés.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-108">While the security subsystem localizes this account name, the SCM does not support localized names.</span></span> <span data-ttu-id="5f5a0-109">Par conséquent, vous recevrez un nom localisé pour ce compte à partir de la fonction [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) , mais le nom du compte doit être NT Authority \\ LocalService quand vous appelez **CreateService** ou **ChangeServiceConfig**, indépendamment des paramètres régionaux, ou des résultats inattendus peuvent se produire.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-109">Therefore, you will receive a localized name for this account from the [**LookupAccountSid**](/windows/desktop/api/winbase/nf-winbase-lookupaccountsida) function, but the name of the account must be NT AUTHORITY\\LocalService when you call **CreateService** or **ChangeServiceConfig**, regardless of the locale, or unexpected results can occur.</span></span>

<span data-ttu-id="5f5a0-110">Le SID de l’utilisateur est créé à partir de la valeur **\_ \_ \_ RID du service local de sécurité** .</span><span class="sxs-lookup"><span data-stu-id="5f5a0-110">The user SID is created from the **SECURITY\_LOCAL\_SERVICE\_RID** value.</span></span>

<span data-ttu-id="5f5a0-111">Le compte LocalService possède sa propre sous-clé sous la clé de Registre **HKEY \_ Users** .</span><span class="sxs-lookup"><span data-stu-id="5f5a0-111">The LocalService account has its own subkey under the **HKEY\_USERS** registry key.</span></span> <span data-ttu-id="5f5a0-112">Par conséquent, la clé de Registre **HKEY \_ Current \_ User** est associée au compte LocalService.</span><span class="sxs-lookup"><span data-stu-id="5f5a0-112">Therefore, the **HKEY\_CURRENT\_USER** registry key is associated with the LocalService account.</span></span>

<span data-ttu-id="5f5a0-113">Le compte LocalService dispose des privilèges suivants :</span><span class="sxs-lookup"><span data-stu-id="5f5a0-113">The LocalService account has the following privileges:</span></span>

-   <span data-ttu-id="5f5a0-114">**Se \_ \_Nom de ASSIGNPRIMARYTOKEN** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-114">**SE\_ASSIGNPRIMARYTOKEN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="5f5a0-115">**Se \_ \_Nom de l’audit** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-115">**SE\_AUDIT\_NAME** (disabled)</span></span>
-   <span data-ttu-id="5f5a0-116">**Se \_ MODIFIER \_ le \_ nom** de la notification (activé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-116">**SE\_CHANGE\_NOTIFY\_NAME** (enabled)</span></span>
-   <span data-ttu-id="5f5a0-117">**Se \_ CRÉER \_ un \_ nom global** (activé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-117">**SE\_CREATE\_GLOBAL\_NAME** (enabled)</span></span>
-   <span data-ttu-id="5f5a0-118">**Se \_ \_Nom d’emprunt d’identité** (activé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-118">**SE\_IMPERSONATE\_NAME** (enabled)</span></span>
-   <span data-ttu-id="5f5a0-119">**Se \_ AUGMENTER \_ le \_ nom du quota** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-119">**SE\_INCREASE\_QUOTA\_NAME** (disabled)</span></span>
-   <span data-ttu-id="5f5a0-120">**Se \_ \_Nom** de l’arrêt (désactivé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-120">**SE\_SHUTDOWN\_NAME** (disabled)</span></span>
-   <span data-ttu-id="5f5a0-121">**Se \_ Détacher le \_ nom** (désactivé)</span><span class="sxs-lookup"><span data-stu-id="5f5a0-121">**SE\_UNDOCK\_NAME** (disabled)</span></span>
-   <span data-ttu-id="5f5a0-122">Tous les privilèges attribués aux utilisateurs et aux utilisateurs authentifiés</span><span class="sxs-lookup"><span data-stu-id="5f5a0-122">Any privileges assigned to users and authenticated users</span></span>

<span data-ttu-id="5f5a0-123">Pour plus d’informations, consultez [sécurité des services et droits d’accès](service-security-and-access-rights.md).</span><span class="sxs-lookup"><span data-stu-id="5f5a0-123">For more information, see [Service Security and Access Rights](service-security-and-access-rights.md).</span></span>

 

 
