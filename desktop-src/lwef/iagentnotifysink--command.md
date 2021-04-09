---
title: Commande IAgentNotifySink
description: Commande IAgentNotifySink
ms.assetid: d54fb2e8-27d6-47a4-8a1e-5419a94ea26d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9690d2914db9d284cd4ba4b826905d3169b83f2c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "103940927"
---
# <a name="iagentnotifysinkcommand"></a><span data-ttu-id="37037-103">IAgentNotifySink :: commande</span><span class="sxs-lookup"><span data-stu-id="37037-103">IAgentNotifySink::Command</span></span>

<span data-ttu-id="37037-104">\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="37037-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

<span data-ttu-id="37037-105">Avertit une application cliente qu’une [**commande**](/windows/desktop/lwef/the-command-object) a été sélectionnée par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="37037-105">Notifies a client application that a [**Command**](/windows/desktop/lwef/the-command-object) was selected by the user.</span></span>

-   <span data-ttu-id="37037-106">Pas de valeur de retour.</span><span class="sxs-lookup"><span data-stu-id="37037-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="37037-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="37037-107"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="37037-108">Identificateur de la meilleure commande de correspondance.</span><span class="sxs-lookup"><span data-stu-id="37037-108">Identifier of the best match command alternative.</span></span>

</dd> <dt>

<span data-ttu-id="37037-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span><span class="sxs-lookup"><span data-stu-id="37037-109"><span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*</span></span>
</dt> <dd>

<span data-ttu-id="37037-110">Adresse de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pour l’objet [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="37037-110">Address of the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface for the [**IAgentUserInput**](iagentuserinput.md) object.</span></span>

</dd> </dl>

<span data-ttu-id="37037-111">Utilisez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer l’interface [**IAgentUserInput**](iagentuserinput.md) .</span><span class="sxs-lookup"><span data-stu-id="37037-111">Use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to retrieve the [**IAgentUserInput**](iagentuserinput.md) interface.</span></span>

<span data-ttu-id="37037-112">Le serveur notifie le client d’entrée-actif lorsque l’utilisateur choisit une commande par voix ou en sélectionnant une commande dans le menu contextuel du caractère.</span><span class="sxs-lookup"><span data-stu-id="37037-112">The server notifies the input-active client when the user chooses a command by voice or by selecting a command from the character's pop-up menu.</span></span> <span data-ttu-id="37037-113">L’événement se produit même lorsque l’utilisateur sélectionne l’une des commandes du serveur.</span><span class="sxs-lookup"><span data-stu-id="37037-113">The event occurs even when the user selects one of the server's commands.</span></span> <span data-ttu-id="37037-114">Dans ce cas, le serveur retourne un ID de commande null, le score de confiance et le texte vocal renvoyé par le moteur de reconnaissance vocale pour cette entrée.</span><span class="sxs-lookup"><span data-stu-id="37037-114">In this case the server returns a null command ID, the confidence score, and the voice text returned by the speech engine for that entry.</span></span>

## <a name="see-also"></a><span data-ttu-id="37037-115">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="37037-115">See Also</span></span>

[<span data-ttu-id="37037-116">**IAgentUserInput**</span><span class="sxs-lookup"><span data-stu-id="37037-116">**IAgentUserInput**</span></span>](iagentuserinput.md)


 

 