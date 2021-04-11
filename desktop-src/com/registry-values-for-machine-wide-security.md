---
title: Valeurs de Registre pour la sécurité System-Wide
description: Valeurs de Registre pour la sécurité System-Wide
ms.assetid: f1db42b8-4328-4b39-b87f-583382395235
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e7addfb59bd8074a5a1392e5f74f9cee73d64f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939825"
---
# <a name="registry-values-for-system-wide-security"></a><span data-ttu-id="08a68-103">Valeurs de Registre pour la sécurité System-Wide</span><span class="sxs-lookup"><span data-stu-id="08a68-103">Registry Values for System-Wide Security</span></span>

<span data-ttu-id="08a68-104">Il n’est pas recommandé de modifier les paramètres de sécurité à l’ensemble du système, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="08a68-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="08a68-105">Si vous modifiez les paramètres de sécurité à l’ensemble du système pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="08a68-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="08a68-106">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité Process-Wide](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="08a68-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="08a68-107">Certaines valeurs du Registre sont utilisées pour déterminer les paramètres de sécurité des applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="08a68-107">Certain values in the registry are used to determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="08a68-108">Vous pouvez utiliser Dcomcnfg.exe pour modifier ces paramètres de sécurité par défaut pour un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="08a68-108">You can use Dcomcnfg.exe to modify these default security settings for a computer.</span></span> <span data-ttu-id="08a68-109">Pour obtenir des procédures pas à pas qui décrivent comment utiliser Dcomcnfg.exe à cet effet, consultez [définition de la sécurité des System-Wide à l’aide de DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span><span class="sxs-lookup"><span data-stu-id="08a68-109">For step-by-step procedures that describe how to use Dcomcnfg.exe for this purpose, see [Setting System-Wide Security Using DCOMCNFG](setting-machine-wide-security-using-dcomcnfg.md).</span></span>

<span data-ttu-id="08a68-110">Une autre façon de modifier les paramètres par défaut à l’ensemble du système consiste à manipuler les valeurs de Registre directement.</span><span class="sxs-lookup"><span data-stu-id="08a68-110">Another way to change default system-wide settings is to manipulate registry values directly.</span></span> <span data-ttu-id="08a68-111">Toutefois, seuls les administrateurs et le système ont un accès complet à la partie du Registre qui contient les paramètres de sécurité par défaut des appels à l’échelle du système.</span><span class="sxs-lookup"><span data-stu-id="08a68-111">However, only administrators and the system have full access to the portion of the registry that contains the default system-wide call-security settings.</span></span> <span data-ttu-id="08a68-112">Tous les autres utilisateurs disposent uniquement d’un accès en lecture.</span><span class="sxs-lookup"><span data-stu-id="08a68-112">All other users have read-access only.</span></span>

<span data-ttu-id="08a68-113">Les valeurs nommées qui affectent les paramètres de sécurité par défaut à l’ensemble du système sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="08a68-113">The named values that affect system-wide security defaults are as follows:</span></span>

-   [<span data-ttu-id="08a68-114">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="08a68-114">DefaultLaunchPermission</span></span>](defaultlaunchpermission.md)
-   [<span data-ttu-id="08a68-115">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="08a68-115">DefaultAccessPermission</span></span>](defaultaccesspermission.md)
-   [<span data-ttu-id="08a68-116">LegacyAuthenticationLevel</span><span class="sxs-lookup"><span data-stu-id="08a68-116">LegacyAuthenticationLevel</span></span>](legacyauthenticationlevel.md)
-   [<span data-ttu-id="08a68-117">LegacyImpersonationLevel</span><span class="sxs-lookup"><span data-stu-id="08a68-117">LegacyImpersonationLevel</span></span>](legacyimpersonationlevel.md)
-   [<span data-ttu-id="08a68-118">LegacySecureReferences</span><span class="sxs-lookup"><span data-stu-id="08a68-118">LegacySecureReferences</span></span>](legacysecurereferences.md)
-   [<span data-ttu-id="08a68-119">SRPRunningObjectChecks</span><span class="sxs-lookup"><span data-stu-id="08a68-119">SRPRunningObjectChecks</span></span>](srprunningobjectchecks.md)
-   [<span data-ttu-id="08a68-120">SRPActivateAsActivatorChecks</span><span class="sxs-lookup"><span data-stu-id="08a68-120">SRPActivateAsActivatorChecks</span></span>](srpactivateasactivatorchecks.md)

## <a name="related-topics"></a><span data-ttu-id="08a68-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08a68-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="08a68-122">Définition de la sécurité Process-Wide</span><span class="sxs-lookup"><span data-stu-id="08a68-122">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




