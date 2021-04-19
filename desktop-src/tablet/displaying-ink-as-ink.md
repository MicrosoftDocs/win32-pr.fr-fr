---
description: Le comportement par défaut du contrôle InkEdit consiste à reconnaître et convertir l’encre en texte après l’expiration d’un bref délai d’attente.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Affichage de l’encre sous forme d’encre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518856"
---
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="b6eaf-103">Affichage de l’encre sous forme d’encre</span><span class="sxs-lookup"><span data-stu-id="b6eaf-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="b6eaf-104">Le comportement par défaut du contrôle [InkEdit](inkedit-control-reference.md) consiste à reconnaître et convertir l’encre en texte après l’expiration d’un bref délai d’attente.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="b6eaf-105">Étant donné que le contrôle est une superclasse de [RichEdit](../controls/rich-edit-controls.md), il est également possible d’incorporer et d’afficher de l’encre dans le contrôle.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="b6eaf-106">Chaque mot est inséré dans le contrôle en tant qu’objet [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="b6eaf-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="b6eaf-107">L’objet **InkDisp** contient l’encre et ses alternatives de reconnaissance.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="b6eaf-108">Lorsqu’elle est insérée, l’encre est mise à l’échelle en fonction de la taille de police actuelle et d’autres propriétés ambiantes, telles que l’italique ou le gras, sont appliquées.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="b6eaf-109">Si l’utilisateur choisit de modifier le texte d’un objet [**InkDisp**](inkdisp-class.md) , il doit d’abord convertir l’entrée manuscrite en texte.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="b6eaf-110">Toutes les autres données d’encre et de reconnaissance sont perdues lors de la conversion.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="b6eaf-111">Cette fonctionnalité est disponible uniquement sur les ordinateurs qui exécutent Microsoft Windows XP Édition Tablet PC, Windows Vista ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="b6eaf-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
