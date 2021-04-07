---
title: Création d’un gestionnaire de fichiers ou de flux
description: Création d’un gestionnaire de fichiers ou de flux
ms.assetid: 9ec1af9a-f428-4323-a4f8-3eb923ce78d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b2f118f4f5279cea1aacedd58b86f23afa9a9af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029075"
---
# <a name="creating-a-file-or-stream-handler"></a><span data-ttu-id="20077-103">Création d’un gestionnaire de fichiers ou de flux</span><span class="sxs-lookup"><span data-stu-id="20077-103">Creating a File or Stream Handler</span></span>

<span data-ttu-id="20077-104">Dans une application écrite dans le langage de programmation C, un gestionnaire de fichiers ou de flux crée généralement une fonction pour chaque méthode.</span><span class="sxs-lookup"><span data-stu-id="20077-104">In an application written in the C programming language, a file or stream handler usually creates a function for each method.</span></span> <span data-ttu-id="20077-105">Votre application accède à ces fonctions par le biais d’un tableau de pointeurs de fonction créés par le gestionnaire de flux.</span><span class="sxs-lookup"><span data-stu-id="20077-105">Your application accesses these functions through an array of function pointers the stream handler creates.</span></span> <span data-ttu-id="20077-106">Une structure **IAVIStreamVtbl** contient le tableau de pointeurs de fonction.</span><span class="sxs-lookup"><span data-stu-id="20077-106">An **IAVIStreamVtbl** structure contains the array of function pointers.</span></span> <span data-ttu-id="20077-107">Un gestionnaire de flux peut assigner n’importe quel nom à des fonctions qu’il crée pour les méthodes.</span><span class="sxs-lookup"><span data-stu-id="20077-107">A stream handler can assign any name it wants to functions it creates for the methods.</span></span> <span data-ttu-id="20077-108">La position du pointeur de fonction dans la structure implique la correspondance entre la fonction et la méthode.</span><span class="sxs-lookup"><span data-stu-id="20077-108">The position of the function pointer in the structure implies the correspondence of the function to the method.</span></span> <span data-ttu-id="20077-109">Par exemple, le premier pointeur de fonction de la structure correspond à la méthode **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="20077-109">For example, the first function pointer in the structure corresponds to the **QueryInterface** method.</span></span> <span data-ttu-id="20077-110">Votre gestionnaire de flux doit fournir toutes les fonctions d’une interface.</span><span class="sxs-lookup"><span data-stu-id="20077-110">Your stream handler must provide all the functions of an interface.</span></span>

 

 




