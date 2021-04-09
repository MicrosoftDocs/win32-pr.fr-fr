---
description: Un gestionnaire d’interface utilisateur externe peut retourner n’importe quel nombre de valeurs à Windows Installer en fonction du type de bouton fourni dans le paramètre de type de message que le programme d’installation transmet au gestionnaire.
ms.assetid: a918082d-709d-4b4f-ae3b-5f16ed0ca910
title: Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b466f6bc3cc034551a01bd2b87caa7292824e0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103754204"
---
# <a name="returning-values-from-an-external-user-interface-handler"></a><span data-ttu-id="48379-103">Retour de valeurs à partir d’un gestionnaire d’interface utilisateur externe</span><span class="sxs-lookup"><span data-stu-id="48379-103">Returning Values from an External User Interface Handler</span></span>

<span data-ttu-id="48379-104">Un gestionnaire d’interface utilisateur externe peut retourner n’importe quel nombre de valeurs à Windows Installer en fonction du type de bouton fourni dans le paramètre de type de message que le programme d’installation transmet au gestionnaire.</span><span class="sxs-lookup"><span data-stu-id="48379-104">An external user interface (UI) handler can return any number of values to Windows Installer depending on the button type provided in the message type parameter the installer passes to the handler.</span></span>

<span data-ttu-id="48379-105">Le gestionnaire d’interface utilisateur externe peut retourner les valeurs 1 et 0 à tout moment, car celles-ci ne sont pas liées aux types de boutons.</span><span class="sxs-lookup"><span data-stu-id="48379-105">The external UI handler can return the values –1 and 0 at any time because these are not related to the button types.</span></span> <span data-ttu-id="48379-106">Une valeur de retour de-1 indique qu’une erreur interne s’est produite dans le gestionnaire d’interface utilisateur externe.</span><span class="sxs-lookup"><span data-stu-id="48379-106">A return value of –1 indicates that an internal error occurred in the external UI handler.</span></span> <span data-ttu-id="48379-107">Une valeur de retour de 0 indique que le gestionnaire de l’interface utilisateur externe n’a pas géré le message du programme d’installation et que le programme d’installation doit gérer le message à la place.</span><span class="sxs-lookup"><span data-stu-id="48379-107">A return value of 0 indicates that the external UI handler has not handled the installer message and the installer must handle the message instead.</span></span>

<span data-ttu-id="48379-108">Pour les messages qui n’incluent pas de type de bouton, tels que INSTALLMESSAGE \_ ACTIONDATA et INSTALLMESSAGE \_ Progress, le retour de IDCANCEL annule l’installation.</span><span class="sxs-lookup"><span data-stu-id="48379-108">For messages that do not include a button type, such as INSTALLMESSAGE\_ACTIONDATA and INSTALLMESSAGE\_PROGRESS, returning IDCANCEL cancels the installation.</span></span> <span data-ttu-id="48379-109">Le renvoi de IDOK notifie le programme d’installation que le message a été géré par le gestionnaire d’interface utilisateur externe.</span><span class="sxs-lookup"><span data-stu-id="48379-109">Returning IDOK notifies the installer that the message was handled by the external UI handler.</span></span>

<span data-ttu-id="48379-110">Les valeurs de retour restantes, comme décrit ci-dessous, sont directement liées aux types de bouton inclus avec le type de message.</span><span class="sxs-lookup"><span data-stu-id="48379-110">The remaining return values, as described below, are directly related to the button types that are included with the message type.</span></span>



| <span data-ttu-id="48379-111">Valeur de retour de l’interface utilisateur externe</span><span class="sxs-lookup"><span data-stu-id="48379-111">External UI return value</span></span> | <span data-ttu-id="48379-112">Signification</span><span class="sxs-lookup"><span data-stu-id="48379-112">Meaning</span></span>                                                                                                |
|--------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48379-113">IDOK</span><span class="sxs-lookup"><span data-stu-id="48379-113">IDOK</span></span>                     | <span data-ttu-id="48379-114">L’utilisateur a cliqué sur le bouton **OK** .</span><span class="sxs-lookup"><span data-stu-id="48379-114">The **OK** button was pressed by the user.</span></span> <span data-ttu-id="48379-115">Les informations du message ont été comprises.</span><span class="sxs-lookup"><span data-stu-id="48379-115">The message information was understood.</span></span>                     |
| <span data-ttu-id="48379-116">IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="48379-116">IDCANCEL</span></span>                 | <span data-ttu-id="48379-117">Le bouton **Annuler** a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="48379-117">The **CANCEL** button was pressed.</span></span> <span data-ttu-id="48379-118">Annulez l’installation.</span><span class="sxs-lookup"><span data-stu-id="48379-118">Cancel the installation.</span></span>                                            |
| <span data-ttu-id="48379-119">IDABORT</span><span class="sxs-lookup"><span data-stu-id="48379-119">IDABORT</span></span>                  | <span data-ttu-id="48379-120">Le bouton **abandonner** a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="48379-120">The **ABORT** button was pressed.</span></span> <span data-ttu-id="48379-121">Abandonner l’installation.</span><span class="sxs-lookup"><span data-stu-id="48379-121">Abort the installation.</span></span>                                              |
| <span data-ttu-id="48379-122">IDRETRY</span><span class="sxs-lookup"><span data-stu-id="48379-122">IDRETRY</span></span>                  | <span data-ttu-id="48379-123">Le bouton **Réessayer** a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="48379-123">The **RETRY** button was pressed.</span></span> <span data-ttu-id="48379-124">Recommencez l’opération.</span><span class="sxs-lookup"><span data-stu-id="48379-124">Try the action again.</span></span>                                                |
| <span data-ttu-id="48379-125">IDIGNORE</span><span class="sxs-lookup"><span data-stu-id="48379-125">IDIGNORE</span></span>                 | <span data-ttu-id="48379-126">L’utilisateur a cliqué sur le bouton **Ignorer** .</span><span class="sxs-lookup"><span data-stu-id="48379-126">The **IGNORE** button was pressed.</span></span> <span data-ttu-id="48379-127">Ignorez l’erreur et continuez.</span><span class="sxs-lookup"><span data-stu-id="48379-127">Ignore the error and continue.</span></span>                                      |
| <span data-ttu-id="48379-128">IDYES</span><span class="sxs-lookup"><span data-stu-id="48379-128">IDYES</span></span>                    | <span data-ttu-id="48379-129">Le bouton **Oui** a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="48379-129">The **YES** button was pressed.</span></span> <span data-ttu-id="48379-130">La réponse affirmative, poursuivez avec la séquence d’événements actuelle.</span><span class="sxs-lookup"><span data-stu-id="48379-130">The affirmative response, continue with current sequence of events..</span></span>   |
| <span data-ttu-id="48379-131">IDNO</span><span class="sxs-lookup"><span data-stu-id="48379-131">IDNO</span></span>                     | <span data-ttu-id="48379-132">Le bouton **non** a été enfoncé.</span><span class="sxs-lookup"><span data-stu-id="48379-132">The **NO** button was pressed.</span></span> <span data-ttu-id="48379-133">La réponse négative ne continue pas avec la séquence d’événements en cours.</span><span class="sxs-lookup"><span data-stu-id="48379-133">The negative response, do not continue with current sequence of events.</span></span> |



 

<span data-ttu-id="48379-134">Par exemple, si le gestionnaire d’interface utilisateur externe reçoit un message avec l' \_ indicateur de styles de la boîte de message Mo ABORTRETRYIGNORE, le gestionnaire d’interface utilisateur externe peut retourner l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="48379-134">For example, if the external UI handler is sent a message with the MB\_ABORTRETRYIGNORE message box styles flag, the external UI handler can return one of the following values:</span></span>

-   <span data-ttu-id="48379-135">– 1 (erreur dans le gestionnaire d’interface utilisateur externe)</span><span class="sxs-lookup"><span data-stu-id="48379-135">–1 (error in external UI handler)</span></span>
-   <span data-ttu-id="48379-136">0 (aucune action effectuée dans le gestionnaire d’interface utilisateur externe, laissez Windows Installer le gérer)</span><span class="sxs-lookup"><span data-stu-id="48379-136">0 (no action taken in external UI handler, let Windows Installer handle it)</span></span>
-   <span data-ttu-id="48379-137">IDABORT (bouton **abandonner** enfoncé)</span><span class="sxs-lookup"><span data-stu-id="48379-137">IDABORT (**ABORT** button pressed)</span></span>
-   <span data-ttu-id="48379-138">IDRETRY (bouton **Réessayer** enfoncé)</span><span class="sxs-lookup"><span data-stu-id="48379-138">IDRETRY (**RETRY** button pressed)</span></span>
-   <span data-ttu-id="48379-139">IDIGNORE (bouton **Ignorer** enfoncé)</span><span class="sxs-lookup"><span data-stu-id="48379-139">IDIGNORE (**IGNORE** button pressed)</span></span>

 

 



