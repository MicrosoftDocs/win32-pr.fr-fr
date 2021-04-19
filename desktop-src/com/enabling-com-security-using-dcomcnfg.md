---
title: Activation de la sécurité COM à l’aide de DCOMCNFG
description: Dcomcnfg.exe fournit une interface utilisateur qui permet de modifier certains paramètres du Registre.
ms.assetid: 9aad6b71-47b8-4377-88e5-f463991d9e86
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c01139584b715fccdad923bc5eb3d6a863a63ef8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509990"
---
# <a name="enabling-com-security-using-dcomcnfg"></a><span data-ttu-id="0aea1-103">Activation de la sécurité COM à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0aea1-103">Enabling COM Security Using DCOMCNFG</span></span>

<span data-ttu-id="0aea1-104">Dcomcnfg.exe fournit une interface utilisateur qui permet de modifier certains paramètres du Registre.</span><span class="sxs-lookup"><span data-stu-id="0aea1-104">Dcomcnfg.exe provides a user interface for modifying certain settings in the registry.</span></span> <span data-ttu-id="0aea1-105">En utilisant Dcomcnfg.exe, vous pouvez activer la sécurité à l’échelle de l’ordinateur ou au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="0aea1-105">By using Dcomcnfg.exe, you can enable security either on a computer-wide or a process-wide basis.</span></span> <span data-ttu-id="0aea1-106">Vous pouvez activer la sécurité pour un ordinateur particulier afin que, lorsqu’un processus ne fournit pas ses propres paramètres de sécurité, par programmation ou par le biais de valeurs de Registre, les valeurs définies par Dcomcnfg.exe seront utilisées.</span><span class="sxs-lookup"><span data-stu-id="0aea1-106">You can enable security for a particular computer so that when a process does not provide its own security settings, either programmatically or through registry values, the values set by Dcomcnfg.exe will be used.</span></span> <span data-ttu-id="0aea1-107">Vous pouvez utiliser Dcomcnfg.exe pour activer la sécurité pour une application particulière uniquement.</span><span class="sxs-lookup"><span data-stu-id="0aea1-107">Or you can use Dcomcnfg.exe to enable security for a particular application only.</span></span>

<span data-ttu-id="0aea1-108">Lors de l’activation de la sécurité, il existe deux tâches principales à accomplir :</span><span class="sxs-lookup"><span data-stu-id="0aea1-108">When enabling security, there are two primary tasks to accomplish:</span></span>

-   <span data-ttu-id="0aea1-109">Définissez un niveau d’authentification qui n’a pas la valeur None.</span><span class="sxs-lookup"><span data-stu-id="0aea1-109">Set an authentication level that is not None.</span></span>
-   <span data-ttu-id="0aea1-110">Définissez les autorisations, y compris les autorisations de lancement et d’accès.</span><span class="sxs-lookup"><span data-stu-id="0aea1-110">Set permissions, including both launch and access permissions.</span></span>

<span data-ttu-id="0aea1-111">Les étapes à suivre pour accomplir ces tâches varient selon que vous activez la sécurité pour l’ensemble de l’ordinateur ou uniquement pour une application particulière.</span><span class="sxs-lookup"><span data-stu-id="0aea1-111">The steps taken to accomplish these tasks depend on whether you are enabling security for the whole computer or just for a particular application.</span></span> <span data-ttu-id="0aea1-112">Vous pouvez également définir d’autres valeurs pour l’ordinateur ou l’application.</span><span class="sxs-lookup"><span data-stu-id="0aea1-112">Also, you may want to set other values for the computer or application.</span></span>

> [!Note]  
> <span data-ttu-id="0aea1-113">Vous devez être administrateur pour exécuter Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="0aea1-113">You must be an administrator to run Dcomcnfg.exe.</span></span>

 

<span data-ttu-id="0aea1-114">Les rubriques suivantes fournissent des procédures pas à pas pour définir la sécurité avec Dcomcnfg.exe :</span><span class="sxs-lookup"><span data-stu-id="0aea1-114">The following topics provide step-by-step procedures on how to set security with Dcomcnfg.exe:</span></span>

-   [<span data-ttu-id="0aea1-115">Définition de la sécurité System-Wide à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0aea1-115">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="0aea1-116">Définition de la sécurité échelle à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="0aea1-116">Setting Processwide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="0aea1-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0aea1-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0aea1-118">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="0aea1-118">Security in COM</span></span>](security-in-com.md)
</dt> <dt>

[<span data-ttu-id="0aea1-119">Désactivation de la sécurité</span><span class="sxs-lookup"><span data-stu-id="0aea1-119">Turning Off Security</span></span>](turning-off-security.md)
</dt> </dl>

 

 




