---
title: Fenêtre de caractères
description: Fenêtre de caractères
ms.assetid: 92b6111f-b52d-4720-8bd9-59585d826bf5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a386dc769e2b5fe7313b768d1b2debfe4a1131
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383356"
---
# <a name="the-character-window"></a><span data-ttu-id="f304e-103">Fenêtre de caractères</span><span class="sxs-lookup"><span data-stu-id="f304e-103">The Character Window</span></span>

<span data-ttu-id="f304e-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="f304e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="f304e-105">Microsoft Agent affiche les caractères animés dans leurs propres fenêtres qui apparaissent toujours en haut de l’ordre de plan de la fenêtre (c’est-à-dire toujours visible).</span><span class="sxs-lookup"><span data-stu-id="f304e-105">Microsoft Agent displays animated characters in their own windows that always appear at the top of the window z-order (that is, always on top).</span></span> <span data-ttu-id="f304e-106">Un utilisateur peut déplacer la fenêtre d’un caractère en faisant glisser le caractère avec le bouton gauche de la souris.</span><span class="sxs-lookup"><span data-stu-id="f304e-106">A user can move a character's window by dragging the character with the left mouse button.</span></span> <span data-ttu-id="f304e-107">L’image de caractère se déplace avec le pointeur.</span><span class="sxs-lookup"><span data-stu-id="f304e-107">The character image moves with the pointer.</span></span> <span data-ttu-id="f304e-108">En outre, une application peut déplacer un caractère à l’aide de la méthode [**MoveTo**](moveto-method.md) .</span><span class="sxs-lookup"><span data-stu-id="f304e-108">In addition, an application can move a character using the [**MoveTo**](moveto-method.md) method.</span></span>

<span data-ttu-id="f304e-109">Quand l’utilisateur clique avec le bouton droit sur un caractère, un menu contextuel s’affiche avec les commandes suivantes :</span><span class="sxs-lookup"><span data-stu-id="f304e-109">When the user right-clicks a character, a pop-up menu appears that displays the following commands:</span></span>

<span data-ttu-id="f304e-110">Ouvrir la \| fenêtre fermer les commandes <span class="underline">V</span>OCAL</span><span class="sxs-lookup"><span data-stu-id="f304e-110">Open \| Close <span class="underline">V</span>oice Commands Window</span></span>

<span data-ttu-id="f304e-111">IDE <span class="underline">H</span></span><span class="sxs-lookup"><span data-stu-id="f304e-111"><span class="underline">H</span>ide</span></span>

<span data-ttu-id="f304e-112">----------------------------…</span><span class="sxs-lookup"><span data-stu-id="f304e-112">----------------------------…</span></span>

<span data-ttu-id="f304e-113">Commande\*</span><span class="sxs-lookup"><span data-stu-id="f304e-113">Command\*</span></span>


<span data-ttu-id="f304e-114">*OtherHostingApplicationCaption\*\**</span><span class="sxs-lookup"><span data-stu-id="f304e-114">*OtherHostingApplicationCaption\*\**</span></span>

<span data-ttu-id="f304e-115">\*Les commandes répertoriées sont basées sur le client d’entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="f304e-115">\*Commands listed are based on the input-active client.</span></span> <span data-ttu-id="f304e-116">Pour plus d’informations sur la définition des commandes qui s’affichent dans le menu contextuel, consultez la vue d’ensemble de l’interface de programmation Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f304e-116">For more information on defining commands that appear in the pop-up menu, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="f304e-117">\*\*Les entrées répertoriées sont toutes les autres applications qui hébergent actuellement le caractère.</span><span class="sxs-lookup"><span data-stu-id="f304e-117">\*\*Entries listed are all other applications currently hosting the character.</span></span> <span data-ttu-id="f304e-118">Pour plus d’informations sur la définition de cette entrée, consultez la vue d’ensemble de l’interface de programmation Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="f304e-118">For more information on defining this entry, see The Microsoft Agent Programming Interface Overview.</span></span>

<span data-ttu-id="f304e-119">La \| commande ouvrir fermer les commandes vocales de la fenêtre contrôle l’affichage de la fenêtre commandes du caractère actif actuel.</span><span class="sxs-lookup"><span data-stu-id="f304e-119">The Open \| Close Voice Commands Window command controls the display of the Commands Window of the current active character.</span></span> <span data-ttu-id="f304e-120">Si les services de reconnaissance vocale sont désactivés, cette commande est désactivée.</span><span class="sxs-lookup"><span data-stu-id="f304e-120">If speech recognition services are disabled, this command is disabled.</span></span> <span data-ttu-id="f304e-121">Si les services de reconnaissance vocale ne sont pas installés, cette commande n’apparaît pas.</span><span class="sxs-lookup"><span data-stu-id="f304e-121">If speech recognition services are not installed, this command does not appear.</span></span>

<span data-ttu-id="f304e-122">La commande masquer masque le caractère.</span><span class="sxs-lookup"><span data-stu-id="f304e-122">The Hide command hides the character.</span></span> <span data-ttu-id="f304e-123">L’animation assignée à l’état de **masquage** du caractère lit et masque le caractère.</span><span class="sxs-lookup"><span data-stu-id="f304e-123">The animation assigned to the character's **Hiding** state plays and hides the character.</span></span> <span data-ttu-id="f304e-124">La lettre « H » dans Hide est la clé d’accès de la commande (mnémonique).</span><span class="sxs-lookup"><span data-stu-id="f304e-124">The letter "H" in hide is the command's access key (mnemonic).</span></span>

<span data-ttu-id="f304e-125">Les commandes de la ou des applications qui hébergent actuellement le caractère suivent la commande masquer, précédée d’un séparateur.</span><span class="sxs-lookup"><span data-stu-id="f304e-125">The commands for the application(s) currently hosting the character follow the Hide command, preceded by a separator.</span></span> <span data-ttu-id="f304e-126">Les noms des autres applications qui utilisent le caractère apparaissent, également précédés d’un séparateur.</span><span class="sxs-lookup"><span data-stu-id="f304e-126">Then the names of other applications using the character appear, also preceded by a separator.</span></span>

 

 




