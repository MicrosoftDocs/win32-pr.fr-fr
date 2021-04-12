---
title: Indicateurs d’initialisation de la boîte de dialogue commune
description: Les indicateurs sont utilisés pour modifier le comportement et l’apparence d’une boîte de dialogue commune.
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- Bibliothèque de boîtes de dialogue communes, initialisation
- boîtes de dialogue communes, initialisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/19/2020
ms.locfileid: "104463983"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="8ab50-105">Indicateurs d’initialisation de la boîte de dialogue commune</span><span class="sxs-lookup"><span data-stu-id="8ab50-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="8ab50-106">Les indicateurs sont utilisés pour modifier le comportement et l’apparence d’une boîte de dialogue commune.</span><span class="sxs-lookup"><span data-stu-id="8ab50-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="8ab50-107">Les indicateurs d’initialisation sont les valeurs que vous définissez dans le membre **Flags** de la structure utilisée pour créer la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8ab50-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="8ab50-108">Vous utilisez les indicateurs pour spécifier les contrôles d’une boîte de dialogue qui reçoivent des valeurs initiales, pour désactiver les contrôles sélectionnés et pour modifier la plage de valeurs que l’utilisateur peut définir avec les contrôles.</span><span class="sxs-lookup"><span data-stu-id="8ab50-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="8ab50-109">Vous utilisez également les indicateurs pour activer les procédures de hook et les modèles personnalisés pour les boîtes de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8ab50-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="8ab50-110">Par exemple, vous pouvez définir la valeur des **\_ effets CF** dans le membre **Flags** de la structure [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) pour indiquer à la boîte de dialogue **police** d’afficher les contrôles Effects.</span><span class="sxs-lookup"><span data-stu-id="8ab50-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="8ab50-111">Ces contrôles permettent à l’utilisateur de choisir une couleur de police, ainsi que les effets du barré et du trait de soulignement.</span><span class="sxs-lookup"><span data-stu-id="8ab50-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="8ab50-112">Les valeurs d’indicateur d’initialisation sont uniques à chaque boîte de dialogue commune et sont décrites en détail par les membres **indicateurs** des structures suivantes qui correspondent :</span><span class="sxs-lookup"><span data-stu-id="8ab50-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="8ab50-113">**LES ChooseColor.**</span><span class="sxs-lookup"><span data-stu-id="8ab50-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="8ab50-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="8ab50-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="8ab50-115">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="8ab50-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="8ab50-116">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="8ab50-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="8ab50-117">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="8ab50-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="8ab50-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="8ab50-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="8ab50-119">**PRINTDLGEX**</span><span class="sxs-lookup"><span data-stu-id="8ab50-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




