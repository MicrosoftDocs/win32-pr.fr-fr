---
description: Sur les systèmes d’exploitation 64 bits, Windows Installer pouvez appeler des actions personnalisées qui sont compilées pour des systèmes 32 bits ou 64 bits.
ms.assetid: e9ef684d-e22c-43b3-a5ea-75a4cce663c1
title: Utilisation d’actions personnalisées 64 bits
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1465f1b82d18c8e07d95e6d3ab08e9da6827bf1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952395"
---
# <a name="using-64-bit-custom-actions"></a>Utilisation d’actions personnalisées 64 bits

Sur les systèmes d’exploitation 64 bits, Windows Installer pouvez appeler des actions personnalisées qui sont compilées pour des systèmes 32 bits ou 64 bits. Une action personnalisée 64 bits basée sur des [scripts](scripts.md) doit être explicitement marquée comme une action personnalisée de 64 bits en ajoutant le bit **msidbCustomActionType64BitScript** au type numérique de l’action personnalisée dans la colonne type de la [table CustomAction](customaction-table.md). Les actions personnalisées basées sur des [fichiers exécutables](executable-files.md) ou des [bibliothèques de liens dynamiques](dynamic-link-libraries.md) conformes aux systèmes d’exploitation 64 bits ne nécessitent pas l’inclusion de ce bit supplémentaire dans la colonne type de la table CustomAction.

Pour plus d’informations, consultez [actions personnalisées 64 bits](64-bit-custom-actions.md).

 

 



