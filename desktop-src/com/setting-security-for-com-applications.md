---
title: Définition de la sécurité pour les applications COM
description: Définition de la sécurité pour les applications COM
ms.assetid: 5b615007-e04b-41be-872c-20e0ea818ff1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a8dd705015aaa2ca1965d07c556ff3d55aada00
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840902"
---
# <a name="setting-security-for-com-applications"></a><span data-ttu-id="c657c-103">Définition de la sécurité pour les applications COM</span><span class="sxs-lookup"><span data-stu-id="c657c-103">Setting Security for COM Applications</span></span>

<span data-ttu-id="c657c-104">Il existe plusieurs façons de mieux contrôler la sécurité de vos applications.</span><span class="sxs-lookup"><span data-stu-id="c657c-104">There are several ways you can help control security for your applications.</span></span> <span data-ttu-id="c657c-105">Vous pouvez modifier les paramètres de sécurité par défaut d’un ordinateur, qui sont utilisés par toutes les applications de l’ordinateur qui ne fournissent pas leurs propres valeurs de sécurité.</span><span class="sxs-lookup"><span data-stu-id="c657c-105">You can change a computer's default security settings, which are used by all applications on the computer that do not supply their own security values.</span></span> <span data-ttu-id="c657c-106">Vous pouvez définir la sécurité pour un processus particulier, à l’aide de Dcomcnfg.exe ou en appelant [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span><span class="sxs-lookup"><span data-stu-id="c657c-106">You can set security for a particular process, either by using Dcomcnfg.exe or by calling [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity).</span></span> <span data-ttu-id="c657c-107">Vous pouvez également contrôler par programmation les paramètres de sécurité au niveau du proxy d’interface.</span><span class="sxs-lookup"><span data-stu-id="c657c-107">You can also programmatically control security settings at the interface proxy level.</span></span>

<span data-ttu-id="c657c-108">Les rubriques suivantes fournissent des procédures qui expliquent comment définir la sécurité :</span><span class="sxs-lookup"><span data-stu-id="c657c-108">The following topics provide procedures that explain how to set security:</span></span>

-   [<span data-ttu-id="c657c-109">Modification des valeurs par défaut de sécurité pour un ordinateur</span><span class="sxs-lookup"><span data-stu-id="c657c-109">Modifying the Security Defaults for a Computer</span></span>](modifying-the-security-defaults-for-a-computer.md)
-   [<span data-ttu-id="c657c-110">Définition de la sécurité Process-Wide</span><span class="sxs-lookup"><span data-stu-id="c657c-110">Setting Process-Wide Security</span></span>](setting-processwide-security.md)
-   [<span data-ttu-id="c657c-111">Définition de la sécurité au niveau du proxy d’interface</span><span class="sxs-lookup"><span data-stu-id="c657c-111">Setting Security at the Interface Proxy Level</span></span>](setting-security-at-the-interface-proxy-level.md)

## <a name="related-topics"></a><span data-ttu-id="c657c-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c657c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c657c-113">Sécurité dans COM</span><span class="sxs-lookup"><span data-stu-id="c657c-113">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




