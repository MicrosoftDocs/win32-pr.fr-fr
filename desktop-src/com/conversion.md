---
title: Conversion
description: Utilisé par la boîte de dialogue Convertir pour déterminer les formats qu’une application peut lire et écrire.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversion de la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507438"
---
# <a name="conversion"></a>Conversion

Utilisé par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire.

## <a name="registry-entry"></a>Entrée de Registre

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a>Notes

Les informations de conversion sont utilisées par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire. Un format de fichier délimité par des virgules est indiqué par un nombre s’il s’agit de l’un des formats de presse-papiers définis dans Windows. h. Une chaîne indique que le format n’est pas défini dans Windows. h (privé). Dans ce cas, le format lisible et accessible en écriture est \_ plan CF (privé).

La valeur *rformat* spécifie le format de fichier qu’une application peut lire (conversion à partir de).

La valeur *rwformat* spécifie le format de fichier qu’une application peut lire et écrire (activer en tant que).

 

 




