---
description: Les contextes d’application peuvent être utilisés pour créer des classes Windows côte à côte.
ms.assetid: 4941ae1b-f9c6-45ff-b39b-a4078a12a58c
title: Création de classes Windows côte à côte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 161732522a12fb6924a2850031d77cff53e44eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866022"
---
# <a name="creating-side-by-side-windows-classes"></a><span data-ttu-id="41cb8-103">Création de classes Windows côte à côte</span><span class="sxs-lookup"><span data-stu-id="41cb8-103">Creating Side-By-Side Windows Classes</span></span>

<span data-ttu-id="41cb8-104">Les contextes d’application peuvent être utilisés pour créer des classes Windows côte à côte.</span><span class="sxs-lookup"><span data-stu-id="41cb8-104">Application contexts can be used to create side-by-side Windows classes.</span></span> <span data-ttu-id="41cb8-105">En utilisant des classes Windows côte à côte, votre application peut avoir des versions différentes d’une classe actives en même temps dans une fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="41cb8-105">By using side-by-side Windows classes, your application can have different versions of a class active at the same time in a lone parent window.</span></span> <span data-ttu-id="41cb8-106">Pour créer une classe Windows côte à côte, votre application doit activer un contexte d’activation avant d’appeler [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) pour obtenir un handle vers la nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="41cb8-106">To create a side-by-side Windows class, your application must activate an activation context before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) to obtain a handle to the new window.</span></span>

<span data-ttu-id="41cb8-107">Par exemple, les contrôles communs Windows version 5,82 et version 6,0 disposent tous les deux d’un contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="41cb8-107">For example, Windows Common Controls version 5.82 and version 6.0 both had an Edit control.</span></span> <span data-ttu-id="41cb8-108">Windows utilise par défaut la version 5,82 du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="41cb8-108">Windows defaults to using the version 5.82 Edit control.</span></span> <span data-ttu-id="41cb8-109">Pour obtenir une fenêtre côte à côte avec la version 6,0 du contrôle d’édition, avant d’appeler [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) comme d’habitude, votre application peut référencer un assembly qui expose des classes de fenêtres nommées, puis activer le contexte d’activation qui référence les contrôles de la version 6,0.</span><span class="sxs-lookup"><span data-stu-id="41cb8-109">To obtain a side-by-side window that has the version 6.0 Edit control, before calling [**CreateWindow**](/windows/win32/api/winuser/nf-winuser-createwindowa) as usual, your application can reference an assembly that exposes named window classes and then activate the activation context that references the version 6.0 controls.</span></span>

 

 
