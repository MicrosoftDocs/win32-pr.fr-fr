---
title: Propriété Top (objet Characters)
description: En savoir plus sur la propriété Top (objet Characters). Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.
ms.assetid: d5758a77-2d9a-44b8-bbbb-57ddf96c7fe4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a5e26d2ef578a98447d47eb2a3fae3613760a9
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396344"
---
# <a name="top-property-characters-object"></a>Propriété Top (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le bord supérieur du frame du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[  =  *Valeur* supérieure\]



| Partie    | Description                                             |
|---------|---------------------------------------------------------|
| *value* | Entier long qui spécifie le bord supérieur du caractère. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **Top** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche). Le paramètre de cette propriété s’applique à tous les clients du caractère.

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.

Utilisez la méthode [**MoveTo**](moveto-method.md) pour modifier l’emplacement du caractère.

## <a name="see-also"></a>Voir aussi

[**Propriété Left**](left-property.md), [ **méthode MoveTo**](moveto-method.md)


 

 




