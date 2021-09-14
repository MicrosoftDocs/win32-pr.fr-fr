---
title: Spécifier des rappels
description: Vous pouvez spécifier jusqu’à cinq fonctions de rappel pour un pavage.
ms.assetid: b49a8400-8111-450d-a2d7-c313a898a213
keywords:
- Utilitaire OpenGL (GLU), spécification de fonctions de rappel
- GLU (utilitaire OpenGL), spécification de fonctions de rappel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6086448cf6f4a71ea6a49359d5656f12f613d760
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009265"
---
# <a name="specifying-callbacks"></a>Spécifier des rappels

Vous pouvez spécifier jusqu’à cinq fonctions de rappel pour un pavage. Toutes les fonctions que vous ne spécifiez pas ne sont pas appelées pendant le pavage et aucune information n’est renvoyée. Vous spécifiez les fonctions de rappel avec [*gluTessCallback*](glutess.md).

La fonction **gluTessCallback** associe la fonction de rappel *FN* à l’objet de pavage *tessobj*. Le type du rappel est déterminé par le *type* de paramètre, qui peut être **Glu \_ Begin**, **Glu \_ Edge \_ Flag**, **Glu \_ vertex**, **Glu \_ end** ou **Glu \_ Error**. Les cinq fonctions de rappel possibles ont les prototypes suivants.



| Fonction de rappel   | Prototype                                    |
|---------------------|----------------------------------------------|
| **début de GLU \_**      | **void** **Begin**(_type_ GLenum);       |
| **\_indicateur de bord Glu \_** | **void** **edgeFlag**(_indicateur_ GLboolean); |
| **GLU \_ vertex**     | **void** **vertex**(**void \* * * * Data* );     |
| **fin de GLU \_**        | **void** **end**( *void* );                  |
| **\_erreur Glu**      | **void** **Error**(**GLenum**_errno_ );      |



 

Pour modifier une fonction de rappel, appelez [*gluTessCallback*](glutess.md) avec la nouvelle fonction. Pour éliminer une fonction de rappel sans la remplacer par une nouvelle, transmettez **gluTessCallback** un pointeur null pour la fonction appropriée.

À mesure que le pavage se poursuit, les fonctions de rappel sont appelées de manière similaire à la façon dont vous utilisez les fonctions OpenGL [**glBegin**](glbegin.md), [glEdgeFlag](gledgeflag-functions.md), [glVertex](glvertex-functions.md)et [**glEnd**](glend.md).

La fonction de rappel **Glu \_ Begin** est appelée avec l’un des trois paramètres possibles :

-   \_ventilateur à triangles GL \_
-   \_bande triangulaire GL \_
-   \_TRIangles GL

Après l’appel de la fonction de rappel **Glu \_ Begin** , et avant l’appel de la fonction de rappel associée à **Glu \_ end**, une combinaison de l' **\_ \_ indicateur de périphérie Glu** et des rappels de **\_ vertex Glu** est appelée. Les sommets et les indicateurs de bord associés sont interprétés exactement comme ils se trouvent dans OpenGL entre **glBegin**(ventilateur triangulaire GL \_ \_ ), **glBegin**( \_ bande triangulaire GL \_ ) ou **GlBegin**( \_ triangles GL **)** et le **glEnd** de correspondance.

Étant donné que les indicateurs de périphérie n’ont aucune signification dans un ventilateur triangulaire ou une bande triangulaire, si une fonction de rappel est associée à l' **\_ \_ indicateur Glu Edge**, le rappel de **\_ début Glu** est appelé uniquement avec des **\_ triangles GL**. La fonction de rappel de l' **\_ \_ indicateur Edge Glu** fonctionne de la même façon que la fonction [glEdgeFlag](gledgeflag-functions.md) OpenGL.

En cas d’erreur pendant le pavage, la fonction de rappel d’erreur est appelée. La fonction de rappel d’erreur reçoit un numéro d’erreur GLU. Vous pouvez obtenir une chaîne de caractères décrivant l’erreur avec la fonction [**gluErrorString**](gluerrorstring.md) .

 

 




