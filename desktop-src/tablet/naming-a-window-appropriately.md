---
description: Vue d’ensemble de la désignation d’une fenêtre de manière appropriée et de la définition de la légende de la fenêtre pour Tablet PC.
ms.assetid: 9d064188-53a1-4cb5-b516-99610d7b8134
title: Attribution d’un nom à une fenêtre de manière appropriée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaee320f621acf834d7c0ec5978a9e42f0811e31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520057"
---
# <a name="naming-a-window-appropriately"></a><span data-ttu-id="a1af0-103">Attribution d’un nom à une fenêtre de manière appropriée</span><span class="sxs-lookup"><span data-stu-id="a1af0-103">Naming a Window Appropriately</span></span>

<span data-ttu-id="a1af0-104">Assignez à chaque fenêtre une légende conviviale, même si la fenêtre ou sa légende est invisible.</span><span class="sxs-lookup"><span data-stu-id="a1af0-104">Assign every window a user-friendly caption, even if the window or its caption is invisible.</span></span> <span data-ttu-id="a1af0-105">Cela permet à la fonctionnalité de reconnaissance vocale d’identifier la fenêtre et la hiérarchie de la fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a1af0-105">This allows the speech functionality to identify the window and the window hierarchy.</span></span> <span data-ttu-id="a1af0-106">Cette recommandation s’applique à toutes les fenêtres : les fenêtres de niveau supérieur avec des frames visibles. les fenêtres enfants, telles que les palettes flottantes ; contrôles personnalisés ; barres d’outils et les volets dans une fenêtre, lorsqu’ils sont implémentés en tant que fenêtres enfants.</span><span class="sxs-lookup"><span data-stu-id="a1af0-106">This recommendation applies to all windows: top-level windows with visible frames; child windows, such as floating palettes; custom controls; toolbars; and panes within a window, when implemented as child windows.</span></span>

<span data-ttu-id="a1af0-107">Il existe trois façons de définir le titre de la fenêtre :</span><span class="sxs-lookup"><span data-stu-id="a1af0-107">There are three ways to set the window caption:</span></span>

-   <span data-ttu-id="a1af0-108">Définissez la chaîne dans votre script de ressources lors de l’appel de [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou de fonctions connexes.</span><span class="sxs-lookup"><span data-stu-id="a1af0-108">Set the string in your resource script when calling [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) or related functions.</span></span>
-   <span data-ttu-id="a1af0-109">Appelez la fonction [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) .</span><span class="sxs-lookup"><span data-stu-id="a1af0-109">Call the [**SetWindowText**](/windows/desktop/api/winuser/nf-winuser-setwindowtexta) function.</span></span>
-   <span data-ttu-id="a1af0-110">Définissez le nom des contrôles dans les boîtes de dialogue à l’aide des techniques décrites dans la rubrique [nommer des contrôles dans les boîtes de dialogue](naming-controls-in-dialog-boxes.md).</span><span class="sxs-lookup"><span data-stu-id="a1af0-110">Define the name of controls in dialog boxes by using the techniques described in [Naming Controls in Dialog Boxes](naming-controls-in-dialog-boxes.md).</span></span> <span data-ttu-id="a1af0-111">Il s’agit de la seule méthode pour étiqueter un contrôle d’édition, car la définition de l’étiquette intrinsèque Controls modifie le contenu des contrôles.</span><span class="sxs-lookup"><span data-stu-id="a1af0-111">This is the only method for labeling an edit control, because setting the controls intrinsic label changes the controls contents.</span></span>

<span data-ttu-id="a1af0-112">Vous pouvez interroger la légende à l’aide de l’Active Accessibility Microsoft ou du \_ message WM GETTEXT.</span><span class="sxs-lookup"><span data-stu-id="a1af0-112">You can query the caption by using either Microsoft Active Accessibility or the WM\_GETTEXT message.</span></span>

<span data-ttu-id="a1af0-113">Pour plus d’informations sur l’interrogation de la légende à l’aide de Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) .</span><span class="sxs-lookup"><span data-stu-id="a1af0-113">For more information about querying the caption by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
