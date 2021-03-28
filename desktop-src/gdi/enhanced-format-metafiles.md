---
description: Enhanced-Format les sous-fichiers
ms.assetid: 8d7015cb-5e1d-4805-a7a8-1f8b693e0681
title: Enhanced-Format les sous-fichiers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbae113c65e4dd05e67c155c2323698cd023191
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972686"
---
# <a name="enhanced-format-metafiles"></a>Enhanced-Format les sous-fichiers

Le *métafichier de format amélioré* se compose des éléments suivants :

-   Un en-tête
-   Tableau de handles vers des objets GDI
-   Une palette privée
-   Tableau d’enregistrements de métafichier

Les sous-fichiers améliorés fournissent une véritable indépendance des appareils. Vous pouvez considérer l’image stockée dans un métafichier amélioré comme un « instantané » de l’affichage vidéo pris à un moment donné. Cet instantané conserve ses dimensions, quel que soit l’endroit où il apparaît sur une imprimante, un traceur, le bureau ou dans la zone cliente d’une application.

Vous pouvez utiliser des fichiers de base de fichiers améliorés pour stocker une image créée à l’aide des fonctions GDI (y compris les nouvelles fonctions de transformation et de chemin d’accès). Étant donné que le format de métafichier amélioré est standardisé, les images stockées dans ce format peuvent être copiées d’une application à une autre. en effet, étant donné que les images sont véritablement indépendantes des appareils, elles sont assurées de conserver leur forme et leur proportion sur n’importe quel périphérique de sortie.

-   [Enregistrements de métafichiers améliorés](enhanced-metafile-records.md)
-   [Création de métafichiers améliorée](enhanced-metafile-creation.md)
-   [Opérations de métafichier améliorées](enhanced-metafile-operations.md)

 

 



