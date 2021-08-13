---
title: Propriété Active
description: Propriété Active
ms.assetid: 76ada073-782a-4355-b4e8-42dd84d0139b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac75a83724c793f2a7aba01718d57e47b25a0dd6b467ca7797ad6f0e4ced018e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753168"
---
# <a name="active-property"></a>Propriété Active

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne une valeur indiquant si votre application est le client actif du caractère et si le caractère est le plus haut.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***caractères * * * * ("**_CharacterID_*_")._ *  \[  =  *État* actif\]



| Partie    | Description                                                                                                                                                                                                |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *state* | Expression entière spécifiant l’état de votre application cliente. 0 n’est pas le client actif.<br/> 1 le client actif. <br/> 2 le client d’entrée-actif. (Le caractère le plus élevé.)<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque plusieurs applications clientes partagent le même caractère, le client actif du caractère reçoit l’entrée de la souris (par exemple, les événements [**Click**](click-event.md) ou [DragStart](dragstart-event.md) du contrôle Microsoft Agent). De même, lorsque plusieurs caractères sont affichés, le client actif du caractère le plus haut (également appelé client d’entrée-actif) reçoit des événements de commande.

Vous pouvez utiliser la méthode [**Activate**](activate-method.md)pour définir si votre application est le client actif du personnage ou pour faire de votre application le client actif d’entrée (ce qui rend également le caractère le plus haut).

## <a name="see-also"></a>Voir aussi

[Activate * *, méthode * *](activate-method.md)


 

 





