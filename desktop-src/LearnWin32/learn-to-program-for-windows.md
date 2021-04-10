---
title: Bien démarrer avec Win32 et C++
description: L’objectif de cette série de prise en main est de vous apprendre à écrire un programme de bureau en C++ à l’aide des API Win32 et COM.
ms.assetid: a9470cb9-a1e7-4d6d-a4be-61b81d209ada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b1ad80530877e9502d158a16295013e3f4a05e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675630"
---
# <a name="get-started-with-win32-and-c"></a><span data-ttu-id="4caf0-103">Bien démarrer avec Win32 et C++</span><span class="sxs-lookup"><span data-stu-id="4caf0-103">Get Started with Win32 and C++</span></span>

<span data-ttu-id="4caf0-104">L’objectif de cette série de prise en main est de vous apprendre à écrire un programme de bureau en C++ à l’aide des API Win32 et COM.</span><span class="sxs-lookup"><span data-stu-id="4caf0-104">The aim of this Get Started series is to teach you how to write a desktop program in C++ using Win32 and COM APIs.</span></span>

<span data-ttu-id="4caf0-105">Dans le premier module, vous apprendrez comment créer et afficher une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="4caf0-105">In the first module, you'll learn step-by-step how to create and show a window.</span></span> <span data-ttu-id="4caf0-106">Les modules ultérieurs présentent le modèle COM (Component Object Model), les graphiques et le texte, ainsi que l’entrée utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4caf0-106">Later modules will introduce the Component Object Model (COM), graphics and text, and user input.</span></span>

<span data-ttu-id="4caf0-107">Pour cette série, il est supposé que vous avez une bonne connaissance pratique de la programmation C++.</span><span class="sxs-lookup"><span data-stu-id="4caf0-107">For this series, it is assumed that you have a good working knowledge of C++ programming.</span></span> <span data-ttu-id="4caf0-108">Aucune expérience précédente avec la programmation Windows n’est supposée.</span><span class="sxs-lookup"><span data-stu-id="4caf0-108">No previous experience with Windows programming is assumed.</span></span> <span data-ttu-id="4caf0-109">Si vous débutez avec C++, vous trouverez des documents de formation dans le [Centre de développement Visual C++](https://msdn.microsoft.com/vstudio//default.aspx).</span><span class="sxs-lookup"><span data-stu-id="4caf0-109">If you are new to C++, you can find learning material at the [Visual C++ Developer Center](https://msdn.microsoft.com/vstudio//default.aspx).</span></span> <span data-ttu-id="4caf0-110">(Cette ressource n’est peut-être pas disponible dans certaines langues et certains pays.)</span><span class="sxs-lookup"><span data-stu-id="4caf0-110">(This resource may not be available in some languages and countries.)</span></span>

## <a name="in-this-section"></a><span data-ttu-id="4caf0-111">Contenu de cette section</span><span class="sxs-lookup"><span data-stu-id="4caf0-111">In this section</span></span>



| <span data-ttu-id="4caf0-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="4caf0-112">Topic</span></span>                                                                                                     | <span data-ttu-id="4caf0-113">Description</span><span class="sxs-lookup"><span data-stu-id="4caf0-113">Description</span></span>                                                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4caf0-114">Introduction à la programmation Windows en C++</span><span class="sxs-lookup"><span data-stu-id="4caf0-114">Introduction to Windows Programming in C++</span></span>](introduction-to-windows-programming-in-c--.md)<br/>   | <span data-ttu-id="4caf0-115">Cette section décrit certaines des conventions de base relatives à la terminologie et au codage utilisées dans la programmation Windows.</span><span class="sxs-lookup"><span data-stu-id="4caf0-115">This section describes some of the basic terminology and coding conventions used in Windows programming.</span></span><br/>  |
| [<span data-ttu-id="4caf0-116">Module 1. Votre premier programme Windows</span><span class="sxs-lookup"><span data-stu-id="4caf0-116">Module 1. Your First Windows Program</span></span>](your-first-windows-program.md)<br/>                         | <span data-ttu-id="4caf0-117">Dans ce module, vous allez créer un programme Windows simple qui affiche une fenêtre vide.</span><span class="sxs-lookup"><span data-stu-id="4caf0-117">In this module, you will create a simple Windows program that shows a blank window.</span></span><br/>                       |
| [<span data-ttu-id="4caf0-118">Module 2. Utilisation de COM dans votre programme Windows</span><span class="sxs-lookup"><span data-stu-id="4caf0-118">Module 2. Using COM in Your Windows Program</span></span>](module-2--using-com-in-your-windows-program.md)<br/> | <span data-ttu-id="4caf0-119">Ce module présente le modèle COM (Component Object Model), qui repose sur la plupart des API Windows modernes.</span><span class="sxs-lookup"><span data-stu-id="4caf0-119">This module introduces the Component Object Model (COM), which underlies many of the modern Windows APIs.</span></span><br/> |
| [<span data-ttu-id="4caf0-120">Module 3. Graphiques Windows</span><span class="sxs-lookup"><span data-stu-id="4caf0-120">Module 3. Windows Graphics</span></span>](module-3---windows-graphics.md)<br/>                                  | <span data-ttu-id="4caf0-121">Ce module présente l’architecture graphique Windows, avec un focus sur Direct2D.</span><span class="sxs-lookup"><span data-stu-id="4caf0-121">This module introduces the Windows graphics architecture, with a focus on Direct2D.</span></span><br/>                       |
| [<span data-ttu-id="4caf0-122">Module 4. Entrée utilisateur</span><span class="sxs-lookup"><span data-stu-id="4caf0-122">Module 4. User Input</span></span>](module-4--user-input.md)<br/>                                               | <span data-ttu-id="4caf0-123">Ce module décrit les entrées de souris et de clavier.</span><span class="sxs-lookup"><span data-stu-id="4caf0-123">This module describes mouse and keyboard input.</span></span><br/>                                                           |
| [<span data-ttu-id="4caf0-124">Exemple de Code</span><span class="sxs-lookup"><span data-stu-id="4caf0-124">Sample Code</span></span>](learn-to-program-for-windows--sample-code.md)<br/>                                   | <span data-ttu-id="4caf0-125">Contient des liens pour télécharger l’exemple de code pour cette série.</span><span class="sxs-lookup"><span data-stu-id="4caf0-125">Contains links to download the sample code for this series.</span></span><br/>                                               |



 

 

 





