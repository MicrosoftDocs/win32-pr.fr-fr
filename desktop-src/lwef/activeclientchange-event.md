---
title: Événement ActiveClientChange
description: Événement ActiveClientChange
ms.assetid: 617b40e6-cafb-463e-8b36-2a12c468d3ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8137edd559d934fd1a478350cd1185885c7dc148
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196769"
---
# <a name="activeclientchange-event"></a>Événement ActiveClientChange

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le client actif du caractère change.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent.* ActiveClientChange (ByVal *CharacterID*, ByVal *actif* **)**



| Partie          | Description                                                                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère pour lequel l’événement s’est produit.                                                                                                                                                                                                      |
| *Actif*      | Valeur booléenne qui indique si le client est devenu actif ou non actif. **True** L’application cliente est devenue le client actif du caractère. <br/> **Valeur false** L’application cliente n’est plus le client actif du caractère.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent). De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements de [commande](command-event.md) .

Lorsque le client actif d’un caractère change, cet événement transmet l’ID de ce caractère et la **valeur true** si votre application est devenue le client actif du caractère ou **false** si elle n’est plus le client actif du caractère.

Une application cliente peut recevoir cet événement lorsque l’utilisateur sélectionne l’entrée d’une application cliente dans le menu contextuel d’un caractère ou par une commande vocale, lorsque l’application cliente modifie son état actif ou lorsqu’une autre application cliente quitte sa connexion à l’agent. Agent envoie cet événement uniquement aux applications clientes qui sont directement affectées ; qu’il s’agisse du client actif ou d’un arrêt du client actif.

### <a name="see-also"></a>Voir aussi

* * * * [ActivateInput * * Event * *](activateinput-event.md)* [* *](active-property.md)* * * * * * * * * * * * * * * * * * * * * * * * * * [* * *](deactivateinput-event.md)* * * * * * * * * * * * * * * * * * * * * [* *](activate-method.md)


 

 





