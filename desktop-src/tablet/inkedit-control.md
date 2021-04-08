---
description: Le contrôle InkEdit offre un moyen simple de capturer, reconnaître et afficher de l’encre.
ms.assetid: a1dfa254-cade-44c5-8fdd-74bb40849063
title: InkEdit, contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf6d5441506ee791eefddba05b9b1f3ddb8a8ec4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866138"
---
# <a name="inkedit-control"></a><span data-ttu-id="acbcc-103">InkEdit, contrôle</span><span class="sxs-lookup"><span data-stu-id="acbcc-103">InkEdit Control</span></span>

<span data-ttu-id="acbcc-104">Le contrôle [InkEdit](inkedit-control-reference.md) offre un moyen simple de capturer, reconnaître et afficher de l’encre.</span><span class="sxs-lookup"><span data-stu-id="acbcc-104">The [InkEdit](inkedit-control-reference.md) control provides an easy way to capture, recognize, and display ink.</span></span>

<span data-ttu-id="acbcc-105">Cette implémentation du contrôle [InkEdit](inkedit-control-reference.md) est basée sur le contrôle [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) .</span><span class="sxs-lookup"><span data-stu-id="acbcc-105">This implementation of the [InkEdit](inkedit-control-reference.md) control is based on the [**RichEdit**](/windows/desktop/api/richole/nn-richole-iricheditole) control.</span></span> <span data-ttu-id="acbcc-106">L’implémentation managée (.NET Framework) de [InkEdit](/previous-versions/ms835842(v=msdn.10)) est basée sur le contrôle [**RichTextBox**](/previous-versions/windows/) .</span><span class="sxs-lookup"><span data-stu-id="acbcc-106">The managed (.NET Framework) implementation of [InkEdit](/previous-versions/ms835842(v=msdn.10)) is based on the [**RichTextBox**](/previous-versions/windows/) control.</span></span>

<span data-ttu-id="acbcc-107">L’objectif principal du contrôle [InkEdit](inkedit-control-reference.md) est de collecter l’encre, de la reconnaître et de l’afficher sous forme de texte.</span><span class="sxs-lookup"><span data-stu-id="acbcc-107">The primary purpose of the [InkEdit](inkedit-control-reference.md) control is to collect ink, recognize it, and display it in text form.</span></span> <span data-ttu-id="acbcc-108">En outre, il prend en charge l’affichage de l’encre comme un objet incorporé avec des fonctionnalités de mise en forme du texte, telles que le gras et le soulignement.</span><span class="sxs-lookup"><span data-stu-id="acbcc-108">Additionally, it supports displaying ink as an embedded object with text formatting capabilities, such as bold and underline.</span></span>

## <a name="gestures-and-correction"></a><span data-ttu-id="acbcc-109">Mouvements et correction</span><span class="sxs-lookup"><span data-stu-id="acbcc-109">Gestures and Correction</span></span>

<span data-ttu-id="acbcc-110">[InkEdit](inkedit-control-reference.md) prend en charge les gestes suivants.</span><span class="sxs-lookup"><span data-stu-id="acbcc-110">[InkEdit](inkedit-control-reference.md) supports the following gestures.</span></span>



| <span data-ttu-id="acbcc-111">Mouvement</span><span class="sxs-lookup"><span data-stu-id="acbcc-111">Gesture</span></span>                                                                    | <span data-ttu-id="acbcc-112">Nom du geste</span><span class="sxs-lookup"><span data-stu-id="acbcc-112">Gesture Name</span></span>              | <span data-ttu-id="acbcc-113">Action</span><span class="sxs-lookup"><span data-stu-id="acbcc-113">Action</span></span>               |
|----------------------------------------------------------------------------|---------------------------|----------------------|
| ![geste vers le gauche](images/d8b00c0a-f450-4f71-980f-3bca1b558e4c.gif)      | <span data-ttu-id="acbcc-115">Vers le gauche</span><span class="sxs-lookup"><span data-stu-id="acbcc-115">Down-left</span></span><br/>      | <span data-ttu-id="acbcc-116">Entrez</span><span class="sxs-lookup"><span data-stu-id="acbcc-116">Enter</span></span><br/>     |
| ![geste vers le long-gauche-long](images/b8cb23b5-b947-477d-922f-2ffb42756804.gif) | <span data-ttu-id="acbcc-118">En baisse à gauche</span><span class="sxs-lookup"><span data-stu-id="acbcc-118">Down-left-long</span></span><br/> | <span data-ttu-id="acbcc-119">Entrez</span><span class="sxs-lookup"><span data-stu-id="acbcc-119">Enter</span></span><br/>     |
| ![geste vers le haut](images/02c34d24-c2d7-404f-b99a-742ba6de7f0c.gif)       | <span data-ttu-id="acbcc-121">En haut à droite</span><span class="sxs-lookup"><span data-stu-id="acbcc-121">Up-right</span></span><br/>       | <span data-ttu-id="acbcc-122">Onglet</span><span class="sxs-lookup"><span data-stu-id="acbcc-122">Tab</span></span><br/>       |
| ![geste vers le haut à droite.](images/5e3522d3-2920-4a86-86ae-f29b01d93993.gif) | <span data-ttu-id="acbcc-124">Up-Right-long</span><span class="sxs-lookup"><span data-stu-id="acbcc-124">Up-right-long</span></span><br/>  | <span data-ttu-id="acbcc-125">Onglet</span><span class="sxs-lookup"><span data-stu-id="acbcc-125">Tab</span></span><br/>       |
| ![mouvement de droite](images/864cf4e1-2619-49cf-ac96-72994232e465.jpg)          | <span data-ttu-id="acbcc-127">Right</span><span class="sxs-lookup"><span data-stu-id="acbcc-127">Right</span></span><br/>          | <span data-ttu-id="acbcc-128">Espace</span><span class="sxs-lookup"><span data-stu-id="acbcc-128">Space</span></span><br/>     |
| ![mouvement de gauche](images/ce60cc20-1769-428d-80de-7f47c86021fb.jpg)           | <span data-ttu-id="acbcc-130">Gauche</span><span class="sxs-lookup"><span data-stu-id="acbcc-130">Left</span></span><br/>           | <span data-ttu-id="acbcc-131">Retour arrière</span><span class="sxs-lookup"><span data-stu-id="acbcc-131">Backspace</span></span><br/> |



 

<span data-ttu-id="acbcc-132">Les événements de mouvement que vous pouvez gérer contiennent des informations de mouvement, de trait et de curseur que vous pouvez utiliser pour envoyer du texte à [InkEdit](inkedit-control-reference.md) ou placer des données dans le presse-papiers.</span><span class="sxs-lookup"><span data-stu-id="acbcc-132">Gesture events that you can handle contain gesture, stroke, and cursor information you can use to send text to [InkEdit](inkedit-control-reference.md) or place data on the clipboard.</span></span>

<span data-ttu-id="acbcc-133">[InkEdit](inkedit-control-reference.md) fournit également une interface utilisateur de correction qui permet aux utilisateurs d’afficher et de sélectionner parmi d’autres, d’utiliser le clavier visuel et les détecteurs de caractères/lettres/bloc.</span><span class="sxs-lookup"><span data-stu-id="acbcc-133">[InkEdit](inkedit-control-reference.md) also provides a correction user interface that enables users to view and select from alternates, use the on-screen keyboard, and character/letter/block recognizers.</span></span>

## <a name="other-details"></a><span data-ttu-id="acbcc-134">Autres détails</span><span class="sxs-lookup"><span data-stu-id="acbcc-134">Other Details</span></span>

<span data-ttu-id="acbcc-135">[InkEdit](inkedit-control-reference.md) est conçu pour fonctionner correctement dans un scénario de formulaire pour une ligne unique, ainsi que pour la saisie et la modification de texte multiligne.</span><span class="sxs-lookup"><span data-stu-id="acbcc-135">[InkEdit](inkedit-control-reference.md) is designed to work well in a form scenario for single line as well as multiline text entry and editing.</span></span> <span data-ttu-id="acbcc-136">L’utilisation principale prévue pour InkEdit consiste à obtenir la saisie de texte d’un utilisateur sous la forme d’une écriture manuscrite.</span><span class="sxs-lookup"><span data-stu-id="acbcc-136">The primary intended use for InkEdit is to get text input from a user in the form of handwriting.</span></span> <span data-ttu-id="acbcc-137">Par défaut, l’entrée manuscrite est reconnue et le texte est inséré à la place.</span><span class="sxs-lookup"><span data-stu-id="acbcc-137">By default, ink input is recognized and text is inserted in its place.</span></span> <span data-ttu-id="acbcc-138">L’interface utilisateur par défaut pour InkEdit ressemble à celle du contrôle [**RichTextBox**](/previous-versions/windows/) , sauf lorsque l’utilisateur fixe une entrée manuscrite.</span><span class="sxs-lookup"><span data-stu-id="acbcc-138">The default user interface for InkEdit resembles that of the [**RichTextBox**](/previous-versions/windows/) control, except when the user is laying down ink.</span></span> <span data-ttu-id="acbcc-139">Vous pouvez afficher l’encre d’origine plutôt que le texte. Toutefois, l’encre est mise à l’échelle en fonction de la taille actuelle de la police d’entrée du contrôle InkEdit et s’affiche en ligne avec un autre texte.</span><span class="sxs-lookup"><span data-stu-id="acbcc-139">You can display original ink rather than text; however, the ink is scaled to the current input font size of the InkEdit control and is displayed inline with other text.</span></span>

> [!Note]  
> <span data-ttu-id="acbcc-140">Pour des raisons de sécurité, vous devez utiliser des procédures standard pour ouvrir ou fermer un fichier, diffuser en continu l’entrée/sortie et définir la propriété [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) ou [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) .</span><span class="sxs-lookup"><span data-stu-id="acbcc-140">For security reasons, you must use standard procedures to open or close a file, stream the input/output, and set the [**RTF**](/windows/desktop/api/inked/nf-inked-iinkedit-get_selrtf) or [**Text**](/windows/desktop/api/inked/nf-inked-iinkedit-get_seltext) property.</span></span>

 

<span data-ttu-id="acbcc-141">Le contrôle [InkEdit](inkedit-control-reference.md) est défini pour reconnaître l’entrée manuscrite comme texte par défaut.</span><span class="sxs-lookup"><span data-stu-id="acbcc-141">The [InkEdit](inkedit-control-reference.md) control is set to recognize ink as text by default.</span></span> <span data-ttu-id="acbcc-142">Pour permettre aux utilisateurs d’ajouter de l’encre comme entrée manuscrite, affectez à la propriété [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) la valeur **InsertAsInk**.</span><span class="sxs-lookup"><span data-stu-id="acbcc-142">To enable users to add ink as ink, set the [**InkInsertMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkinsertmode) property to **InsertAsInk**.</span></span>

<span data-ttu-id="acbcc-143">Pour obtenir des informations de référence détaillées sur le contrôle [InkEdit](inkedit-control-reference.md) , consultez InkEdit.</span><span class="sxs-lookup"><span data-stu-id="acbcc-143">For detailed reference information about the [InkEdit](inkedit-control-reference.md) control, see InkEdit.</span></span>

> [!Note]  
> <span data-ttu-id="acbcc-144">Si vous utilisez le contrôle [InkEdit](inkedit-control-reference.md) Win32 et le placez à l’intérieur d’une zone de groupe, assurez-vous que la zone a un style transparent ; dans le cas contraire, InkEdit n’est pas en mesure de collecter l’encre.</span><span class="sxs-lookup"><span data-stu-id="acbcc-144">If you use the Win32 [InkEdit](inkedit-control-reference.md) control and place it inside a group box, make sure the box has a transparent style; otherwise, InkEdit is not able to collect ink.</span></span>

 

> [!Note]  
> <span data-ttu-id="acbcc-145">Pour vous assurer que l’entrée manuscrite est correctement affichée, appelez la méthode d' [**actualisation**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) du contrôle [InkEdit](inkedit-control-reference.md) lorsqu’elle reçoit un événement [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) ou [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) .</span><span class="sxs-lookup"><span data-stu-id="acbcc-145">To ensure ink is displayed properly, call the [InkEdit](inkedit-control-reference.md) control [**Refresh**](/windows/desktop/api/inked/nf-inked-iinkedit-refresh) method when it receives an [**HScroll**](/dotnet/api/system.windows.forms.richtextbox.hscroll?view=netcore-3.1) or [**VScroll**](/dotnet/api/system.windows.forms.richtextbox.vscroll?view=netcore-3.1) event.</span></span>

 

<span data-ttu-id="acbcc-146">Les sections suivantes détaillent l’utilisation du contrôle [InkEdit](inkedit-control-reference.md) :</span><span class="sxs-lookup"><span data-stu-id="acbcc-146">The following sections detail the use of the [InkEdit](inkedit-control-reference.md) control:</span></span>

-   [<span data-ttu-id="acbcc-147">Instanciation de InkEdit</span><span class="sxs-lookup"><span data-stu-id="acbcc-147">Instantiating InkEdit</span></span>](instantiating-inkedit.md)
-   [<span data-ttu-id="acbcc-148">Word et reconnaissance de caractères</span><span class="sxs-lookup"><span data-stu-id="acbcc-148">Word vs. Character Recognition</span></span>](word-vs--character-recognition.md)
-   [<span data-ttu-id="acbcc-149">Affichage de l’encre sous forme d’encre</span><span class="sxs-lookup"><span data-stu-id="acbcc-149">Displaying Ink as Ink</span></span>](displaying-ink-as-ink.md)
-   [<span data-ttu-id="acbcc-150">Utilisation d’InkEdit sur les versions antérieures de Windows</span><span class="sxs-lookup"><span data-stu-id="acbcc-150">Using InkEdit on Earlier Versions of Windows</span></span>](using-inkedit-on-earlier-versions-of-windows.md)
-   [<span data-ttu-id="acbcc-151">Utilisation d’un dictionnaire d’applications avec InkEdit</span><span class="sxs-lookup"><span data-stu-id="acbcc-151">Using an Application Dictionary with InkEdit</span></span>](using-an-application-dictionary-with-inkedit.md)

 

