---
title: Shell (COM)
description: fournit les informations d’impression et d’ouverture de fichier Windows 3,1.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Clé de Registre Shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363335"
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

 

 




