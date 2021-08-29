---
title: Shell (COM)
description: fournit les informations d’impression et d’ouverture de fichier Windows 3,1.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Clé de Registre Shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ebbc83642896aa22f33b315e26097760f7311ec93d938cb0440a10e0aae049
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129901"
---
# <a name="shell-com"></a>Shell (COM)

fournit les informations d’impression et d' **ouverture de fichier** Windows 3,1.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes
   {ProgID}
      Shell
         Open
            command = path %1
         Print
            command = path %1
```

## <a name="remarks"></a>Remarques

Ces entrées doivent fournir le chemin d’accès et le nom de fichier de l’application.

 

 




