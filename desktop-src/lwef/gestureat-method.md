---
title: Méthode GestureAt
description: Méthode GestureAt
ms.assetid: c84e9363-e905-476a-832b-9acf6ddee5f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7222c2c0529a486583999f4f9f363e3a30cafc02
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104462987"
---
# <a name="gestureat-method"></a>Méthode GestureAt

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Lit l’animation gesturing pour le caractère spécifié à l’emplacement spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («*** CharacterID * * * »). GestureAt* *  *x, y*



| Partie  | Description                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y* | Obligatoire. Valeur entière qui indique la coordonnée d’écran horizontale (*x*) et la coordonnée d’écran verticale (*y*) à laquelle le caractère sera geste. Ces coordonnées doivent être spécifiées en pixels. |



 

</dd> </dl>

## <a name="remarks"></a>Notes

Le serveur lit automatiquement l’animation appropriée au geste vers l’emplacement spécifié. Les coordonnées sont toujours relatives à l’origine de l’écran (en haut à gauche).

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si l’animation associée n’a pas été chargée sur l’ordinateur local, le serveur définit la propriété d' [**État**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro d’erreur approprié. Par conséquent, si vous utilisez le protocole HTTP pour accéder aux données d’animation de caractères, utilisez la méthode d' [**extraction**](get-method.md) pour charger les animations d’état **gesturing** avant d’appeler la méthode **GestureAt** .

 

 