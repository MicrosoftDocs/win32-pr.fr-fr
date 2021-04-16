---
title: Modification des valeurs par défaut de sécurité pour un ordinateur
description: Modification des valeurs par défaut de sécurité pour un ordinateur
ms.assetid: c6d84375-59ea-42d5-87f9-af514b6f7d7c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607e7a17e7db1f8852dff42e62384c730090bbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379583"
---
# <a name="modifying-the-security-defaults-for-a-computer"></a><span data-ttu-id="5f936-103">Modification des valeurs par défaut de sécurité pour un ordinateur</span><span class="sxs-lookup"><span data-stu-id="5f936-103">Modifying the Security Defaults for a Computer</span></span>

<span data-ttu-id="5f936-104">Il n’est pas recommandé de modifier les paramètres de sécurité à l’ensemble du système, car cela affecte toutes les applications serveur COM qui ne définissent pas leur propre sécurité au niveau du processus, et peut les empêcher de fonctionner correctement.</span><span class="sxs-lookup"><span data-stu-id="5f936-104">It is not recommended that you change the system-wide security settings, because this will affect all COM server applications that do not set their own process-wide security, and might prevent them from working properly.</span></span> <span data-ttu-id="5f936-105">Si vous modifiez les paramètres de sécurité à l’ensemble du système pour affecter les paramètres de sécurité d’une application COM particulière, vous devez à la place modifier les paramètres de sécurité à l’ensemble du processus pour cette application COM particulière.</span><span class="sxs-lookup"><span data-stu-id="5f936-105">If you are changing the system-wide security settings to affect the security settings for a particular COM application, then you should instead change the process-wide security settings for that particular COM application.</span></span> <span data-ttu-id="5f936-106">Pour plus d’informations sur la définition de la sécurité au niveau du processus, consultez Définition de la [sécurité Process-Wide](setting-processwide-security.md).</span><span class="sxs-lookup"><span data-stu-id="5f936-106">For more information about setting process-wide security, see [Setting Process-Wide Security](setting-processwide-security.md).</span></span>

<span data-ttu-id="5f936-107">Certaines valeurs du Registre déterminent les paramètres de sécurité des applications qui n’appellent pas [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="5f936-107">Certain values in the registry determine security settings for applications that do not call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="5f936-108">Vous pouvez modifier ces paramètres à l’aide de Dcomcnfg.exe.</span><span class="sxs-lookup"><span data-stu-id="5f936-108">You can modify these settings using Dcomcnfg.exe.</span></span>

<span data-ttu-id="5f936-109">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5f936-109">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="5f936-110">Valeurs de Registre pour la sécurité System-Wide</span><span class="sxs-lookup"><span data-stu-id="5f936-110">Registry Values for System-Wide Security</span></span>](registry-values-for-machine-wide-security.md)
-   [<span data-ttu-id="5f936-111">Définition de la sécurité System-Wide à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="5f936-111">Setting System-Wide Security Using DCOMCNFG</span></span>](setting-machine-wide-security-using-dcomcnfg.md)

## <a name="related-topics"></a><span data-ttu-id="5f936-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f936-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f936-113">Définition de la sécurité au niveau du processus</span><span class="sxs-lookup"><span data-stu-id="5f936-113">Setting Process-wide Security</span></span>](setting-processwide-security.md)
</dt> <dt>

[<span data-ttu-id="5f936-114">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="5f936-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




