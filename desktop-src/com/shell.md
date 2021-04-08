---
title: Shell (COM)
description: Fournit les informations d’impression et d’ouverture de fichier du shell Windows 3,1.
ms.assetid: 15e329f2-ed64-4940-aa00-63edbd283b07
keywords:
- Clé de Registre Shell COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1acf4a62d72892d1cd25a5f2276e71d52ab7f700
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739348"
---
# <a name="shell-com"></a>Shell (COM)

Fournit les informations d’impression et d' **ouverture de fichier** du shell Windows 3,1.

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

## <a name="remarks"></a>Notes

Ces entrées doivent fournir le chemin d’accès et le nom de fichier de l’application.

 

 




