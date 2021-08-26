---
title: Sortie du compilateur MIDL
description: Avec les fichiers IDL et ACF comme entrée, le compilateur MIDL génère jusqu’à cinq fichiers sources en langage C.
ms.assetid: 151bd643-1da0-4b33-b8a3-3d7037e63319
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aea74b77d8e709d8a71d3c84f457d301bb38d8c35bdccaa77e9e3033d08ed70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120019689"
---
# <a name="midl-compiler-output"></a>Sortie du compilateur MIDL

Avec les fichiers IDL et ACF comme entrée, le compilateur MIDL génère jusqu’à cinq fichiers sources en langage C. Par défaut, le compilateur MIDL utilise le nom de fichier de base du fichier IDL dans le cadre des fichiers stub générés. Lorsque plus de six caractères sont présents dans le nom de fichier de base, certains systèmes de fichiers peuvent ne pas accepter le nom de stub complet. Le tableau suivant répertorie les conventions utilisées pour les noms de fichiers.



| Fichier        | Partie par défaut du nom de fichier de base | Exemple      |
|-------------|-----------------------------------|--------------|
| Fichier IDL    | ---                               | ABCDEFGH. idl |
| En-tête      | .h                                | Abcdef. h     |
| Stub client | \_c. c                             | Abcdef \_ c. c  |
| Stub serveur | \_s. c                             | Abcdef \_ s. c  |



 

 

 




