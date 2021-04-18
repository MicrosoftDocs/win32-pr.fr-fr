---
title: LibMain. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e309d3c6454901b26f5ab67351033b39d73dd7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106526927"
---
# <a name="libmaincpp"></a>LibMain. COTISATIONS

Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.



| Élément                                  | Description                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| **DllGetClassObject**<br/>      | Point d’entrée de DLL standard pour la localisation des fabriques de classes.<br/>        |
| **DllCanUnloadNow**<br/>        | Point d’entrée de DLL standard pour déterminer si la DLL peut être déchargée.<br/> |
| **LibMain**<br/>                | Point d’entrée de l’initialisation de la DLL standard.<br/>                      |
| **IsCompatibleOleVersion**<br/> | Vérifiez la compatibilité avec l’exécution OLE.<br/>                   |
| **DllMain**<br/>                | Point d’entrée pour la plupart des versions de Windows 2000 ou Windows NT.<br/>     |



 

 

 





