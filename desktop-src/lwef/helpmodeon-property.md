---
title: Propriété HelpModeOn
description: Propriété HelpModeOn
ms.assetid: 4a9b5fd3-12e2-489b-8ce0-9b66b01f517a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43662469c6461e92186a92daddb505b851f8740a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673482"
---
# <a name="helpmodeon-property"></a>Propriété HelpModeOn

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit une valeur indiquant si le mode d’aide contextuelle est activé pour le caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent. ***Caractères («*** CharacterID * * * »). HelpModeOn* *  \[  =  *booléen*\]



| Partie      | Description                                                                                                                                                       |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *boolean* | Expression booléenne spécifiant si le mode d’aide contextuelle est activé. **True** Le mode d’aide est activé. <br/> Le mode d’aide **false** (par défaut) est désactivé.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Lorsque vous affectez la valeur **true** à cette propriété, le pointeur de la souris se transforme en image d’aide contextuelle lorsqu’il est déplacé sur le caractère ou sur le menu contextuel du caractère. Quand l’utilisateur clique ou fait glisser le caractère ou clique sur un élément dans le menu contextuel du caractère, le serveur déclenche l’événement [**HelpComplete**](helpcomplete-event.md) et quitte le mode d’aide.

Dans le mode d’aide, le serveur n’envoie pas les événements [**Click**](click-event.md), [**DragStart**](dragstart-event.md), [**DragComplete**](dragcomplete-event.md)et [**Command**](command-event.md) , sauf si vous affectez la valeur **true** à la propriété [**AutoPopupMenu**](autopopupmenu-property.md) . Dans ce cas, le serveur enverra l’événement **Click** (ne quitte pas le mode d’aide), mais uniquement pour le bouton droit de la souris pour vous permettre d’afficher le menu contextuel.

Cette propriété s’applique uniquement à l’utilisation du caractère par votre application cliente ; le paramètre n’affecte pas les autres clients du caractère ou d’autres caractères de votre application cliente.

## <a name="see-also"></a>Voir aussi

[**Événement HelpComplete**](helpcomplete-event.md)


 

 





