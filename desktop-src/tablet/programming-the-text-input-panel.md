---
description: À compter de Windows Vista, le TextInputPanel remplace le PenInputPanel pour contrôler l’apparence et le comportement à l’écran du panneau de saisie de tablette. les sections suivantes décrivent la programmation du panneau de saisie à l’aide des interfaces de programmation d’application du panneau de saisie de texte. TextInputPanel pour les utilisateurs du panneau de saisie PenInputPanelUsing correction de texte AutoCompleteEnabling pour l’encre personnalisée CollectorsNote le panneau de saisie de texte est implémenté dans un fichier exécutable appelé TabTip.exe. L’exécution de TabTip.exe avec le paramètre/SeekDesktop tente d’exécuter une version de fonctionnalité réduite du panneau de saisie sur un bureau interactif non standard, tel qu’il est créé avec CreateDesktop. Pour la plupart des bureaux créés, le panneau de saisie s’exécutera automatiquement dans ce mode. Ce paramètre permet de le lancer dans des scénarios d’application inhabituels qui, sinon, empêchent le lancement automatique. Si le panneau de saisie est déjà en cours d’exécution sur le bureau, ce paramètre n’a aucun effet et l’instance de TabTip.exe s’arrête immédiatement.
ms.assetid: af0a2946-88d0-4f2e-98ca-446398aeb6b8
title: Programmation du panneau de saisie de texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5e6b379a26199e602fc68402d77fa89fb4f8fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536655"
---
# <a name="programming-the-text-input-panel"></a><span data-ttu-id="2add1-107">Programmation du panneau de saisie de texte</span><span class="sxs-lookup"><span data-stu-id="2add1-107">Programming the Text Input Panel</span></span>

<span data-ttu-id="2add1-108">À compter de Windows Vista, le [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) remplace le [**PenInputPanel**](peninputpanel-class.md) pour contrôler l’apparence et le comportement à l’écran du panneau de saisie Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="2add1-108">Starting with Windows Vista, the [**TextInputPanel**](/windows/desktop/api/peninputpanel/nn-peninputpanel-itextinputpanel) supersedes the [**PenInputPanel**](peninputpanel-class.md) for controlling the onscreen appearance and behavior of the Tablet Input Panel.</span></span>

<span data-ttu-id="2add1-109">Les sections suivantes décrivent la programmation du panneau de saisie à l’aide des interfaces de programmation d’application du panneau de saisie de texte.</span><span class="sxs-lookup"><span data-stu-id="2add1-109">The following sections describe programming the Input Panel using the Text Input Panel application programming interfaces.</span></span>

-   [<span data-ttu-id="2add1-110">TextInputPanel pour les utilisateurs de PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="2add1-110">TextInputPanel for Users of PenInputPanel</span></span>](textinputpanel-for-users-of-peninputpanel.md)
-   [<span data-ttu-id="2add1-111">Utilisation de la saisie semi-automatique du panneau de saisie</span><span class="sxs-lookup"><span data-stu-id="2add1-111">Using Input Panel AutoComplete</span></span>](using-input-panel-autocomplete.md)
-   [<span data-ttu-id="2add1-112">Activation de la correction de texte pour les collecteurs d’encre personnalisés</span><span class="sxs-lookup"><span data-stu-id="2add1-112">Enabling Text Correction for Custom Ink Collectors</span></span>](enabling-text-correction-for-custom-ink-collectors.md)

> [!Note]  
> <span data-ttu-id="2add1-113">Le panneau de saisie de texte est implémenté dans un fichier exécutable appelé TabTip.exe.</span><span class="sxs-lookup"><span data-stu-id="2add1-113">The Text Input Panel is implemented in an executable file called TabTip.exe.</span></span> <span data-ttu-id="2add1-114">L’exécution de TabTip.exe avec le paramètre */SeekDesktop* tente d’exécuter une version de fonctionnalité réduite du panneau de saisie sur un bureau interactif non standard, tel qu’il est créé avec [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span><span class="sxs-lookup"><span data-stu-id="2add1-114">Running TabTip.exe with the */SeekDesktop* parameter attempts to run a reduced functionality version of Input Panel on a nonstandard interactive desktop, as created with [**CreateDesktop**](/windows/win32/api/winuser/nf-winuser-createdesktopa).</span></span> <span data-ttu-id="2add1-115">Pour la plupart des bureaux créés, le panneau de saisie s’exécutera automatiquement dans ce mode.</span><span class="sxs-lookup"><span data-stu-id="2add1-115">For most created desktops, Input Panel will automatically run in this mode already.</span></span> <span data-ttu-id="2add1-116">Ce paramètre permet de le lancer dans des scénarios d’application inhabituels qui, sinon, empêchent le lancement automatique.</span><span class="sxs-lookup"><span data-stu-id="2add1-116">This parameter provides the means for launching it in unusual application scenarios that otherwise prevent the automatic launch.</span></span> <span data-ttu-id="2add1-117">Si le panneau de saisie est déjà en cours d’exécution sur le bureau, ce paramètre n’a aucun effet et l’instance de TabTip.exe s’arrête immédiatement.</span><span class="sxs-lookup"><span data-stu-id="2add1-117">If Input Panel is already running on the desktop, this parameter will have no effect and the instance of TabTip.exe will exit immediately.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="2add1-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2add1-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2add1-119">Programmation du panneau de saisie à l’aide de la classe PenInputPanel</span><span class="sxs-lookup"><span data-stu-id="2add1-119">Programming the Input Panel Using the PenInputPanel Class</span></span>](programming-the-input-panel-using-the-peninputpanel-class.md)
</dt> </dl>

 

 
