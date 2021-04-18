---
title: DefaultLaunchPermission
description: Définit la liste de Access Control (ACL) des principaux qui peuvent lancer des classes qui ne spécifient pas leur propre ACL via la valeur de Registre LaunchPermission.
ms.assetid: 23ca87fc-7829-46a9-9fc3-2cd7f677bbff
keywords:
- Valeur de Registre DefaultLaunchPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 599a0993a4a1238e57e357f428f7046331412cc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106527139"
---
# <a name="defaultlaunchpermission"></a><span data-ttu-id="1997f-104">DefaultLaunchPermission</span><span class="sxs-lookup"><span data-stu-id="1997f-104">DefaultLaunchPermission</span></span>

<span data-ttu-id="1997f-105">Définit la liste de Access Control (ACL) des principaux qui peuvent lancer des classes qui ne spécifient pas leur propre ACL via la valeur de Registre [**LaunchPermission**](launchpermission.md) .</span><span class="sxs-lookup"><span data-stu-id="1997f-105">Defines the Access Control List (ACL) of the principals that can launch classes that do not specify their own ACL through the [**LaunchPermission**](launchpermission.md) registry value.</span></span>

> [!Caution]  
> <span data-ttu-id="1997f-106">Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="1997f-106">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="1997f-107">Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="1997f-107">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="1997f-108">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="1997f-108">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="1997f-109">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="1997f-109">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultLaunchPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="1997f-110">Notes</span><span class="sxs-lookup"><span data-stu-id="1997f-110">Remarks</span></span>

<span data-ttu-id="1997f-111">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="1997f-111">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="1997f-112">Les autorisations d’accès par défaut sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1997f-112">The default access permissions are as follows:</span></span>

-   <span data-ttu-id="1997f-113">Administrateurs : autoriser le lancement</span><span class="sxs-lookup"><span data-stu-id="1997f-113">Administrators: allow launch</span></span>
-   <span data-ttu-id="1997f-114">SYSTÈME : autoriser le lancement</span><span class="sxs-lookup"><span data-stu-id="1997f-114">SYSTEM: allow launch</span></span>
-   <span data-ttu-id="1997f-115">INTERACTIF : autoriser le lancement</span><span class="sxs-lookup"><span data-stu-id="1997f-115">INTERACTIVE: allow launch</span></span>

<span data-ttu-id="1997f-116">Si la valeur [**LaunchPermission**](launchpermission.md) est définie pour un serveur, elle est prioritaire sur la valeur **DefaultLaunchPermission** .</span><span class="sxs-lookup"><span data-stu-id="1997f-116">If the [**LaunchPermission**](launchpermission.md) value is set for a server, it takes precedence over the **DefaultLaunchPermission** value.</span></span> <span data-ttu-id="1997f-117">Lors de la réception d’une demande locale ou distante pour lancer un serveur dont la clé [**AppID**](appid-key.md) n’a pas sa propre valeur **LaunchPermission** , la liste de contrôle d’accès décrite par cette valeur est vérifiée en usurpant l’identité du client et sa réussite autorise ou interdit le lancement du code de la classe.</span><span class="sxs-lookup"><span data-stu-id="1997f-117">Upon receiving a local or remote request to launch a server whose [**AppID**](appid-key.md) key has no **LaunchPermission** value of its own, the ACL described by this value is checked while impersonating the client and its success either allows or disallows the launching of the class code.</span></span>

<span data-ttu-id="1997f-118">Cette valeur fournit un niveau simple d’administration centralisée de l’accès par défaut au lancement des classes non gérées sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1997f-118">This value provides a simple level of centralized administration of the default launching access to otherwise unadministered classes on a computer.</span></span> <span data-ttu-id="1997f-119">Par exemple, un administrateur peut utiliser l’outil DCOMCNFG pour configurer le système afin d’autoriser l’accès en lecture seule pour les utilisateurs avec pouvoir.</span><span class="sxs-lookup"><span data-stu-id="1997f-119">For example, an administrator might use the DCOMCNFG tool to configure the system to allow read-only access for Power Users.</span></span> <span data-ttu-id="1997f-120">OLE limite donc les demandes de lancement du code de la classe aux membres du groupe utilisateurs avec pouvoir.</span><span class="sxs-lookup"><span data-stu-id="1997f-120">OLE would therefore restrict requests to launch class code to members of the Power Users group.</span></span> <span data-ttu-id="1997f-121">Un administrateur peut ensuite configurer des autorisations de lancement pour des classes individuelles afin d’accorder la possibilité de lancer le code de classe à d’autres groupes ou utilisateurs individuels en fonction des besoins.</span><span class="sxs-lookup"><span data-stu-id="1997f-121">An administrator could subsequently configure launch permissions for individual classes to grant the ability to launch class code to other groups or individual users as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1997f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1997f-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1997f-123">**LaunchPermission**</span><span class="sxs-lookup"><span data-stu-id="1997f-123">**LaunchPermission**</span></span>](launchpermission.md)
</dt> <dt>

[<span data-ttu-id="1997f-124">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="1997f-124">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="1997f-125">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="1997f-125">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




