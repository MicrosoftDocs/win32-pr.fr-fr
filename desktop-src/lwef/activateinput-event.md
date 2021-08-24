---
title: Événement ActivateInput
description: Événement ActivateInput
ms.assetid: bc395750-5da0-4379-8eca-3195e936052c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db21d605a014002063a7c5aa42554a06adb1ed35296242944de789daeb3155c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610679"
---
# <a name="activateinput-event"></a>Événement ActivateInput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un client devient en entrée-actif.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent* \_ ActivateInput **(ByVal** *CharacterID * * *)**



| Partie          | Description                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère par le biais duquel le client devient Input-active. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Le client d’entrée-actif reçoit des événements d’entrée de la souris et de la parole fournis par le serveur. Le serveur envoie cet événement uniquement au client qui devient en entrée-actif.

Cet événement peut se produire lorsque l’utilisateur bascule vers votre objet de [commande](the-command-object.md) , par exemple, en choisissant l’entrée de l’objet de commande dans la fenêtre commandes ou dans le menu contextuel d’un caractère. Cela peut également se produire lorsque l’utilisateur sélectionne un caractère (en cliquant ou parlant son nom), lorsqu’un caractère devient visible et lorsque le caractère d’une autre application cliente devient masqué. Vous pouvez également appeler la [méthode Activate](activate-method.md) (avec un **État** défini sur 2) pour rendre explicitement le caractère le plus haut, ce qui a pour effet que votre application cliente devient une entrée-active et déclenche cet événement. Toutefois, cet événement ne se produit pas si vous utilisez la méthode Activate uniquement pour spécifier si votre client est le client actif du caractère.

### <a name="see-also"></a>Voir aussi

[Événement **DeactivateInput**](deactivateinput-event.md), [méthode **Activate**](activate-method.md)


 

 




