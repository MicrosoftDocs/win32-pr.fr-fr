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
# <a name="iagentuserinputgetallitemdata"></a>IAgentUserInput::GetAllItemData

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

``` syntax
HRESULT GetAllItemData(
   VARIANT * pdwItemIndices,  // address of variable for alternative IDs
   VARIANT * plConfidences,   // address of variable for confidence scores
   VARIANT * pbszText         // address of variable for voice text
);
```

Récupère les données pour toutes les autres [**commandes**](command-event.md) passées à un rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

-   Retourne \_ la valeur S OK pour indiquer que l’opération a réussi.

<dl> <dt>

<span id="pdwItemIndices"></span><span id="pdwitemindices"></span><span id="PDWITEMINDICES"></span>*pdwItemIndices*
</dt> <dd>

Adresse d’une variable qui reçoit les ID des [**commandes**](command-event.md) passées au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="plConfidences"></span><span id="plconfidences"></span><span id="PLCONFIDENCES"></span>*plConfidences*
</dt> <dd>

Adresse d’une variable qui reçoit les scores de confiance pour les alternatives de [**commande**](command-event.md) transmises au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> <dt>

<span id="pbszText"></span><span id="pbsztext"></span><span id="PBSZTEXT"></span>*pbszText*
</dt> <dd>

Adresse d’une variable qui reçoit le texte vocal pour les [**commandes**](command-event.md) alternatives transmises au rappel [**IAgentNotifySink :: Command**](iagentnotifysink--command.md) .

</dd> </dl>

Si l’entrée vocale déclenche [**IAgentNotifySink :: Command**](iagentnotifysink--command.md), le serveur renvoie la meilleure correspondance, la deuxième-meilleure correspondance et la troisième, si elles sont fournies par le moteur de reconnaissance vocale. Il fournit les scores de confiance relatifs, dans la plage comprise entre-100 et 100, et le texte réel « entendu » par le moteur de reconnaissance vocale. Si la meilleure correspondance était une commande fournie par le serveur, le serveur envoie un ID NULL, mais envoie toujours un score de confiance et le texte [**vocal**](voice-property.md) .

Si l’entrée vocale n’est pas la source de l’événement ; par exemple, si l’utilisateur a sélectionné la commande dans le menu contextuel du caractère, le serveur Microsoft Agent renvoie l’ID de la [**commande**](command-event.md) sélectionnée, avec un score de confiance de 100 et un texte vocal comme null. Les autres alternatives retournent comme NULL avec des scores de confiance de zéro (0) et un texte vocal comme NULL.

> [!Note]  
> Tous les moteurs de reconnaissance vocale ne peuvent pas retourner toutes les valeurs de tous les paramètres de cet événement. Contactez votre fournisseur de moteur pour déterminer si le moteur prend en charge l’interface de l’API Microsoft Speech pour retourner des alternatives et des scores de confiance.

 

## <a name="see-also"></a>Voir aussi

[**IAgentUserInput :: GetItemConfidence**](iagentuserinput--getitemconfidence.md), [**IAgentUserInput :: GetItemText**](iagentuserinput--getitemtext.md), [**IAgentUserInput :: getItemID**](iagentuserinput--getitemid.md)


 

 




