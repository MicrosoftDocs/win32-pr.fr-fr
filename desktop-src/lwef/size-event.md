---
title: Événement de taille
description: Événement de taille
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d9a896d2dcbf8b925c0ca13fa429f6dfd95bc21
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839866"
---
# <a name="size-event"></a>Événement de taille

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque la taille d’un caractère change.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

Taille du **sous** *-agent* \_ **(ByVal** *CharacterID*, *largeur* **ByVal** , **ByVal** *hauteur*)



| Partie          | Description                                                         |
|---------------|---------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère qui a été déplacé.                         |
| *Width*       | Retourne la nouvelle largeur de la trame de caractère (en pixels) sous la forme d’un entier.  |
| *Height*      | Retourne la nouvelle hauteur de la trame de caractère (en pixels) sous la forme d’un entier. |



 

</dd> </dl>

### <a name="remarks"></a>Notes

Cet événement se produit lorsqu’une application modifie la taille d’un caractère. Cet événement est envoyé uniquement aux clients du caractère (applications qui ont chargé le caractère).

### <a name="see-also"></a>Voir aussi

[**Déplacer l’événement**](move-event.md)


 

 




