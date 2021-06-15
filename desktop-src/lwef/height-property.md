---
title: Propriété Height (objet Characters)
description: En savoir plus sur la propriété Height de l’objet Characters. Microsoft Agent est déconseillé à partir de Windows 7.
ms.assetid: 2c8dc333-e3c1-4f25-833b-9a4262c75b9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d93d288276bd9717378c9a1ab0d9b00489959c00
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068509"
---
# <a name="height-property-characters-object"></a>Propriété Height (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit la hauteur du cadre du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[ =  *Valeur* de hauteur\]



| Partie    | Description                                                 |
|---------|-------------------------------------------------------------|
| *value* | Entier long qui spécifie la hauteur du frame du caractère. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

La propriété **Height** est toujours exprimée en pixels, par rapport aux coordonnées d’écran (en haut à gauche). Le paramètre de cette propriété s’applique à tous les clients du caractère.

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, la hauteur du caractère est basée sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.

 

 




