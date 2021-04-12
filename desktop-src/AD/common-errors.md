---
title: Erreurs courantes (AD DS)
description: Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.
ms.assetid: 844d4280-a943-4906-b0c6-0c650ef9c114
ms.tgt_platform: multiple
keywords:
- Erreurs courantes AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c719aad39690932de51c58d0f8081a8c855980bd
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/11/2019
ms.locfileid: "104462675"
---
# <a name="common-errors-ad-ds"></a><span data-ttu-id="90187-104">Erreurs courantes (AD DS)</span><span class="sxs-lookup"><span data-stu-id="90187-104">Common Errors (AD DS)</span></span>

<span data-ttu-id="90187-105">Le tableau suivant contient une liste d’erreurs courantes qui peuvent se produire en fonction de l’étendue du groupe imbriqué.</span><span class="sxs-lookup"><span data-stu-id="90187-105">The following table contains a list of common errors that can occur based on the scope of the group being nested.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90187-106">HRESULT</span><span class="sxs-lookup"><span data-stu-id="90187-106">HRESULT</span></span></th>
<th><span data-ttu-id="90187-107">Description</span><span class="sxs-lookup"><span data-stu-id="90187-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="90187-108">0x8007001F</span><span class="sxs-lookup"><span data-stu-id="90187-108">0x8007001F</span></span></td>
<td><span data-ttu-id="90187-109">Échec général.</span><span class="sxs-lookup"><span data-stu-id="90187-109">General failure.</span></span> <span data-ttu-id="90187-110">Cette erreur se produit si vous tentez d’effectuer les opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="90187-110">This error occurs if you attempt to:</span></span>
<ul>
<li><span data-ttu-id="90187-111">Ajoutez un groupe de domaine local à un groupe global ou universel ou à un groupe de domaine local dans un autre domaine.</span><span class="sxs-lookup"><span data-stu-id="90187-111">Add a domain local group to a global or universal group or a domain local group in another domain.</span></span> <span data-ttu-id="90187-112">Les groupes locaux de domaine peuvent uniquement être ajoutés en tant que membres à d’autres groupes locaux de domaine dans le même domaine.</span><span class="sxs-lookup"><span data-stu-id="90187-112">Domain local groups can only be added as members to other domain local groups in the same domain.</span></span></li>
<li><span data-ttu-id="90187-113">Ajoutez un groupe universel à un groupe global.</span><span class="sxs-lookup"><span data-stu-id="90187-113">Add a universal group to a global group.</span></span> <span data-ttu-id="90187-114">Les groupes universels peuvent être ajoutés à des groupes universels et locaux de domaine, mais pas à des groupes globaux.</span><span class="sxs-lookup"><span data-stu-id="90187-114">Universal groups can be added to universal and domain local groups, but not global groups.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="90187-115">0x8007202F</span><span class="sxs-lookup"><span data-stu-id="90187-115">0x8007202F</span></span></td>
<td><span data-ttu-id="90187-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span><span class="sxs-lookup"><span data-stu-id="90187-116"><strong>ERROR_DS_CONSTRAINT_VIOLATION</strong>.</span></span> <span data-ttu-id="90187-117">Cette erreur se produit si vous tentez d’ajouter un groupe de sécurité à un autre groupe dans un domaine s’exécutant en mode mixte.</span><span class="sxs-lookup"><span data-stu-id="90187-117">This error occurs if you attempt to add a security group to another group in a domain running in mixed mode.</span></span> <span data-ttu-id="90187-118">Les groupes de sécurité ne peuvent pas être imbriqués en mode mixte ; les groupes de sécurité peuvent uniquement être imbriqués en mode natif.</span><span class="sxs-lookup"><span data-stu-id="90187-118">Security groups cannot be nested in mixed mode; security groups can only be nested in native mode.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




