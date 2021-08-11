---
title: LibMain. COTISATIONS
description: Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.
ms.assetid: aa05fbd1-509d-4ed6-8a49-1ce11ce54c0e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d2753d2067a7e33f9139836ed6e4c6806e628aa48f87d719a85c31ca6e0c8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118179267"
---
# <a name="libmaincpp"></a>LibMain. COTISATIONS

Dans l’exemple de composant fournisseur, un exemple de code de point d’entrée de DLL standard pour Adssmp.dll se trouve dans LibMain. cpp. Les routines prises en charge sont répertoriées dans le tableau suivant.



| Élément                                  | Description                                                              |
|---------------------------------------|--------------------------------------------------------------------------|
| **DllGetClassObject**<br/>      | Point d’entrée de DLL standard pour la localisation des fabriques de classes.<br/>        |
| **DllCanUnloadNow**<br/>        | Point d’entrée de DLL standard pour déterminer si la DLL peut être déchargée.<br/> |
| **LibMain**<br/>                | Point d’entrée de l’initialisation de la DLL standard.<br/>                      |
| **IsCompatibleOleVersion**<br/> | Vérifiez la compatibilité avec l’exécution OLE.<br/>                   |
| **DllMain**<br/>                | point d’entrée pour la plupart des versions Windows 2000 ou Windows NT.<br/>     |



 

 

 





