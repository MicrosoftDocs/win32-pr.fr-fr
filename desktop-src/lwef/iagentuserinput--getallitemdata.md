---
title: IAgentUserInput GetAllItemData
description: IAgentUserInput GetAllItemData
ms.assetid: d1857b28-c745-4ed2-b49e-774f247e7348
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced6a618d4fbbc093bf54c19fc393b7e195f2069
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104461958"
---
# <a name="iagentuserinputgetallitemdata"></a><span data-ttu-id="5f56b-103">IAgentUserInput::GetAllItemData</span><span class="sxs-lookup"><span data-stu-id="5f56b-103">IAgentUserInput::GetAllItemData</span></span>

<span data-ttu-id="5f56b-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5f56b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

<span data-ttu-id="5f56b-105">Récupère les données pour toutes les autres [**commandes**](command-event.md) passées à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56b-105">Retrieves the data for all [**Command**](command-event.md) alternatives passed to an [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

-   <span data-ttu-id="5f56b-106">Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.</span><span class="sxs-lookup"><span data-stu-id="5f56b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5f56b-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span><span class="sxs-lookup"><span data-stu-id="5f56b-107"><span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*</span></span>
</dt> <dd>

<span data-ttu-id="5f56b-108">Adresse d’une variable qui reçoit les ID des [**commandes**](command-event.md) passées au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56b-108">Address of a variable that receives the IDs of [**Commands**](command-event.md) passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="5f56b-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span><span class="sxs-lookup"><span data-stu-id="5f56b-109"><span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*</span></span>
</dt> <dd>

<span data-ttu-id="5f56b-110">Adresse d’une variable qui reçoit les scores de confiance pour les alternatives de [**commande**](command-event.md) transmises au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56b-110">Address of a variable that receives the confidence scores for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> <dt>

<span data-ttu-id="5f56b-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span><span class="sxs-lookup"><span data-stu-id="5f56b-111"><span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*</span></span>
</dt> <dd>

<span data-ttu-id="5f56b-112">Adresse d’une variable qui reçoit le texte vocal pour les [**commandes**](command-event.md) alternatives transmises au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56b-112">Address of a variable that receives the voice text for [**Command**](command-event.md) alternatives passed to the [**IAgentNotifySink::Command**](iagentnotifysink--command.md) callback.</span></span>

</dd> </dl>

<span data-ttu-id="5f56b-113">Si l’entrée vocale déclenche [**IAgentNotifySink :: Command**](iagentnotifysink--command.md), le serveur renvoie la meilleure correspondance, la deuxième-meilleure correspondance et la troisième, si elles sont fournies par le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="5f56b-113">If speech input triggers [**IAgentNotifySink::Command**](iagentnotifysink--command.md), the server returns the best match, the second-best match, and the third-best match, if these are provided by the speech engine.</span></span> <span data-ttu-id="5f56b-114">Il fournit les scores de confiance relatifs, dans la plage comprise entre-100 et 100, et le texte réel « entendu » par le moteur de reconnaissance vocale.</span><span class="sxs-lookup"><span data-stu-id="5f56b-114">It provides the relative confidence scores, in the range of -100 to 100, and actual text "heard" by the speech engine.</span></span> <span data-ttu-id="5f56b-115">Si la meilleure correspondance était une commande fournie par le serveur, le serveur envoie un ID NULL, mais envoie toujours un score de confiance et le texte [**vocal**](voice-property.md) .</span><span class="sxs-lookup"><span data-stu-id="5f56b-115">If the best match was a server-supplied command, the server sends a NULL ID, but still sends a confidence score and the [**Voice**](voice-property.md) text.</span></span>

<span data-ttu-id="5f56b-116">Si l’entrée vocale n’est pas la source de l’événement ; par exemple, si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur Microsoft Agent renvoie l’ID de la [**commande**](command-event.md) sélectionnée, avec un score de confiance de 100 et un texte vocal comme null.</span><span class="sxs-lookup"><span data-stu-id="5f56b-116">If speech input was not the source for the event; for example, if the user selected the command from the character's pop-up menu, the Microsoft Agent server returns the ID of the [**Command**](command-event.md) selected, with a confidence score of 100 and voice text as NULL.</span></span> <span data-ttu-id="5f56b-117">Les autres alternatives retournent comme NULL avec des scores de confiance de zéro (0) et un texte vocal comme NULL.</span><span class="sxs-lookup"><span data-stu-id="5f56b-117">The other alternatives return as NULL with confidence scores of zero (0) and voice text as NULL.</span></span>

> [!Note]  
> <span data-ttu-id="5f56b-118">Tous les moteurs de reconnaissance vocale ne peuvent pas retourner toutes les valeurs de tous les paramètres de cet événement.</span><span class="sxs-lookup"><span data-stu-id="5f56b-118">Not all speech recognition engines may return all the values for all the parameters of this event.</span></span> <span data-ttu-id="5f56b-119">Contactez votre fournisseur de moteur pour déterminer si le moteur prend en charge l’interface de l’API Microsoft Speech pour retourner des alternatives et des scores de confiance.</span><span class="sxs-lookup"><span data-stu-id="5f56b-119">Check with your engine vendor to determine whether the engine supports the Microsoft Speech API interface for returning alternatives and confidence scores.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5f56b-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5f56b-120">See Also</span></span>

<span data-ttu-id="5f56b-121">[**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput :: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md)</span><span class="sxs-lookup"><span data-stu-id="5f56b-121">[**IAgentUserInput::GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput::GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput::GetItemID**](iagentuserinput--getitemid.md)</span></span>


 

 




