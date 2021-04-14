---
description: Lorsque vous utilisez les boîtes de dialogue Microsoft Windows, vous devez étiqueter tous les contrôles pour faciliter la fonctionnalité vocale. La boîte de dialogue Exécuter suivante affiche une étiquette de contrôle de texte statique pour une zone de liste déroulante. Le texte statique se termine par un signe deux-points.
ms.assetid: 3b01a4d2-9deb-413f-bab8-566df86b6af9
title: Nommer des contrôles dans les boîtes de dialogue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f0f74ecb3737b422450388ee87ab4177e899aa6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104565160"
---
# <a name="naming-controls-in-dialog-boxes"></a><span data-ttu-id="ff976-105">Nommer des contrôles dans les boîtes de dialogue</span><span class="sxs-lookup"><span data-stu-id="ff976-105">Naming Controls in Dialog Boxes</span></span>

<span data-ttu-id="ff976-106">Lorsque vous utilisez les boîtes de dialogue Microsoft Windows, vous devez étiqueter tous les contrôles pour faciliter la fonctionnalité vocale.</span><span class="sxs-lookup"><span data-stu-id="ff976-106">When using Microsoft Windows dialog boxes, you must label all controls to facilitate speech functionality.</span></span> <span data-ttu-id="ff976-107">La boîte de dialogue **exécuter** suivante affiche une étiquette de contrôle de texte statique pour une zone de liste déroulante.</span><span class="sxs-lookup"><span data-stu-id="ff976-107">The following **Run** dialog box shows a static text control label for a drop-down list box.</span></span> <span data-ttu-id="ff976-108">Le texte statique se termine par un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="ff976-108">Static text ends with a colon.</span></span>

![capture d’écran montrant la boîte de dialogue Exécuter](images/fb0bd076-e9f9-4260-a54a-9d7db93157da.jpg)

<span data-ttu-id="ff976-110">Il existe deux types de contrôles :</span><span class="sxs-lookup"><span data-stu-id="ff976-110">There are two types of controls:</span></span>

-   <span data-ttu-id="ff976-111">Les contrôles qui ont leurs légendes comme propriété de ce contrôle, tels que les boutons de commande et les cases à cocher.</span><span class="sxs-lookup"><span data-stu-id="ff976-111">Controls that have their captions as a property of that control, such as command buttons and check boxes.</span></span> <span data-ttu-id="ff976-112">Les aides à l’accessibilité n’ont aucun problème pour identifier ces contrôles tant que la légende est correctement définie.</span><span class="sxs-lookup"><span data-stu-id="ff976-112">Accessibility aids have no trouble identifying these controls as long as the caption is properly defined.</span></span>
-   <span data-ttu-id="ff976-113">Les contrôles qui n’ont pas leurs propres légendes, tels que les contrôles d’édition, les zones de liste et les affichages de liste, doivent être étiquetés à l’aide de contrôles de texte statique distincts.</span><span class="sxs-lookup"><span data-stu-id="ff976-113">Controls that do not have their own captions, such as edit controls, list boxes and list views, must be labeled by using separate static text controls.</span></span> <span data-ttu-id="ff976-114">Pour plus d’informations sur les contrôles qui n’ont pas leurs propres légendes, consultez [contrôles sans propriétés de légende](controls-without-caption-properties.md).</span><span class="sxs-lookup"><span data-stu-id="ff976-114">For more information about controls that do not have their own captions, see [Controls Without Caption Properties](controls-without-caption-properties.md).</span></span>

<span data-ttu-id="ff976-115">Plusieurs techniques peuvent être utilisées pour surmonter les situations dans lesquelles les contrôles n’ont pas leurs propres légendes, mais elles ne sont effectives que pour les fenêtres qui sont affichées par le gestionnaire de boîtes de dialogue standard (SDM).</span><span class="sxs-lookup"><span data-stu-id="ff976-115">Several techniques can be used to overcome situations in which controls do not have their own captions, but they are only effective for windows that are displayed by the Standard Dialog Manager (SDM).</span></span> <span data-ttu-id="ff976-116">Toutes les autres fenêtres doivent exposer les noms et les relations entre les contrôles en prenant explicitement en charge Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="ff976-116">All other windows need to expose the names and relationship between controls by explicitly supporting Microsoft Active Accessibility.</span></span> <span data-ttu-id="ff976-117">Pour plus d’informations sur Active Accessibility, consultez la section [accessibilité](/windows/desktop/accessibility) de MSDN Library.</span><span class="sxs-lookup"><span data-stu-id="ff976-117">For more information about Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section of the MSDN Library.</span></span>

 

 
