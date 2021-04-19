---
description: Un propriétaire d’objets dispose implicitement \_ d’un accès en écriture à l’objet DAC. Cela signifie que le propriétaire peut modifier la liste de contrôle d’accès discrétionnaire des objets (DACL, Discretionary Access Control List) et peut donc contrôler l’accès à l’objet.
ms.assetid: 16144f38-3416-4594-b5e4-ca84fcbdddc9
title: Propriétaire d’un nouvel objet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32f16124d84e17a075c78c676465ad753fcc12db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106533983"
---
# <a name="owner-of-a-new-object"></a><span data-ttu-id="3c9f1-104">Propriétaire d’un nouvel objet</span><span class="sxs-lookup"><span data-stu-id="3c9f1-104">Owner of a New Object</span></span>

<span data-ttu-id="3c9f1-105">Le propriétaire d’un objet dispose implicitement \_ d’un accès en écriture à l’objet de la DAC.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-105">An object's owner implicitly has WRITE\_DAC access to the object.</span></span> <span data-ttu-id="3c9f1-106">Cela signifie que le propriétaire peut modifier la liste de contrôle d’accès discrétionnaire de l’objet (DACL, [*Discretionary Access Control List*](/windows/desktop/SecGloss/d-gly) ) et peut donc contrôler l’accès à l’objet.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-106">This means that the owner can modify the object's [*discretionary access control list*](/windows/desktop/SecGloss/d-gly) (DACL), and thus, can control access to the object.</span></span>

<span data-ttu-id="3c9f1-107">Le propriétaire d’un nouvel objet est l’identificateur de [*sécurité*](/windows/desktop/SecGloss/s-gly) (SID) du propriétaire par défaut du jeton [*principal*](/windows/desktop/SecGloss/p-gly) ou d' [*emprunt d’identité*](/windows/desktop/SecGloss/i-gly) du [*processus*](/windows/desktop/SecGloss/p-gly)de création.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-107">The owner of a new object is the default owner [*security identifier*](/windows/desktop/SecGloss/s-gly) (SID) from the [*primary*](/windows/desktop/SecGloss/p-gly) or [*impersonation token*](/windows/desktop/SecGloss/i-gly) of the creating [*process*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="3c9f1-108">Pour récupérer ou définir le propriétaire par défaut dans un [*jeton d’accès*](/windows/desktop/SecGloss/a-gly), appelez la fonction [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) ou [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) avec la structure du [**\_ propriétaire du jeton**](/windows/desktop/api/Winnt/ns-winnt-token_owner) .</span><span class="sxs-lookup"><span data-stu-id="3c9f1-108">To get or set the default owner in an [*access token*](/windows/desktop/SecGloss/a-gly), call the [**GetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-gettokeninformation) or [**SetTokenInformation**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-settokeninformation) function with the [**TOKEN\_OWNER**](/windows/desktop/api/Winnt/ns-winnt-token_owner) structure.</span></span> <span data-ttu-id="3c9f1-109">Le système ne vous permet pas de définir le propriétaire par défaut d’un jeton sur un SID qui n’est pas valide, tel que le SID d’un autre compte d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-109">The system does not allow you to set a token's default owner to a SID that is not valid, such as the SID of another user's account.</span></span>

<span data-ttu-id="3c9f1-110">Un processus avec le \_ privilège Take \_ appropriation activé peut se définir comme propriétaire d’un objet.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-110">A process with the SE\_TAKE\_OWNERSHIP privilege enabled can set itself as the owner of an object.</span></span> <span data-ttu-id="3c9f1-111">Un processus avec un privilège de nom de restauration de SE \_ \_ activé ou un accès de propriétaire en écriture \_ à l’objet peut définir un SID d’utilisateur ou de groupe valide comme propriétaire d’un objet.</span><span class="sxs-lookup"><span data-stu-id="3c9f1-111">A process with the SE\_RESTORE\_NAME privilege enabled or with WRITE\_OWNER access to the object can set any valid user or group SID as the owner of an object.</span></span>

 

 
