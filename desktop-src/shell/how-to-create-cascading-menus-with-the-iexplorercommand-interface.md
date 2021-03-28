---
description: 'Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de IExplorerCommand :: EnumSubCommands.'
ms.assetid: 010157F3-B950-4A57-B0AA-248B4990DA34
title: Créer des menus en cascade avec l’interface IExplorerCommand
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afb88a7ac04857ac64e79115a4e8984d325e47b
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104560965"
---
# <a name="how-to-create-cascading-menus-with-the-iexplorercommand-interface"></a><span data-ttu-id="f5fed-103">Comment créer des menus en cascade avec l’interface IExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="f5fed-103">How to Create Cascading Menus with the IExplorerCommand Interface</span></span>

<span data-ttu-id="f5fed-104">Vous pouvez également ajouter des verbes à un menu en cascade à l’aide de [**IExplorerCommand :: EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span><span class="sxs-lookup"><span data-stu-id="f5fed-104">Another option for adding verbs to a cascading menu is through [**IExplorerCommand::EnumSubCommands**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-enumsubcommands).</span></span> <span data-ttu-id="f5fed-105">Cette méthode permet aux sources de données qui fournissent leurs commandes de module de commande par le biais de l’interface [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) d’utiliser ces commandes comme verbes dans un menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="f5fed-105">This method enables data sources that provide their command module commands through the [**IExplorerCommandProvider**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider) interface to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="f5fed-106">Dans Windows 7 et versions ultérieures, vous pouvez fournir la même implémentation de verbe à l’aide de l’interface [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) , comme vous pouvez le faire avec l’interface [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) .</span><span class="sxs-lookup"><span data-stu-id="f5fed-106">In Windows 7 and later, you can provide the same verb implementation using the [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) interface as you can with the [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) interface.</span></span>

## <a name="instructions"></a><span data-ttu-id="f5fed-107">Instructions</span><span class="sxs-lookup"><span data-stu-id="f5fed-107">Instructions</span></span>


<span data-ttu-id="f5fed-108">Les deux captures d’écran suivantes illustrent l’utilisation des menus en cascade dans le dossier **appareils** .</span><span class="sxs-lookup"><span data-stu-id="f5fed-108">The following two screen shots illustrate the use of cascading menus in the **Devices** folder.</span></span>

![Capture d’écran montrant un exemple de menu en cascade dans le dossier appareils.](images/file-assoc/filecascademenu.png)

![capture d’écran montrant un exemple de menu en cascade dans le dossier appareils](images/file-assoc/cascadedevices2.png)

## <a name="remarks"></a><span data-ttu-id="f5fed-111">Notes</span><span class="sxs-lookup"><span data-stu-id="f5fed-111">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f5fed-112">Étant donné que [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) prend uniquement en charge l’activation in-process, il est recommandé d’utiliser des sources de données Shell qui doivent partager l’implémentation entre des commandes et des menus contextuels.</span><span class="sxs-lookup"><span data-stu-id="f5fed-112">Because [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f5fed-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f5fed-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5fed-114">**IExplorerCommand**</span><span class="sxs-lookup"><span data-stu-id="f5fed-114">**IExplorerCommand**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)
</dt> <dt>

[<span data-ttu-id="f5fed-115">**IExplorerCommandProvider**</span><span class="sxs-lookup"><span data-stu-id="f5fed-115">**IExplorerCommandProvider**</span></span>](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider)
</dt> <dt>

[<span data-ttu-id="f5fed-116">**IContextMenu**</span><span class="sxs-lookup"><span data-stu-id="f5fed-116">**IContextMenu**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)
</dt> </dl>

 

 
