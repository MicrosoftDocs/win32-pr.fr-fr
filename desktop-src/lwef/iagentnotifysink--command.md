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
# <a name="iagentnotifysinkcommand"></a>IAgentNotifySink :: commande

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT Command(
   long dwCommandID,         // Command ID of the best match
   IUnknown * punkUserInput  // address of IAgentUserInput object 
);                          
```

Avertit une application cliente qu’une [**commande**](/windows/desktop/lwef/the-command-object) a été sélectionnée par l’utilisateur.

-   Pas de valeur de retour.

<dl> <dt>

<span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*
</dt> <dd>

Identificateur de la meilleure commande de correspondance.

</dd> <dt>

<span id="punkUserInput"></span><span id="punkuserinput"></span><span id="PUNKUSERINPUT"></span>*punkUserInput*
</dt> <dd>

Adresse de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) pour l’objet [**IAgentUserInput**](iagentuserinput.md) .

</dd> </dl>

Utilisez [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour récupérer l’interface [**IAgentUserInput**](iagentuserinput.md) .

Le serveur notifie le client d’entrée-actif lorsque l’utilisateur choisit une commande par voix ou en sélectionnant une commande dans le menu contextuel du caractère. L’événement se produit même lorsque l’utilisateur sélectionne l’une des commandes du serveur. Dans ce cas, le serveur retourne un ID de commande null, le score de confiance et le texte vocal renvoyé par le moteur de reconnaissance vocale pour cette entrée.

## <a name="see-also"></a>Voir aussi

[**IAgentUserInput**](iagentuserinput.md)


 

 