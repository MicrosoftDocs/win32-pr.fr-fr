---
title: Modification de l’étendue ou du type d’un groupe
description: Cette rubrique montre comment modifier l’étendue ou le type d’un groupe dans des domaines en mode natif.
ms.assetid: bdae7bc9-072a-4063-9562-8e0fcb1b7937
ms.tgt_platform: multiple
keywords:
- regroupe Active Directory, en modifiant l’étendue ou le type d’un groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65c64b4a2dafe4bf6c0e65463ef16e0270c0be3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671005"
---
# <a name="changing-a-groups-scope-or-type"></a><span data-ttu-id="b55eb-104">Modification de l’étendue ou du type d’un groupe</span><span class="sxs-lookup"><span data-stu-id="b55eb-104">Changing a Group's Scope or Type</span></span>

<span data-ttu-id="b55eb-105">La modification d’une étendue de groupe ou d’un type n’est pas autorisée dans les domaines en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="b55eb-105">Changing a group scope or type is not allowed in mixed-mode domains.</span></span> <span data-ttu-id="b55eb-106">Toutefois, les conversions suivantes sont autorisées dans les domaines en mode natif :</span><span class="sxs-lookup"><span data-stu-id="b55eb-106">However, the following conversions are allowed in native-mode domains:</span></span>

<span data-ttu-id="b55eb-107">Groupe global vers groupe universel : cela est autorisé uniquement si le groupe global n’est pas membre d’un autre groupe global.</span><span class="sxs-lookup"><span data-stu-id="b55eb-107">Global group to universal group: This is only allowed if the global group is not a member of another global group.</span></span>

<span data-ttu-id="b55eb-108">Groupe de domaine local vers groupe universel : le groupe de domaine local en cours de conversion ne peut pas contenir un autre groupe de domaine local.</span><span class="sxs-lookup"><span data-stu-id="b55eb-108">Domain local group to universal group: The domain local group being converted cannot contain another domain local group.</span></span>

<span data-ttu-id="b55eb-109">Groupe universel à groupe global ou groupe de domaine local : pour la conversion en groupe global, le groupe universel en cours de conversion ne peut pas contenir des utilisateurs ou des groupes globaux d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="b55eb-109">Universal group to global or domain local group: For conversion to global group, the universal group being converted cannot contain users or global groups from another domain.</span></span> <span data-ttu-id="b55eb-110">Pour la conversion en groupe de domaine local, le groupe universel en cours de conversion ne peut pas être membre d’un groupe universel ou d’un groupe de domaine local d’un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="b55eb-110">For conversion to domain local group, the universal group being converted cannot be a member of any universal group or a domain local group from another domain.</span></span>

<span data-ttu-id="b55eb-111">En mode natif, un type de groupe peut être converti librement entre des groupes de sécurité et des groupes de distribution.</span><span class="sxs-lookup"><span data-stu-id="b55eb-111">In native mode, a group type can be converted freely between security groups and distribution groups.</span></span>

<span data-ttu-id="b55eb-112">Sachez que si un groupe est utilisé pour définir le contrôle d’accès, la modification de l’étendue ou du type peut affecter les entrées de contrôle d’accès (ACE) qui contiennent ce groupe.</span><span class="sxs-lookup"><span data-stu-id="b55eb-112">Be aware that if a group is used to set access control, changing the scope or type can affect the access control entries (ACEs) that contain that group.</span></span> <span data-ttu-id="b55eb-113">Le système de sécurité ignorera les ACE qui contiennent des groupes qui ne sont pas des groupes de sécurité.</span><span class="sxs-lookup"><span data-stu-id="b55eb-113">The security system will ignore ACEs that contain groups that are not security groups.</span></span>

 

 




