---
title: Événement IdleComplete
description: Événement IdleComplete
ms.assetid: 1d684f75-f23e-4ed8-a60a-5e6792332103
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01782825dc880dc4d214a8d0e682d69a9f842e22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028471"
---
# <a name="idlecomplete-event"></a>Événement IdleComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le serveur met fin à l’état de **ralenti** d’un caractère.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent * * * \_ IdleComplete* *  **(ByVal** *CharacterID * * *)**



| Partie          | Description                                         |
|---------------|-----------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère ralenti sous la forme d’une chaîne. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Le serveur envoie cet événement à tous les clients du caractère.

### <a name="see-also"></a>Voir aussi

[**Événement IdleStart**](idlestart-event.md)


 

 




