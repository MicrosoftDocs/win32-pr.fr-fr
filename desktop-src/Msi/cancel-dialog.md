---
description: Une boîte de dialogue annuler confirme que l’utilisateur souhaite mettre fin à l’installation. Il s’agit d’une boîte de dialogue modale.
ms.assetid: 5dab4315-721e-417d-91e0-b38653a65c23
title: Boîte de dialogue annuler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1022a7613f3f5341d8c833b7cbe2645ce871aeb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534475"
---
# <a name="cancel-dialog"></a><span data-ttu-id="cca34-104">Boîte de dialogue annuler</span><span class="sxs-lookup"><span data-stu-id="cca34-104">Cancel Dialog</span></span>

<span data-ttu-id="cca34-105">Une boîte de dialogue **Annuler** confirme que l’utilisateur souhaite mettre fin à l’installation.</span><span class="sxs-lookup"><span data-stu-id="cca34-105">A **Cancel** dialog box confirms that the user wants to terminate the installation.</span></span> <span data-ttu-id="cca34-106">Il s’agit d’une boîte de dialogue modale.</span><span class="sxs-lookup"><span data-stu-id="cca34-106">This is a modal dialog box.</span></span>

<span data-ttu-id="cca34-107">Ce type de boîte de dialogue contient généralement un [contrôle de texte](text-control.md) et deux [boutons](pushbutton-control.md)de commande.</span><span class="sxs-lookup"><span data-stu-id="cca34-107">This type of dialog box commonly contains a [Text control](text-control.md) and two [PushButtons](pushbutton-control.md).</span></span> <span data-ttu-id="cca34-108">Les deux boutons permettent à l’utilisateur de choisir de retourner à la dernière boîte de dialogue ou de confirmer l’arrêt de l’installation.</span><span class="sxs-lookup"><span data-stu-id="cca34-108">The two buttons give the user the choice of either returning to the last dialog box or confirming the termination of the installation.</span></span>

<span data-ttu-id="cca34-109">Le ControlEvent, [EndDialog](enddialog-controlevent.md) est lié à ces deux boutons dans la [table ControlEvent,](controlevent-table.md).</span><span class="sxs-lookup"><span data-stu-id="cca34-109">The [EndDialog](enddialog-controlevent.md) ControlEvent is linked to these two buttons in the [ControlEvent table](controlevent-table.md).</span></span> <span data-ttu-id="cca34-110">Le paramètre de *retour* de l’ControlEvent, EndDialog est lié à l’un des boutons et entraîne l’arrêt de la boîte de dialogue **Annuler** et le focus pour revenir à la boîte de dialogue précédente.</span><span class="sxs-lookup"><span data-stu-id="cca34-110">The *Return* parameter of the EndDialog ControlEvent is linked to one of the buttons and causes the **Cancel** dialog box to be terminated and the focus to return to the previous dialog box.</span></span> <span data-ttu-id="cca34-111">Le paramètre de *sortie* est lié à l’autre bouton et fait en sorte que l’interface utilisateur retourne le contrôle au programme d’installation avec le code approprié indiquant que l’utilisateur souhaite quitter.</span><span class="sxs-lookup"><span data-stu-id="cca34-111">The *Exit* parameter is linked to the other button and causes the user interface to return control to the installer with the appropriate code indicating that the user wants to exit.</span></span> <span data-ttu-id="cca34-112">Le programme d’installation s’arrête ensuite et affiche la [boîte de dialogue UserExit](userexit-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="cca34-112">The installer then shuts down and displays the [UserExit Dialog](userexit-dialog.md).</span></span>

 

 



