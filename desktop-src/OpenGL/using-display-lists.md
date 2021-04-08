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
# <a name="using-display-lists"></a><span data-ttu-id="0cc44-105">Utilisation des listes d’affichage</span><span class="sxs-lookup"><span data-stu-id="0cc44-105">Using Display Lists</span></span>

<span data-ttu-id="0cc44-106">Une liste d’affichage est un groupe de fonctions OpenGL qui a été stocké pour une exécution ultérieure.</span><span class="sxs-lookup"><span data-stu-id="0cc44-106">A display list is a group of OpenGL functions that has been stored for subsequent execution.</span></span> <span data-ttu-id="0cc44-107">La fonction [**glNewList**](glnewlist.md) commence la création d’une liste d’affichage et [**glEndList**](glendlist.md) la termine.</span><span class="sxs-lookup"><span data-stu-id="0cc44-107">The [**glNewList**](glnewlist.md) function begins the creation of a display list, and [**glEndList**](glendlist.md) ends it.</span></span> <span data-ttu-id="0cc44-108">À quelques exceptions près, les fonctions OpenGL appelées entre **glNewList** et **glEndList** sont ajoutées à la liste d’affichage.</span><span class="sxs-lookup"><span data-stu-id="0cc44-108">With few exceptions, OpenGL functions called between **glNewList** and **glEndList** are appended to the display list.</span></span> <span data-ttu-id="0cc44-109">(Consultez **glNewList** pour obtenir la liste des fonctions que vous ne pouvez pas stocker et exécuter à partir d’une liste d’affichage.) Pour déclencher l’exécution d’une liste ou d’un ensemble de listes, utilisez [**glCallList**](glcalllist.md) ou [**glCallLists**](glcalllists.md) et fournissez le numéro d’identification d’une liste ou de listes particulières.</span><span class="sxs-lookup"><span data-stu-id="0cc44-109">(See **glNewList** for a list of the functions that you can't store and execute from within a display list.) To trigger the execution of a list or set of lists, use [**glCallList**](glcalllist.md) or [**glCallLists**](glcalllists.md) and supply the identifying number of a particular list or lists.</span></span> <span data-ttu-id="0cc44-110">Vous gérez les index utilisés pour identifier les listes d’affichage avec [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md)et [**glIsList**](glislist.md).</span><span class="sxs-lookup"><span data-stu-id="0cc44-110">You manage the indexes used to identify display lists with [**glGenLists**](glgenlists.md), [**glListBase**](gllistbase.md), and [**glIsList**](glislist.md).</span></span> <span data-ttu-id="0cc44-111">Pour supprimer un ensemble de listes d’affichage, utilisez [**glDeleteLists**](gldeletelists.md).</span><span class="sxs-lookup"><span data-stu-id="0cc44-111">To delete a set of display lists, use [**glDeleteLists**](gldeletelists.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0cc44-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0cc44-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cc44-113">Référence des listes d’affichage</span><span class="sxs-lookup"><span data-stu-id="0cc44-113">Display Lists Reference</span></span>](display-lists-reference.md)
</dt> </dl>

 

 




