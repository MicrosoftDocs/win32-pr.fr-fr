---
title: Définition de la sécurité Process-Wide
description: Il existe plusieurs façons de définir la sécurité au niveau du processus.
ms.assetid: 596ba257-cbde-4243-aa29-78749304867a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acc483bc6f52963eadc12891e657db1cbe51fb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511456"
---
# <a name="setting-process-wide-security"></a><span data-ttu-id="a4b2c-103">Définition de la sécurité Process-Wide</span><span class="sxs-lookup"><span data-stu-id="a4b2c-103">Setting Process-Wide Security</span></span>

<span data-ttu-id="a4b2c-104">Il existe plusieurs façons de définir la sécurité au niveau du processus.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-104">There are several ways to set process-wide security.</span></span> <span data-ttu-id="a4b2c-105">La première méthode, à l’aide de l’outil Dcomcnfg.exe, est plus simple, car elle ne nécessite pas de programmation.</span><span class="sxs-lookup"><span data-stu-id="a4b2c-105">The first way, using the Dcomcnfg.exe tool, is easiest because it requires no programming.</span></span> <span data-ttu-id="a4b2c-106">La deuxième technique offre au programmeur davantage de contrôle et nécessite un appel à [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="a4b2c-106">The second technique offers the programmer more control, and it requires a call to [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="a4b2c-107">Une autre technique consiste à définir la sécurité au niveau du processus dans le registre à l’aide de la clé [AppID](appid-key.md) .</span><span class="sxs-lookup"><span data-stu-id="a4b2c-107">Another technique is to set process-wide security in the registry by using the [AppID](appid-key.md) key.</span></span>

<span data-ttu-id="a4b2c-108">Pour plus d’informations sur ces techniques, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4b2c-108">For more information about these techniques, see the following topics:</span></span>

-   [<span data-ttu-id="a4b2c-109">Définition de la sécurité Process-Wide à l’aide de DCOMCNFG</span><span class="sxs-lookup"><span data-stu-id="a4b2c-109">Setting Process-Wide Security Using DCOMCNFG</span></span>](setting-processwide-security-using-dcomcnfg.md)
-   [<span data-ttu-id="a4b2c-110">Définition de la sécurité Process-Wide avec CoInitializeSecurity</span><span class="sxs-lookup"><span data-stu-id="a4b2c-110">Setting Process-Wide Security with CoInitializeSecurity</span></span>](setting-processwide-security-with-coinitializesecurity.md)
-   [<span data-ttu-id="a4b2c-111">Définition de la sécurité Process-Wide dans le registre</span><span class="sxs-lookup"><span data-stu-id="a4b2c-111">Setting Process-Wide Security Through the Registry</span></span>](setting-processwide-security-through-the-registry.md)

## <a name="related-topics"></a><span data-ttu-id="a4b2c-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4b2c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4b2c-113">Définition de la sécurité au niveau du proxy d’interface</span><span class="sxs-lookup"><span data-stu-id="a4b2c-113">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)
</dt> <dt>

[<span data-ttu-id="a4b2c-114">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="a4b2c-114">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




