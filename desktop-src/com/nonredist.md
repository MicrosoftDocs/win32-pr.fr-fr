---
title: Pas de REDIM
description: Ajoute des noms à la liste des fichiers qui ne doivent pas être exportés lorsque les applications COM+ sont empaquetées pour être installées sur d’autres ordinateurs. Notez qu’il s’agit d’une sous-clé, et non d’une valeur.
ms.assetid: c50e20e4-1a25-4978-ab84-8f7b4b2f6069
keywords:
- Valeur de Registre inversée COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d537208ecaf98cec46591966e4ae7d9c205850a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923155"
---
# <a name="nonredist"></a>Pas de REDIM

Ajoute des noms à la liste des fichiers qui ne doivent pas être exportés lorsque les applications COM+ sont empaquetées pour être installées sur d’autres ordinateurs. Notez qu’il s’agit d’une sous-clé, et non d’une valeur.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   NONREDIST
      name1
      name2
```

## <a name="remarks"></a>Notes

Les fichiers que vous ajoutez à la liste sont représentés par des paires nom/valeur stockées sous cette clé. Dans chaque paire nom/valeur, le nom est le nom de fichier et la valeur est réservée.

 

 




