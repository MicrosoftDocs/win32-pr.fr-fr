---
title: Portage vers OpenGL
description: Portage vers OpenGL
ms.assetid: 6799e10b-2f7c-4516-92ea-43667784f8e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f8efd2a34ac5d7fb6fc52aef3f24a556712b2c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380110"
---
# <a name="porting-to-opengl"></a><span data-ttu-id="2b429-103">Portage vers OpenGL</span><span class="sxs-lookup"><span data-stu-id="2b429-103">Porting to OpenGL</span></span>

<span data-ttu-id="2b429-104">OpenGL est conçu pour la compatibilité sur le matériel et les systèmes d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="2b429-104">OpenGL is designed for compatibility across hardware and operating systems.</span></span> <span data-ttu-id="2b429-105">Cette conception permet aux programmeurs de déplacer plus facilement les programmes OpenGL d’un système à un autre.</span><span class="sxs-lookup"><span data-stu-id="2b429-105">This design makes it easier for programmers to port OpenGL programs from one system to another.</span></span> <span data-ttu-id="2b429-106">Même si chaque système d’exploitation a des exigences uniques, une grande partie du code OpenGL dans vos programmes actuels peut être utilisé tel quel.</span><span class="sxs-lookup"><span data-stu-id="2b429-106">While each operating system has unique requirements, much of the OpenGL code in your current programs can be used as is.</span></span> <span data-ttu-id="2b429-107">Pour porter votre application OpenGL vers Microsoft Windows, vous devez modifier vos programmes pour qu’ils fonctionnent avec les systèmes de fenêtrage Windows.</span><span class="sxs-lookup"><span data-stu-id="2b429-107">To port your OpenGL application to Microsoft Windows, you'll have to modify your programs to work with the Windows windowing systems.</span></span>

<span data-ttu-id="2b429-108">Dans, les applications générales sont reportées à OpenGL pour Windows à partir de l’une des deux plateformes suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b429-108">In general applications are ported to OpenGL for Windows from one of two platforms:</span></span>

-   <span data-ttu-id="2b429-109">Applications OpenGL développées pour le système X Window et la bibliothèque X (Xlib)</span><span class="sxs-lookup"><span data-stu-id="2b429-109">OpenGL applications developed for the X Window System and the X library (Xlib)</span></span>
-   <span data-ttu-id="2b429-110">Applications du GL IRIS</span><span class="sxs-lookup"><span data-stu-id="2b429-110">IRIS GL applications</span></span>

<span data-ttu-id="2b429-111">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="2b429-111">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2b429-112">Introduction au portage vers OpenGL pour Windows</span><span class="sxs-lookup"><span data-stu-id="2b429-112">Introduction to Porting to OpenGL for Windows</span></span>](introduction-to-porting-to-opengl-for-windows-nt--windows-2000--and-windows-95-98.md)
-   [<span data-ttu-id="2b429-113">Fonctions OpenGL et leurs équivalents de la comptabilité IRIS</span><span class="sxs-lookup"><span data-stu-id="2b429-113">OpenGL Functions and Their IRIS GL Equivalents</span></span>](opengl-functions-and-their-iris-gl-equivalents.md)
-   [<span data-ttu-id="2b429-114">Différences entre l’IRIS dans le GL et OpenGL</span><span class="sxs-lookup"><span data-stu-id="2b429-114">IRIS GL and OpenGL Differences</span></span>](iris-gl-and-opengl-differences.md)

 

 




