---
description: Cette rubrique vous indique comment contrôler la visibilité des verbes.
title: Comment supprimer et contrôler la visibilité des verbes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f689d8b93ce9facb62b654f3f8be62f665e001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202776"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a><span data-ttu-id="7d11d-103">Comment supprimer et contrôler la visibilité des verbes</span><span class="sxs-lookup"><span data-stu-id="7d11d-103">How to Suppress and Control Verb Visibility</span></span>

<span data-ttu-id="7d11d-104">Cette rubrique vous indique comment contrôler la visibilité des verbes.</span><span class="sxs-lookup"><span data-stu-id="7d11d-104">This topic tells you how to control verb visibility.</span></span>

## <a name="instructions"></a><span data-ttu-id="7d11d-105">Instructions</span><span class="sxs-lookup"><span data-stu-id="7d11d-105">Instructions</span></span>


<span data-ttu-id="7d11d-106">Vous pouvez utiliser les paramètres de stratégie Windows pour contrôler la visibilité des verbes.</span><span class="sxs-lookup"><span data-stu-id="7d11d-106">You can use Windows policy settings to control verb visibility.</span></span> <span data-ttu-id="7d11d-107">Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une sous-clé **SuppressionPolicy** ou une valeur Guid **SuppressionPolicyEx** à la sous-clé de Registre du verbe.</span><span class="sxs-lookup"><span data-stu-id="7d11d-107">Verbs can be suppressed through policy settings by adding a **SuppressionPolicy** subkey or a **SuppressionPolicyEx** GUID value to the verb's registry subkey.</span></span> <span data-ttu-id="7d11d-108">Définissez la valeur de la sous-clé **SuppressionPolicy** sur l’ID de stratégie.</span><span class="sxs-lookup"><span data-stu-id="7d11d-108">Set the value of the **SuppressionPolicy** subkey to the policy ID.</span></span> <span data-ttu-id="7d11d-109">Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="7d11d-109">If the policy is turned on, the verb and its associated shortcut menu entry are suppressed.</span></span> <span data-ttu-id="7d11d-110">Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .</span><span class="sxs-lookup"><span data-stu-id="7d11d-110">For possible policy ID values, see the [**RESTRICTIONS**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) enumeration.</span></span>

 

 



