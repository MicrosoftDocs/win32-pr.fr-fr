---
title: Entrées système pour les compresseurs, les décompresseurs et les convertisseurs
description: Entrées système pour les compresseurs, les décompresseurs et les convertisseurs
ms.assetid: b27bbd5b-a218-49bb-b179-b24ce39869a1
keywords:
- Video for Windows (VFW), entrées système du compresseur
- VFW (vidéo pour Windows), entrées du système de compression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b46d9c6fd8974511698bcb687c580e68be3757ee
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675066"
---
# <a name="system-entries-for-compressors-decompressors-and-renderers"></a>Entrées système pour les compresseurs, les décompresseurs et les convertisseurs

Le système utilise des entrées du Registre pour rechercher les pilotes VCM. Ces entrées se présentent sous la forme de codes de 2 4 caractères séparés par un point. Le premier code à quatre caractères est défini par le système et peut prendre l’une des valeurs suivantes :



| Code à quatre caractères | Description                               |
|---------------------|-------------------------------------------|
| VIDC              | Identifie les compresseurs et les décompresseurs. |
| "VIDS"              | Identifie les convertisseurs de flux vidéo.        |
| "TXTS"              | Identifie les convertisseurs de flux de texte.         |
| "AUDS"              | Identifie les gestionnaires de flux audio.         |



 

Les convertisseurs personnalisés peuvent définir leurs propres codes à quatre caractères.

Le deuxième code à quatre caractères est défini par le pilote. En règle générale, le deuxième code de quatre caractères correspond au type de données que le pilote peut gérer.

Lors de l’ouverture d’un pilote VCM, une application spécifie le type de pilote et le type de gestionnaire de données dont il a besoin. En règle générale, ces informations proviennent de l’en-tête de flux. Le système tente d’ouvrir le gestionnaire de données spécifié, mais en cas d’échec, le système recherche un pilote doté du gestionnaire requis dans le registre.

Lors de la recherche du pilote, le système tente de faire correspondre les codes à quatre caractères spécifiés pour le type de pilote et le gestionnaire de données avec ceux spécifiés dans l’entrée du pilote. Par exemple, si une application spécifie le compresseur MSSQ, le système recherche l’entrée de pilote VIDC. MSSQ dans le registre. S’il ne trouve pas de correspondance, il ouvre chaque pilote correspondant au type de pilote et en trouve un qui peut gérer le type de données que votre application spécifie. Dans l’exemple précédent, si le système n’a pas pu trouver VIDC. MSSQ, il ouvre tous les pilotes avec le code à quatre caractères « VIDC » et en trouve un qui peut gérer les données.

 

 




