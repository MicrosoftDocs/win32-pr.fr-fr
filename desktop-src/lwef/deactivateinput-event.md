---
title: Événement DeactivateInput
description: Événement DeactivateInput
ms.assetid: 59747932-82be-45d5-8465-73798904e8a7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b2fe1ff13b599fe5fbcf2dac22e548a0432f415
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127012382"
---
# <a name="deactivateinput-event"></a>Événement DeactivateInput

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsqu’un client devient non-actif.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent * * * \_ DeactivateInput* *  **(ByVal** *CharacterID * * *)**



| Partie          | Description                                                                    |
|---------------|--------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère qui rend le client devenu non actif. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Un client de non-entrée-actif ne reçoit plus d’événements de souris ou de parole du serveur (à moins qu’il ne soit de nouveau en entrée active). Le serveur envoie cet événement uniquement au client qui devient non-actif.

Cet événement se produit lorsque votre application cliente est en entrée-active et que l’utilisateur choisit la légende d’un autre client dans le menu contextuel d’un caractère ou dans la fenêtre commandes vocales ou si vous appelez la méthode [**Activate**](activate-method.md) et définissez le paramètre **State** sur 0. Cela peut également se produire lorsque l’utilisateur sélectionne le nom d’un autre caractère en cliquant ou en parlant. Vous recevez également cet événement lorsque votre caractère est masqué ou qu’un autre caractère devient visible.

### <a name="see-also"></a>Voir aussi

[**Événement ActivateInput**](activateinput-event.md)


 

 




