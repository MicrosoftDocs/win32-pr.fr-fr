---
title: Protocol
description: Indique que cette classe OLE 2 peut être insérée dans les conteneurs OLE 1.
ms.assetid: 320dff51-ac27-42f3-8c0f-353b29e289d9
keywords:
- Clé de Registre du protocole COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 176cb3fce826a6416270fc35a902621521341e6a
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363336"
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

## <a name="remarks"></a>Remarques

L’entrée **StdFileEditing** spécifie les informations de compatibilité OLE 1. Elle doit être présente uniquement si les objets de cette classe peuvent être insérés dans des conteneurs OLE 1.

**Serveur** spécifie le chemin d’accès complet à l’application serveur OLE 2 et le **verbe** spécifie les verbes. Le verbe 0 est le verbe principal et les verbes supplémentaires doivent être numérotés consécutivement.

 

 




