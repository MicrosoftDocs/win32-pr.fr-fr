---
title: Sélection
description: Selection retourne le contenu actuel de la pile de noms, qui est un tableau de noms avec des valeurs entières.
ms.assetid: 66902d2c-0cd7-49b3-a685-5c0bdba0df1c
keywords:
- mode de sélection OpenGL
- accès à la sélection OpenGL
- enregistrements d’accès OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42c057014a4f5a1533e1f5c42683b93f08c31c287dc29f56ea797a5b360d545
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119776739"
---
# <a name="selection"></a>Sélection

Selection retourne le contenu actuel de la pile de noms, qui est un tableau de noms avec des valeurs entières. Vous assignez les noms et créez la pile de noms dans le code de modélisation qui spécifie la géométrie des objets que vous souhaitez dessiner. Ensuite, en mode de sélection, chaque fois qu’une primitive croise le volume du clip, un accès à la sélection se produit. L’enregistrement d’accès, qui est écrit dans le tableau de sélection que vous avez fourni avec [**glSelectBuffer**](glselectbuffer.md), contient des informations sur le contenu de la pile de noms au moment de l’accès.

> [!Note]  
> Appelez [**glSelectBuffer**](glselectbuffer.md) avant de mettre OpenGL en mode de sélection avec [**glRenderMode**](glrendermode.md). La totalité du contenu de la pile de noms n’est pas retournée tant que vous n’avez pas appelé **glRenderMode** pour utiliser OpenGL en mode de sélection.

 

Manipuler la pile de noms avec [**glInitNames**](glinitnames.md), [**glLoadName**](glloadname.md), [**glPushName**](glpushname.md)et [**glPopName**](glpopname.md). Vous pouvez également utiliser [**gluPickMatrix**](glupickmatrix.md) pour la sélection.

 

 




