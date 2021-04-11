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
# <a name="how-to-suppress-and-control-verb-visibility"></a>Comment supprimer et contrôler la visibilité des verbes

Cette rubrique vous indique comment contrôler la visibilité des verbes.

## <a name="instructions"></a>Instructions


Vous pouvez utiliser les paramètres de stratégie Windows pour contrôler la visibilité des verbes. Les verbes peuvent être supprimés par le biais des paramètres de stratégie en ajoutant une sous-clé **SuppressionPolicy** ou une valeur Guid **SuppressionPolicyEx** à la sous-clé de Registre du verbe. Définissez la valeur de la sous-clé **SuppressionPolicy** sur l’ID de stratégie. Si la stratégie est activée, le verbe et son entrée de menu contextuel associée sont supprimés. Pour connaître les valeurs possibles de l’ID de stratégie, consultez l’énumération [**restrictions**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) .

 

 



