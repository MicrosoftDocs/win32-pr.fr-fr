---
title: Conversion
description: Utilisé par la boîte de dialogue Convertir pour déterminer les formats qu’une application peut lire et écrire.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Conversion de la clé de registre COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272090fb48b214daecd6350e6966350861366341fae055298a2fb2c90c9fb983
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993480"
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

## <a name="remarks"></a>Remarques

Les informations de conversion sont utilisées par la boîte de dialogue **convertir** pour déterminer les formats qu’une application peut lire et écrire. un format de fichier délimité par des virgules est indiqué par un nombre s’il s’agit de l’un des formats de presse-papiers définis dans Windows. h. une chaîne indique que le format n’est pas défini dans Windows. h (private). Dans ce cas, le format lisible et accessible en écriture est \_ plan CF (privé).

La valeur *rformat* spécifie le format de fichier qu’une application peut lire (conversion à partir de).

La valeur *rwformat* spécifie le format de fichier qu’une application peut lire et écrire (activer en tant que).

 

 




