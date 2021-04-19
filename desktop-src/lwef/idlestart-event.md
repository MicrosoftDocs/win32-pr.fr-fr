---
title: Événement IdleStart
description: Événement IdleStart
ms.assetid: 3d97c26b-b88a-42e3-9072-0bc65510efc2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706aafc13cb1639484539e3d08b305df217ecec8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513667"
---
# <a name="idlestart-event"></a>Événement IdleStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le serveur définit un caractère à l’état **ralenti** .

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent * * * \_ IdleStart* *  **(ByVal** *CharacterID * * *)**



| Partie          | Description                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère ralenti sous la forme d’une chaîne. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Le serveur envoie cet événement à tous les clients du caractère.

### <a name="see-also"></a>Voir aussi

[**Événement IdleComplete**](idlecomplete-event.md)


 

 




