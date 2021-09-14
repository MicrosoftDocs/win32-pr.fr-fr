---
title: Portage greset
description: OpenGL remplace la fonction IRIS GL, greset, par les fonctions, glPushAttrib et glPopAttrib.
ms.assetid: 348e8b18-4f12-45d1-a4d2-6533a983236b
keywords:
- Portage du grand livre de l’IRIS, variables d’État
- Portage à partir de IRIS GL, variables d’État
- portage vers OpenGL à partir de IRIS GL, variables d’État
- Portage OpenGL à partir de IRIS GL, variables d’État
- variables d’État
- Portage de l’IRIS dans le GL, fonction greset
- Portage à partir de IRIS GL, fonction greset
- portage vers OpenGL à partir de l’IRIS GL, fonction greset
- Portage OpenGL depuis IRIS GL, fonction greset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078482f47dcaf7fd5f84605e2e0fa32d0cf14729
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011447"
---
# <a name="porting-greset"></a>Portage greset

OpenGL remplace la fonction IRIS GL, **greset**, par les fonctions, [**glPushAttrib**](glpushattrib.md) et [**glPopAttrib**](glpopattrib.md). Utilisez ces fonctions pour enregistrer et restaurer des groupes de variables d’État. Par exemple,

``` syntax
void glPushAttrib( GLbitfield mask );
```

Cet exemple prend une opération or au niveau du bit des constantes symboliques, indiquant les groupes de variables d’État à envoyer dans une pile d’attributs. Chaque constante fait référence à un groupe de variables d’État. Le tableau suivant montre les groupes d’attributs avec leurs noms de constantes symboliques équivalents. Pour obtenir la liste complète des variables d’État OpenGL associées à chaque constante, consultez [**glPushAttrib**](glpushattrib.md).



| Attribut                       | Constante                  |
|---------------------------------|---------------------------|
| valeur effacée de la mémoire tampon d’accumulation | \_bit de tampon amort \_ \_    |
| mémoire tampon de couleur                    | \_bit de \_ mémoire tampon de couleur GL \_    |
| actuels                         | \_bit actuel du GL \_          |
| mémoire tampon de profondeur                    | \_bit de \_ mémoire tampon de profondeur GL \_    |
| enable                          | \_bit d’activation du GL \_           |
| évaluateurs                      | EGL \_ Val \_ bit             |
| brouillard                             | \_bit de brouillard GL \_              |
| Paramètre de base de la \_ liste GL \_          | \_bit de liste GL \_             |
| variables d’indicateur                  | \_bit indicateur \_ GL             |
| variables d’éclairage              | \_bit d’éclairage GL \_         |
| mode dessin en courbes               | \_bit de ligne GL \_             |
| variables en mode pixel            | \_bit du \_ mode de pixel GL \_      |
| variables point                 | \_bit de point GL \_            |
| polygon                         | \_bit de polygone GL \_          |
| Polygone stipple                 | \_STIPPLE- \_ \_ bit de polygone de GL |
| ciseaux                         | \_bit de ciseaux de GL \_          |
| tampon de stencil                  | \_bit de \_ tampon de stencil du GL \_  |
| texture                         | \_bit de texture GL \_          |
| transformation                       | \_bit de transformation GL \_        |
| fenêtre d'affichage                        | \_bit de fenêtre d’affichage GL \_         |
|                                 | \_bits de tous les \_ attributs du GL \_     |



 

Pour restaurer les valeurs des variables d’État à celles enregistrées avec le dernier [**glPushAttrib**](glpushattrib.md), il vous suffit d’appeler [**glPopAttrib**](glpopattrib.md). Les variables que vous n’avez pas enregistrées resteront inchangées. La pile d’attributs a une profondeur finie d’au moins 16.

 

 




