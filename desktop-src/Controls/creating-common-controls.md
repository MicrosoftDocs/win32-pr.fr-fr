---
title: Création de contrôles communs
description: Cette rubrique explique comment créer une fenêtre qui appartient à une classe de fenêtre définie dans la bibliothèque de contrôles communs, Comctl32.dll.
ms.assetid: BCF25606-5B49-43A5-8107-E7220BE3253C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 944e8aa70b3367f1d3a12e4f50032e6677c5d706
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103941475"
---
# <a name="creating-common-controls"></a><span data-ttu-id="31458-103">Création de contrôles communs</span><span class="sxs-lookup"><span data-stu-id="31458-103">Creating Common Controls</span></span>

<span data-ttu-id="31458-104">Cette rubrique explique comment créer une fenêtre qui appartient à une classe de fenêtre définie dans la bibliothèque de contrôles communs, Comctl32.dll.</span><span class="sxs-lookup"><span data-stu-id="31458-104">This topic describes how to create a window that belongs to a window class defined in the common control library, Comctl32.dll.</span></span>


<span data-ttu-id="31458-105">La plupart des contrôles communs appartiennent à une classe de fenêtre définie dans la DLL de contrôle commune.</span><span class="sxs-lookup"><span data-stu-id="31458-105">Most common controls belong to a window class defined in the common control DLL.</span></span> <span data-ttu-id="31458-106">La classe de fenêtre et la procédure de fenêtre correspondante définissent les propriétés, l’apparence et le comportement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="31458-106">The window class and the corresponding window procedure define the properties, appearance, and behavior of the control.</span></span> <span data-ttu-id="31458-107">Pour vous assurer que la DLL de contrôles communs est chargée, incluez la fonction [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) dans votre application.</span><span class="sxs-lookup"><span data-stu-id="31458-107">To ensure that the common control DLL is loaded, include the [**InitCommonControlsEx**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex) function in your application.</span></span> <span data-ttu-id="31458-108">Vous créez un contrôle commun en spécifiant le nom de la classe de fenêtre lors de l’appel de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou en spécifiant le nom de classe approprié dans un modèle de boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="31458-108">You create a common control by specifying the name of the window class when calling the [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) function or by specifying the appropriate class name in a dialog box template.</span></span>


<span data-ttu-id="31458-109">Chaque type de contrôle commun possède un ensemble de styles de contrôle que vous pouvez utiliser pour faire varier l’apparence et le comportement du contrôle.</span><span class="sxs-lookup"><span data-stu-id="31458-109">Each type of common control has a set of control styles that you can use to vary the appearance and behavior of the control.</span></span> <span data-ttu-id="31458-110">La bibliothèque de contrôles communs comprend également un ensemble de styles de contrôle qui s’appliquent à deux ou plusieurs types de contrôles communs.</span><span class="sxs-lookup"><span data-stu-id="31458-110">The common control library also includes a set of control styles that apply to two or more types of common controls.</span></span> <span data-ttu-id="31458-111">Les styles de contrôles communs sont décrits dans la section [styles](common-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="31458-111">The common control styles are described in the [Styles](common-control-styles.md) section.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31458-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="31458-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31458-113">À propos des contrôles communs</span><span class="sxs-lookup"><span data-stu-id="31458-113">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 