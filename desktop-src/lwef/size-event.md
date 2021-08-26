---
title: Événement de taille
description: Événement de taille
ms.assetid: 06089f84-8e75-475f-a492-536c83fa6730
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 146763c649ab22c59a8367e3135ee0ea277c8ae4c8e4bc58588cd70c0b5ec1c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961019"
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

### <a name="remarks"></a>Remarques

Cet événement se produit lorsqu’une application modifie la taille d’un caractère. Cet événement est envoyé uniquement aux clients du caractère (applications qui ont chargé le caractère).

### <a name="see-also"></a>Voir aussi

[**Déplacer l’événement**](move-event.md)


 

 




