---
title: Transformation des coordonnées
description: La bibliothèque d’utilitaires OpenGL (GLU) fournit plusieurs fonctions de transformation de matrice couramment utilisées.
ms.assetid: 9ca32be8-3bc0-4fca-a58c-69a4800c3c55
keywords:
- Utilitaire OpenGL (GLU), fonctions de transformation de matrice
- GLU (utilitaire OpenGL), fonctions de transformation de matrice
- fonctions de transformation de matrice OpenGL
- Utilitaire OpenGL (GLU), transformation des coordonnées
- GLU (utilitaire OpenGL), transformation des coordonnées
- transformation de coordonnées OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 504a5a58c723dcccfc54ce2f47a01710133ccc30
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675490"
---
# <a name="transforming-coordinates"></a>Transformation des coordonnées

La bibliothèque d’utilitaires OpenGL (GLU) fournit plusieurs fonctions de transformation de matrice couramment utilisées. Vous pouvez configurer une région d’affichage orthographique à deux dimensions avec [**gluOrtho2D**](gluortho2d.md), un volume de vue de perspective standard à l’aide de [**gluPerspective**](gluperspective.md)ou un volume de vue centré sur un Eyepoint spécifié avec [**gluLookAt**](glulookat.md). Chacune de ces fonctions crée la matrice souhaitée et l’applique à la matrice actuelle à l’aide de [**glMultMatrix**](glmultmatrix.md).

La fonction [**gluPickMatrix**](glupickmatrix.md) simplifie la sélection d’une matrice de prélèvement en créant une matrice qui restreint le dessin à une petite zone de la fenêtre d’affichage. Si vous rerendez la scène en mode de sélection après l’application de cette matrice, tous les objets qui seraient dessinés près du curseur seront sélectionnés et les informations les concernant seront stockées dans la mémoire tampon de sélection. Pour plus d’informations sur le mode de sélection, consultez « sélection de la sélection et des commentaires » [exécution de la sélection et des commentaires](performing-selection-and-feedback.md).

Pour déterminer l’emplacement dans la fenêtre où un objet est dessiné, utilisez [**gluProject**](gluproject.md), qui convertit les coordonnées de l’objet spécifié *objX*, *objy* et *objz* en coordonnées de fenêtre à l’aide de *modelMatrix*, *projMatrix* et *Viewport*. Le résultat est stocké dans *Winx*, *winy* et *WINZ*. Si la fonction est réussie, la valeur de retour est GL \_ true. Si la fonction échoue, la valeur de retour est GL \_ false.

La fonction [**gluUnProject**](gluunproject.md) effectue la conversion inverse : elle transforme les coordonnées de fenêtre spécifiées *Winx*, *winy* et *WINZ* en coordonnées d’objet à l’aide de *modelMatrix*, *projMatrix* et *Viewport*. Le résultat est stocké dans *objX*, *objy* et *objz*. Si la fonction est réussie, la valeur de retour est GL \_ true. Si la fonction échoue, la valeur de retour est GL \_ false.

 

 




