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
ms.openlocfilehash: b9f34bc9035e9aa9fac884a14946a0593cb70702cf19f22d5d4c82011b58077e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012007"
---
# <a name="porting-the-bbox2-function"></a>Portage de la fonction BBOX2

Il n’existe aucun équivalent OpenGL pour la fonction IRIS GL **BBOX2** .

**Pour porter le code qui contient des fonctions BBOX2**

1.  Créez une nouvelle liste d’affichage (OpenGL) qui contient tous les éléments de la liste d’affichage de la comptabilité IRIS équivalente, à l’exception de l’appel à **BBOX2**.
2.  utilisez le code Windows approprié pour dessiner un rectangle de la même taille que le **bbox** de l’IRIS du GL.

 

 




