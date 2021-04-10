---
title: Fichiers composés
description: Bien que vous puissiez implémenter vos propres interfaces et objets de stockage structurés, COM fournit une implémentation standard appelée fichiers composés.
ms.assetid: 23b425e6-dfe5-403b-8f43-de6843a03dcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62be79f09afd23e53a569b76ad3e0af46cae2f9e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190870"
---
# <a name="compound-files"></a>Fichiers composés

Bien que vous puissiez implémenter vos propres interfaces et objets de stockage structurés, COM fournit une implémentation standard appelée fichiers composés. L’utilisation de fichiers composés vous fait gagner du travail de codage de votre propre implémentation du stockage structuré et confère plusieurs avantages supplémentaires dérivés de l’adhésion à une norme définie. Ces avantages incluent ce qui suit :

-   **Indépendance du système de fichiers et de la plateforme**. Étant donné que l’implémentation des fichiers composés de COM s’exécute sur les systèmes de fichiers plats existants, les fichiers composés stockés dans le système de fichiers FAT, le système de fichiers NTFS ou les systèmes de fichiers Macintosh peuvent être ouverts par les applications à l’aide de l’un des autres systèmes de fichiers.
-   **Recherche**. Étant donné que les objets distincts d’un fichier composé sont enregistrés dans un format standard et accessibles à l’aide d’interfaces et d’API COM standard, tout utilitaire de navigateur utilisant ces interfaces et ces API peut répertorier les objets dans le fichier, même si les données d’un objet donné peuvent être dans un format propriétaire.
-   **Accès à certaines données internes**. Étant donné que l’implémentation de fichiers composés fournit des méthodes standard d’écriture de certains types de données (informations de synthèse, par exemple), les applications peuvent lire ces données à l’aide des interfaces COM et des API.

 

 




