---
title: Imbrication en mode mixte
description: Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.
ms.assetid: e9f50485-db09-4d8c-8cf4-0ee7e78cb133
ms.tgt_platform: multiple
keywords:
- Imbrication en mode mixte AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e54d63d475edf77398a69a519a08f3803f69d67d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839285"
---
# <a name="nesting-in-mixed-mode"></a><span data-ttu-id="0c28f-104">Imbrication en mode mixte</span><span class="sxs-lookup"><span data-stu-id="0c28f-104">Nesting in Mixed Mode</span></span>

<span data-ttu-id="0c28f-105">Cette rubrique répertorie les restrictions des groupes de sécurité dans un domaine en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="0c28f-105">This topic lists the restrictions of security groups in a mixed-mode domain.</span></span>

<span data-ttu-id="0c28f-106">Les groupes de sécurité dans un domaine en mode mixte présentent les restrictions suivantes :</span><span class="sxs-lookup"><span data-stu-id="0c28f-106">Security groups in a mixed-mode domain have the following restrictions:</span></span>

-   <span data-ttu-id="0c28f-107">Les groupes universels ne peuvent pas être créés dans des domaines en mode mixte, car l’étendue universelle est prise en charge uniquement dans les domaines en mode natif Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0c28f-107">Universal groups cannot be created in mixed-mode domains because the universal scope is supported only in Windows 2000 native-mode domains.</span></span>
-   <span data-ttu-id="0c28f-108">Un groupe global peut contenir des comptes appartenant au même domaine que le groupe.</span><span class="sxs-lookup"><span data-stu-id="0c28f-108">A global group can contain accounts from the same domain to which the group belongs.</span></span> <span data-ttu-id="0c28f-109">Un groupe global ne peut pas contenir de groupes universels, de groupes globaux ou de comptes d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="0c28f-109">A global group cannot contain any universal groups, any global group, or an account from another domain.</span></span>
-   <span data-ttu-id="0c28f-110">Un groupe de domaine local peut contenir des groupes globaux et des comptes à partir de n’importe quel domaine ou forêt.</span><span class="sxs-lookup"><span data-stu-id="0c28f-110">A domain local group can contain global groups and accounts from any domain or forest.</span></span> <span data-ttu-id="0c28f-111">Un groupe de domaine local ne peut pas contenir un autre groupe de domaine local.</span><span class="sxs-lookup"><span data-stu-id="0c28f-111">A domain local group cannot contain any other domain local group.</span></span>

<span data-ttu-id="0c28f-112">Sachez que les groupes de distribution peuvent être imbriqués en fonction des règles d’imbrication pour le mode natif.</span><span class="sxs-lookup"><span data-stu-id="0c28f-112">Be aware that distribution groups can be nested according to the nesting rules for native mode.</span></span>

 

 




