---
title: Système de fichiers résilient
description: Système de fichiers résilient
ms.assetid: 6E5532F9-64BC-4DD7-9873-3FE4E4DE2DD0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab2938f99e232f37d6f36f575c6c2a419adf3b6dbdc2a06bd9c8e243d6ba4884
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882679"
---
# <a name="resilient-file-system"></a>Système de fichiers résilient

## <a name="platform"></a>Plateforme

**serveurs** – Windows Server 2012 

## <a name="description"></a>Description

Le système de fichiers résilient (ReFS) est un nouveau système de fichiers local. Il optimise la disponibilité des données, malgré les erreurs qui pourraient entraîner une perte de données ou des temps d’arrêt. L’intégrité des données garantit que les données critiques de l’entreprise sont protégées contre les erreurs et disponibles si nécessaire. Son architecture est conçue pour fournir une évolutivité et des performances dans une ère qui augmente constamment la taille des jeux de données et les charges de travail dynamiques.

Les principales fonctionnalités de ReFS sont les suivantes :

-   **Intégrité**: ReFS stocke les données afin qu’elles soient protégées contre nombre des erreurs courantes qui peuvent entraîner une perte de données. Les métadonnées du système de fichiers sont toujours protégées. Si vous le souhaitez, les données utilisateur peuvent être protégées par volume, par répertoire ou par fichier. en cas d’endommagement, ReFS peut détecter et, lorsqu’il est configuré avec espaces de stockage, corriger automatiquement les dommages. En cas d’erreur système, ReFS est conçu pour récupérer rapidement à partir de cette erreur, sans perte de données utilisateur.
-   **Disponibilité**: ReFS est conçu pour hiérarchiser la disponibilité des données. Avec ReFS, si une altération se produit et qu’elle ne peut pas être réparée automatiquement, le processus de récupération en ligne est localisé dans la zone d’altération, ce qui ne nécessite pas de temps d’arrêt du volume. En bref, en cas d’endommagement, ReFS reste en ligne.
-   **Scalabilité**: ReFS est conçu pour les tailles de jeux de données actuelles et les tailles de jeux de données de demain. elle est optimisée pour une évolutivité élevée.
-   **Compatibilité des applications**: pour optimiser AppCompat, ReFS prend en charge un sous-ensemble de fonctionnalités NTFS et les API Win32 qui sont largement adoptées.
-   **Identification proactive des erreurs**: les fonctionnalités d’intégrité de ReFS sont exploitées par un scanneur d’intégrité des données (un « épurateur ») qui analyse régulièrement le volume, tente d’identifier une altération latente, puis déclenche de manière proactive une réparation de ces données endommagées.

## <a name="resources"></a>Ressources

-   [génération de Windows 8 billet de Blog : génération du système de fichiers de nouvelle génération pour Windows : ReFS](/archive/blogs/b8/building-the-next-generation-file-system-for-windows-refs)
-   [Compatibilité des applications et références](https://www.microsoft.com/download/en/details.aspx?id=29043)

 

 