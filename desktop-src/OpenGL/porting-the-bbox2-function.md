---
title: Portage de la fonction BBOX2
description: Il n’existe aucun équivalent OpenGL pour la fonction IRIS GL BBOX2.
ms.assetid: 2d8082bf-c2c3-41d9-9bf7-b4ac2fdefbd6
keywords:
- Portage de l’IRIS dans le GL, fonction BBOX2
- Portage à partir de IRIS GL, fonction BBOX2
- portage vers OpenGL à partir de l’IRIS GL, fonction BBOX2
- Portage OpenGL depuis IRIS GL, fonction BBOX2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21060b8a11ccd6c44297c8b533bca98d79cc00f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674533"
---
# <a name="porting-the-bbox2-function"></a>Portage de la fonction BBOX2

Il n’existe aucun équivalent OpenGL pour la fonction IRIS GL **BBOX2** .

**Pour porter le code qui contient des fonctions BBOX2**

1.  Créez une nouvelle liste d’affichage (OpenGL) qui contient tous les éléments de la liste d’affichage de la comptabilité IRIS équivalente, à l’exception de l’appel à **BBOX2**.
2.  Utilisez le code Windows approprié pour dessiner un rectangle de la même taille que le **Bbox** de l’iris du GL.

 

 




