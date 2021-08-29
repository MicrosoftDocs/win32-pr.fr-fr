---
description: sur les systèmes d’exploitation 64 bits, Windows Installer peut appeler des actions personnalisées qui ont été compilées pour des systèmes 32 bits ou 64 bits.
ms.assetid: fc370ab4-93f3-4e1e-9468-3454d4fee0be
title: Actions personnalisées 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9bc3c3e664d8cfb4a94e089eef403255b2b4b18ad9729342bd9aedbe68f5710
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119066539"
---
# <a name="64-bit-custom-actions"></a>Actions personnalisées 64 bits

sur les systèmes d’exploitation 64 bits, Windows Installer peut appeler des actions personnalisées qui ont été compilées pour des systèmes 32 bits ou 64 bits.

Une action personnalisée 64 bits basée sur des [scripts](scripts.md) doit être marquée explicitement comme une action personnalisée 64 bits en ajoutant le bit **msidbCustomActionType64BitScript** au type numérique actions personnalisées dans la colonne type de la [table CustomAction](customaction-table.md).



| Constante                             | Valeur hexadécimale | Decimal | Signification                                                           |
|--------------------------------------|-------------|---------|-------------------------------------------------------------------|
| **msidbCustomActionType64BitScript** | 0x0001000   | 4096    | Il s’agit d’une action personnalisée 64 bits écrite dans des [scripts](scripts.md). |



 

Les actions personnalisées basées sur des [fichiers exécutables](executable-files.md) ou des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) qui ont été respectées pour un système d’exploitation 64 bits ne nécessitent pas l’inclusion de ce bit supplémentaire dans la colonne type de la table CustomAction.

 

 



