---
description: Le \_ droit accès à la sécurité du système Access \_ contrôle la possibilité d’accéder ou de définir la liste SACL dans un descripteur de sécurité d’objets. Le système accorde ce droit d’accès si le \_ \_ privilège nom de sécurité se est activé dans le jeton d’accès du thread demandeur.
ms.assetid: 88198243-dae5-49ac-9d54-bfae7a3a0b1a
title: Droit d’accès SACL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2366f30748a93294d4f30122102d656fb2590d34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516046"
---
# <a name="sacl-access-right"></a><span data-ttu-id="f2193-104">Droit d’accès SACL</span><span class="sxs-lookup"><span data-stu-id="f2193-104">SACL Access Right</span></span>

<span data-ttu-id="f2193-105">Le \_ droit accès à la sécurité du système Access \_ contrôle la capacité à récupérer ou à définir la liste SACL dans le [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly)d’un objet.</span><span class="sxs-lookup"><span data-stu-id="f2193-105">The ACCESS\_SYSTEM\_SECURITY access right controls the ability to get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly).</span></span> <span data-ttu-id="f2193-106">Le système accorde ce droit d’accès uniquement si le \_ \_ privilège nom de sécurité se est activé dans le [*jeton d’accès*](/windows/desktop/SecGloss/a-gly) du thread demandeur.</span><span class="sxs-lookup"><span data-stu-id="f2193-106">The system grants this access right only if the SE\_SECURITY\_NAME privilege is enabled in the [*access token*](/windows/desktop/SecGloss/a-gly) of the requesting thread.</span></span>

<span data-ttu-id="f2193-107">**Pour accéder à la liste SACL d’un objet**</span><span class="sxs-lookup"><span data-stu-id="f2193-107">**To access an object's SACL**</span></span>

1.  <span data-ttu-id="f2193-108">Appelez la fonction [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour activer le \_ privilège de nom de sécurité se \_ .</span><span class="sxs-lookup"><span data-stu-id="f2193-108">Call the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function to enable the SE\_SECURITY\_NAME privilege.</span></span>
2.  <span data-ttu-id="f2193-109">Demandez le droit accès à la \_ sécurité du système Access \_ lorsque vous ouvrez un handle vers l’objet.</span><span class="sxs-lookup"><span data-stu-id="f2193-109">Request the ACCESS\_SYSTEM\_SECURITY access right when you open a handle to the object.</span></span>
3.  <span data-ttu-id="f2193-110">Obtenir ou définir la liste SACL de l’objet à l’aide d’une fonction telle que [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) ou [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span><span class="sxs-lookup"><span data-stu-id="f2193-110">Get or set the object's SACL by using a function such as [**GetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getsecurityinfo) or [**SetSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setsecurityinfo).</span></span>
4.  <span data-ttu-id="f2193-111">Appelez [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) pour désactiver le \_ privilège de nom de sécurité se \_ .</span><span class="sxs-lookup"><span data-stu-id="f2193-111">Call [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) to disable the SE\_SECURITY\_NAME privilege.</span></span>

<span data-ttu-id="f2193-112">Pour accéder à une liste SACL à l’aide des fonctions [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) ou [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) , activez le \_ privilège nom de sécurité se \_ .</span><span class="sxs-lookup"><span data-stu-id="f2193-112">To access a SACL using the [**GetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-getnamedsecurityinfoa) or [**SetNamedSecurityInfo**](/windows/desktop/api/Aclapi/nf-aclapi-setnamedsecurityinfoa) functions, enable the SE\_SECURITY\_NAME privilege.</span></span> <span data-ttu-id="f2193-113">La fonction demande en interne le droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="f2193-113">The function internally requests the access right.</span></span>

<span data-ttu-id="f2193-114">Le droit d’accès à la \_ sécurité du système \_ d’accès n’est pas valide dans une liste DACL, car les DACL ne contrôlent pas l’accès à une liste SACL.</span><span class="sxs-lookup"><span data-stu-id="f2193-114">The ACCESS\_SYSTEM\_SECURITY access right is not valid in a DACL because DACLs do not control access to a SACL.</span></span> <span data-ttu-id="f2193-115">Toutefois, vous pouvez utiliser le droit accès à la \_ sécurité du système \_ dans une liste SACL pour auditer les tentatives d’utilisation du droit d’accès.</span><span class="sxs-lookup"><span data-stu-id="f2193-115">However, you can use the ACCESS\_SYSTEM\_SECURITY access right in a SACL to audit attempts to use the access right.</span></span>

 

 
