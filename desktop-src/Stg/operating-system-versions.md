---
title: Versions de système d’exploitation
description: Ce type de données DWORD doit contenir le type de système d’exploitation dans le mot de poids fort et le numéro de version du système d’exploitation dans le mot de poids faible. Les valeurs possibles pour le système d’exploitation sont répertoriées dans le tableau suivant.
ms.assetid: 318e277b-a797-45a5-87c5-25b91fdf278d
keywords:
- Versions de système d’exploitation stockage structuré
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd5de916d354a721834b9a10651c36d3bf389e28
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106509662"
---
# <a name="operating-system-versions"></a>Versions de système d’exploitation

Ce type de données **DWORD** doit contenir le type de système d’exploitation dans le mot de poids fort et le numéro de version du système d’exploitation dans le mot de poids faible. Les valeurs possibles pour le système d’exploitation sont répertoriées dans le tableau suivant.



| Système d’exploitation       | Valeur  |
|------------------------|--------|
| 32 bits Windows (Win32) | 0x0002 |
| Macintosh              | 0x0001 |
| Windows 16 bits (Win16) | 0x0000 |



 

Pour les systèmes d’exploitation Microsoft Windows, la version du système d’exploitation est le mot de poids faible retourné par la fonction [**GetVersion**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getversion) . Pour Microsoft Windows, l’exemple de code suivant définit correctement la version du système d’exploitation d’origine.

``` syntax
#ifdef WIN32 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 2 ) ; 
#else 
    dwOSVer = (DWORD)MAKELONG( LOWORD(GetVersion()), 0 ) ; 
#endif
```

 

 