---
title: Événement ActivateInput
description: Événement ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e0b4fdf83256d58dd247dee85b639f5499f013e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029729"
---
# <a name="activateinput-event"></a><span data-ttu-id="73661-103">Événement ActivateInput</span><span class="sxs-lookup"><span data-stu-id="73661-103">ActivateInput Event</span></span>

<span data-ttu-id="73661-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="73661-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="73661-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**</span><span class="sxs-lookup"><span data-stu-id="73661-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="73661-106">Se produit lorsqu’un client devient en entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="73661-106">Occurs when a client becomes input-active.</span></span>

</dd> <dt>

<span data-ttu-id="73661-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**</span><span class="sxs-lookup"><span data-stu-id="73661-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="73661-108">**Sub** *agent* \_ ActivateInput **(ByVal** *CharacterID \* \* *)**</span><span class="sxs-lookup"><span data-stu-id="73661-108">**Sub** *agent*\_ActivateInput **(ByVal** *CharacterID\*\*\*)*\*</span></span>



| <span data-ttu-id="73661-109">Partie</span><span class="sxs-lookup"><span data-stu-id="73661-109">Part</span></span>          | <span data-ttu-id="73661-110">Description</span><span class="sxs-lookup"><span data-stu-id="73661-110">Description</span></span>                                                                    |
|---------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="73661-111">*CharacterID*</span><span class="sxs-lookup"><span data-stu-id="73661-111">*CharacterID*</span></span> | <span data-ttu-id="73661-112">Retourne l’ID du caractère par le biais duquel le client devient Input-active.</span><span class="sxs-lookup"><span data-stu-id="73661-112">Returns the ID of the character through which the client becomes input-active.</span></span> |



 

</dd> </dl>

### <a name="remarks"></a><span data-ttu-id="73661-113">Notes</span><span class="sxs-lookup"><span data-stu-id="73661-113">Remarks</span></span>

<span data-ttu-id="73661-114">Le client d’entrée-actif reçoit des événements d’entrée de la souris et de la parole fournis par le serveur.</span><span class="sxs-lookup"><span data-stu-id="73661-114">The input-active client receives mouse and speech input events supplied by the server.</span></span> <span data-ttu-id="73661-115">Le serveur envoie cet événement uniquement au client qui devient en entrée-actif.</span><span class="sxs-lookup"><span data-stu-id="73661-115">The server sends this event only to the client that becomes input-active.</span></span>

<span data-ttu-id="73661-116">Cet événement peut se produire lorsque l’utilisateur bascule vers votre objet de [commande](the-command-object.md) , par exemple, en choisissant l’entrée de l’objet de commande dans la fenêtre commandes ou dans le menu contextuel d’un caractère.</span><span class="sxs-lookup"><span data-stu-id="73661-116">This event can occur when the user switches to your [Command](the-command-object.md) object, for example, by choosing your Command object entry in the Commands Window or in the pop-up menu for a character.</span></span> <span data-ttu-id="73661-117">Cela peut également se produire lorsque l’utilisateur sélectionne un caractère (en cliquant ou parlant son nom), lorsqu’un caractère devient visible et lorsque le caractère d’une autre application cliente devient masqué.</span><span class="sxs-lookup"><span data-stu-id="73661-117">It can also occur when the user selects a character (by clicking or speaking its name), when a character becomes visible, and when the character of another client application becomes hidden.</span></span> <span data-ttu-id="73661-118">Vous pouvez également appeler la [méthode Activate](activate-method.md) (avec un **État** défini sur 2) pour rendre explicitement le caractère le plus haut, ce qui a pour effet que votre application cliente devient une entrée-active et déclenche cet événement.</span><span class="sxs-lookup"><span data-stu-id="73661-118">You can also call the [Activate Method](activate-method.md) (with **State** set to 2) to explicitly make the character topmost, which results in your client application becoming input-active and triggers this event.</span></span> <span data-ttu-id="73661-119">Toutefois, cet événement ne se produit pas si vous utilisez la méthode Activate uniquement pour spécifier si votre client est le client actif du caractère.</span><span class="sxs-lookup"><span data-stu-id="73661-119">However, this event does not occur if you use the Activate Method method only to specify whether your client is the active client of the character.</span></span>

### <a name="see-also"></a><span data-ttu-id="73661-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="73661-120">See Also</span></span>

<span data-ttu-id="73661-121">[Événement **DeactivateInput**](deactivateinput-event.md), [méthode **Activate**](activate-method.md)</span><span class="sxs-lookup"><span data-stu-id="73661-121">[**DeactivateInput** event](deactivateinput-event.md), [**Activate** method](activate-method.md)</span></span>


 

 




