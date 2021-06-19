---
title: Width, propriété (objet Characters)
description: En savoir plus sur la propriété Width de l’objet Characters, qui retourne ou définit la largeur du cadre pour le caractère spécifié.
ms.assetid: ebada4cc-dbe6-4540-be1f-1f61e176765b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e17f11412774fcf34e887a2f00479ab7d96369de
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112395125"
---
# <a name="width-property-characters-object"></a>Width, propriété (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la largeur du cadre pour le caractère spécifié.

</dd> <dt>

<span id="Syntax_"></span><span id="syntax_"></span><span id="SYNTAX_"></span>**Stockéesyntaxe** 
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[ =  *Valeur* de largeur\]



| Partie    | Description                                                |
|---------|------------------------------------------------------------|
| *value* | Entier long qui spécifie la largeur du cadre du caractère. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété [**Width**](width-property.md) est toujours exprimée en pixels. Le paramètre de cette propriété s’applique à tous les clients du caractère.

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.

 

 




