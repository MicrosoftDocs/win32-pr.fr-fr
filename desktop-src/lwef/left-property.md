---
title: Propriété Left (objet Characters)
description: Propriété Left
ms.assetid: f496f075-6430-4806-a237-1c7b626d355e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a318e659405883c56f296a9371eba7e9423662b1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "106509497"
---
# <a name="left-property-characters-object"></a>Propriété Left (objet Characters)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Retourne ou définit le bord gauche du cadre du caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  \[  =  *Valeur* de gauche\]



| Partie    | Description                                                           |
|---------|-----------------------------------------------------------------------|
| *value* | Entier long qui spécifie le bord gauche du frame du caractère. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

La propriété **Left** est toujours exprimée en pixels, par rapport à l’origine de l’écran (en haut à gauche). Le paramètre de cette propriété s’applique à tous les clients du caractère.

Même si le caractère apparaît dans une fenêtre de zone de forme irrégulière, l’emplacement du caractère est basé sur les dimensions externes du cadre d’animation rectangulaire utilisé lorsque le caractère a été compilé avec l’éditeur de caractères Microsoft Agent.

 

 




