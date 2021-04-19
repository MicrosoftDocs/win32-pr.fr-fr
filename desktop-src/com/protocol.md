---
title: Protocol
description: Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clé de Registre du protocole COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511441"
---
# <a name="protocol"></a>Protocol

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

## <a name="remarks"></a>Notes

L’entrée **StdFileEditing** spécifie les informations de compatibilité OLE 1. Elle doit être présente uniquement si les objets de cette classe peuvent être insérés dans des conteneurs OLE 1.

**Serveur** spécifie le chemin d’accès complet à l’application serveur OLE 2 et le **verbe** spécifie les verbes. Le verbe 0 est le verbe principal et les verbes supplémentaires doivent être numérotés consécutivement.

 

 




