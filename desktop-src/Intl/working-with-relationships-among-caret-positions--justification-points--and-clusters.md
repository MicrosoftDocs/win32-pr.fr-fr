---
description: Le tableau suivant présente les différentes méthodes que l’application peut utiliser pour gérer le signe insertion, la justification et les clusters.
ms.assetid: 950a24b4-62ab-4eaf-ac15-87434d3c28c0
title: Utilisation des relations entre les positions du signe insertion, les points de justification et les clusters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3272fc7284ff0d3223cf2b36a3b764e273bcec66dadc24cc50bf0393ded9b9ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119680859"
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

 

 




