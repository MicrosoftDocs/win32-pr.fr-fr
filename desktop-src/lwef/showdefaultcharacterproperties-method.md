---
title: Méthode ShowDefaultCharacterProperties
description: Méthode ShowDefaultCharacterProperties
ms.assetid: a3b109c0-5701-4a72-baae-bcbb97b025a3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f055b2ca0f00e0a13c24ec95dc82509ae9c45b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672809"
---
# <a name="showdefaultcharacterproperties-method"></a>Méthode ShowDefaultCharacterProperties

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Affiche les propriétés du caractère par défaut.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent * * *. ShowDefaultCharacterProperties* *  \[ *X* , *Y*\]



| Partie | Description                                                                                                                                                |
|------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *X*  | Optionnel. Valeur entière de type short qui indique la coordonnée d’écran horizontale (*X* ) pour afficher la fenêtre. Cette coordonnée doit être spécifiée en pixels. |
| *O*  | Optionnel. Valeur entière de type short qui indique la coordonnée d’écran verticale (*Y*) pour afficher la fenêtre. Cette coordonnée doit être spécifiée en pixels.    |



 

</dd> </dl>

## <a name="remarks"></a>Notes

L’appel de cette méthode affiche la fenêtre de propriétés de caractères par défaut (et non la feuille de propriétés de l’agent Microsoft). Si vous ne spécifiez pas les coordonnées X et Y, la fenêtre s’affiche au dernier emplacement affiché.

## <a name="see-also"></a>Voir aussi

[**Événement DefaultCharacterChange**](defaultcharacterchange-event.md)


 

 




