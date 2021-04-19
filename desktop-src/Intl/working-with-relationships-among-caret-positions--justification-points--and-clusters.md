---
description: Le tableau suivant présente les différentes méthodes que l’application peut utiliser pour gérer le signe insertion, la justification et les clusters.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d051d008a8ae991b2858be598713fe9ad1adc0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517508"
---
# <a name="working-with-relationships-among-caret-positions-justification-points-and-clusters"></a>Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters

Le tableau suivant présente les différentes méthodes que l’application peut utiliser pour gérer le signe insertion, la justification et les clusters.



| Tâche                             | Support Uniscribe                                                                                                                                                                                                                                                              |
|----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Déplacer le signe insertion par cluster de caractères  | Paramètre *pwLogClust* du membre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Saut de ligne entre les caractères | Paramètre *pwLogClust* du membre [**ScriptShape**](/windows/desktop/api/Usp10/nf-usp10-scriptshape) functionThe **FClusterStart** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)<br/> Le membre **fCharStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)<br/> |
| Déplacer le signe insertion par mot               | Le membre **fWordStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Saut de ligne entre les mots      | Le membre **fWordStop** de la structure de [**script \_ LOGATTR**](/windows/win32/api/usp10/ns-usp10-script_logattr)                                                                                                                                                                                            |
| Justification                    | Le membre **uJustification** de la structure de [**script \_ VISATTR**](/windows/win32/api/usp10/ns-usp10-script_visattr)                                                                                                                                                                                       |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 




