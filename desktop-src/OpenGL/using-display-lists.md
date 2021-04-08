---
title: Utilisation des listes d’affichage
description: Utilisation des listes d’affichage
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, afficher les listes
- afficher les listes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 793ec78af0b19ac437e44f16e13b93db6eab32a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839701"
---
# <a name="using-display-lists"></a>Utilisation des listes d’affichage

Une liste d’affichage est un groupe de fonctions OpenGL qui a été stocké pour une exécution ultérieure. La fonction [**glNewList**](glnewlist.md) commence la création d’une liste d’affichage et [**glEndList**](glendlist.md) la termine. À quelques exceptions près, les fonctions OpenGL appelées entre **glNewList** et **glEndList** sont ajoutées à la liste d’affichage. (Consultez **glNewList** pour obtenir la liste des fonctions que vous ne pouvez pas stocker et exécuter à partir d’une liste d’affichage.) Pour déclencher l’exécution d’une liste ou d’un ensemble de listes, utilisez [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) et fournissez le numéro d’identification d’une liste ou de listes particulières. Vous gérez les index utilisés pour identifier les listes d’affichage avec [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)et [**glIsList**](glislist.md). Pour supprimer un ensemble de listes d’affichage, utilisez [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence des listes d’affichage](display-lists-reference.md)
</dt> </dl>

 

 




