---
title: Protocole
description: Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clé de Registre du protocole COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7721e4f90a122fcbc519163d80c1e8e549f2b6aa05526d33d9693783abd1276a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130021"
---
# <a name="protocol"></a>Protocole

Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Protocol
         StdFileEditing
            Server = path
            Verb
               0 = verb1
               1 = verb2
               ...
```

## <a name="remarks"></a>Remarques

L’entrée **StdFileEditing** spécifie les informations de compatibilité OLE 1. Elle doit être présente uniquement si les objets de cette classe peuvent être insérés dans des conteneurs OLE 1.

**Serveur** spécifie le chemin d’accès complet à l’application serveur OLE 2 et le **verbe** spécifie les verbes. Le verbe 0 est le verbe principal et les verbes supplémentaires doivent être numérotés consécutivement.

 

 




