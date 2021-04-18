---
description: Un IME implémente une fonctionnalité appelée &\# 0034 ; reconversion&\# 0034 ;.
ms.assetid: 32b20872-7e5c-487e-99bb-9447ac3aebd4
title: Utilisation de la reconversion avec un IME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e28383a27fd7fd7827cbbf3c7ff97c895fb4a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106512920"
---
# <a name="using-reconversion-with-an-ime"></a><span data-ttu-id="89126-103">Utilisation de la reconversion avec un IME</span><span class="sxs-lookup"><span data-stu-id="89126-103">Using Reconversion with an IME</span></span>

<span data-ttu-id="89126-104">Un IME implémente une fonctionnalité appelée « reconversion ».</span><span class="sxs-lookup"><span data-stu-id="89126-104">An IME implements a feature called "reconversion".</span></span> <span data-ttu-id="89126-105">Normalement, le IMM détermine les listes de candidats en fonction uniquement des entrées tapées par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="89126-105">Normally the IMM determines the lists of candidates based only on entries typed by the user.</span></span> <span data-ttu-id="89126-106">La reconversion permet au IMM de déterminer un ou plusieurs candidats en fonction de la phrase contenante (le contexte).</span><span class="sxs-lookup"><span data-stu-id="89126-106">Reconversion allows the IMM to determine one or more candidates based on the containing sentence (the context).</span></span> <span data-ttu-id="89126-107">Les types de reconversion définis sont simple, normal et amélioré.</span><span class="sxs-lookup"><span data-stu-id="89126-107">The defined reconversion types are simple, normal, and enhanced.</span></span>

<span data-ttu-id="89126-108">La reconversion est utile lorsqu’un utilisateur constate une erreur de composition dans un document.</span><span class="sxs-lookup"><span data-stu-id="89126-108">Reconversion is useful when a user notices a composition error in a document.</span></span> <span data-ttu-id="89126-109">L’utilisateur peut sélectionner l’erreur et choisir reconversion dans un menu.</span><span class="sxs-lookup"><span data-stu-id="89126-109">The user can select the error and choose reconversion from a menu.</span></span> <span data-ttu-id="89126-110">L’IME utilise le contexte pour déterminer le meilleur remplacement.</span><span class="sxs-lookup"><span data-stu-id="89126-110">The IME uses the context to determine the best replacement.</span></span> <span data-ttu-id="89126-111">L’application peut utiliser [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) pour prendre en charge la reconversion.</span><span class="sxs-lookup"><span data-stu-id="89126-111">The application can use [**ImmSetCompositionString**](/windows/desktop/api/Imm/nf-imm-immsetcompositionstringa) to support reconversion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="89126-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="89126-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89126-113">Utilisation du gestionnaire de méthode d’entrée</span><span class="sxs-lookup"><span data-stu-id="89126-113">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 



