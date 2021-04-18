---
title: DefaultAccessPermission
description: Définit la liste de Access Control (ACL) des principaux qui peuvent accéder aux classes pour lesquelles il n’existe aucun paramètre AccessPermission.
ms.assetid: 02675d0e-a96c-476e-820e-e6ff3c2d1be1
keywords:
- Valeur de Registre DefaultAccessPermission COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e6c132096807b8c234259071758ebd361421f8f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511810"
---
# <a name="defaultaccesspermission"></a><span data-ttu-id="e5508-104">DefaultAccessPermission</span><span class="sxs-lookup"><span data-stu-id="e5508-104">DefaultAccessPermission</span></span>

<span data-ttu-id="e5508-105">Définit la liste de Access Control (ACL) des principaux qui peuvent accéder aux classes pour lesquelles il n’existe aucun paramètre [**AccessPermission**](accesspermission.md) .</span><span class="sxs-lookup"><span data-stu-id="e5508-105">Sets the Access Control List (ACL) of the principals that can access classes for which there is no [**AccessPermission**](accesspermission.md) setting.</span></span> <span data-ttu-id="e5508-106">Cette liste de contrôle d’accès est utilisée uniquement par les applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) et qui n’ont pas de valeur **AccessPermission** sous leur clé [**AppID**](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="e5508-106">This ACL is used only by applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and do not have an **AccessPermission** value under their [**AppID**](appid-key.md) key.</span></span>

> [!Caution]  
> <span data-ttu-id="e5508-107">Il n’est pas recommandé de modifier cette valeur, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="e5508-107">It is not recommended that you change this value, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="e5508-108">Si vous modifiez cette valeur pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="e5508-108">If you are changing this value to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="e5508-109">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité au niveau du processus](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="e5508-109">For more information on setting process-wide security, see [Setting Process-wide Security](setting-processwide-security.md).</span></span>

 

## <a name="registry-entry"></a><span data-ttu-id="e5508-110">Entrée de Registre</span><span class="sxs-lookup"><span data-stu-id="e5508-110">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DefaultAccessPermission = ACL
```

## <a name="remarks"></a><span data-ttu-id="e5508-111">Notes</span><span class="sxs-lookup"><span data-stu-id="e5508-111">Remarks</span></span>

<span data-ttu-id="e5508-112">Il s’agit d’une valeur **\_ binaire de Reg** .</span><span class="sxs-lookup"><span data-stu-id="e5508-112">This is a **REG\_BINARY** value.</span></span>

<span data-ttu-id="e5508-113">Le runtime COM du serveur vérifie la liste de contrôle d’accès décrite par cette valeur tout en usurpant l’identité de l’appelant qui tente de se connecter à l’objet, et son succès détermine si l’accès est autorisé ou non.</span><span class="sxs-lookup"><span data-stu-id="e5508-113">The COM runtime in the server checks the ACL described by this value while impersonating the caller that is attempting to connect to the object, and its success determines whether the access is allowed or disallowed.</span></span> <span data-ttu-id="e5508-114">Si la vérification de l’accès échoue, la connexion à l’objet n’est pas autorisée.</span><span class="sxs-lookup"><span data-stu-id="e5508-114">If the access-check fails, the connection to the object is disallowed.</span></span> <span data-ttu-id="e5508-115">Si cette valeur nommée n’existe pas, seul le principal du serveur et le système local sont autorisés à appeler le serveur.</span><span class="sxs-lookup"><span data-stu-id="e5508-115">If this named value does not exist, only the server principal and local system are allowed to call the server.</span></span>

<span data-ttu-id="e5508-116">Par défaut, cette valeur ne contient aucune entrée.</span><span class="sxs-lookup"><span data-stu-id="e5508-116">By default, this value has no entries in it.</span></span> <span data-ttu-id="e5508-117">Seul le principal du serveur et le système sont autorisés à appeler le serveur.</span><span class="sxs-lookup"><span data-stu-id="e5508-117">Only the server principal and system are allowed to call the server.</span></span>

<span data-ttu-id="e5508-118">Cette valeur fournit un niveau simple d’administration centralisée de l’accès à la connexion par défaut aux objets en cours d’exécution sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="e5508-118">This value provides a simple level of centralized administration of the default connection access to running objects on a computer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e5508-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e5508-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5508-120">**AccessPermission**</span><span class="sxs-lookup"><span data-stu-id="e5508-120">**AccessPermission**</span></span>](accesspermission.md)
</dt> <dt>

[<span data-ttu-id="e5508-121">Inscription des serveurs COM</span><span class="sxs-lookup"><span data-stu-id="e5508-121">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="e5508-122">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="e5508-122">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> </dl>

 

 




