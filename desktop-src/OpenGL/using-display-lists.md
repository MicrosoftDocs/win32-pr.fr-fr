---
title: Utilisation des listes d’affichage
description: Utilisation des listes d’affichage
ms.assetid: f5edff21-0928-4ec9-9718-5189bf8ce2d7
keywords:
- OpenGL, afficher les listes
- afficher les listes OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322721868f3bf994382a7604aa2cb76802f268aec7a1298aaa14e3066d5f6cce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118932799"
---
# <a name="using-display-lists"></a>Utilisation des listes d’affichage

Une liste d’affichage est un groupe de fonctions OpenGL qui a été stocké pour une exécution ultérieure. La fonction [**glNewList**](glnewlist.md) commence la création d’une liste d’affichage et [**glEndList**](glendlist.md) la termine. À quelques exceptions près, les fonctions OpenGL appelées entre **glNewList** et **glEndList** sont ajoutées à la liste d’affichage. (Consultez **glNewList** pour obtenir la liste des fonctions que vous ne pouvez pas stocker et exécuter à partir d’une liste d’affichage.) Pour déclencher l’exécution d’une liste ou d’un ensemble de listes, utilisez [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) et fournissez le numéro d’identification d’une liste ou de listes particulières. Vous gérez les index utilisés pour identifier les listes d’affichage avec [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)et [**glIsList**](glislist.md). Pour supprimer un ensemble de listes d’affichage, utilisez [**glDeleteLists**](gldeletelists.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence des listes d’affichage](display-lists-reference.md)
</dt> </dl>

 

 




