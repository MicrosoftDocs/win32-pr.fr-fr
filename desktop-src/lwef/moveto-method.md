---
title: MoveTo, méthode
description: MoveTo, méthode
ms.assetid: cca2b1b8-0d44-4272-9f0b-f7afd091d802
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58a245d389bc23d79d9f6cc105fec28ed14f5d511123c1dd113115ff69fc95c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119609079"
---
# <a name="moveto-method"></a>MoveTo, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Déplace le caractère spécifié vers l’emplacement spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). MoveTo_ *  *x, y* \[ *Vitesse*\]



| Partie    | Description                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *x, y*   | Obligatoire. Valeur entière qui indique le bord gauche (*x*) et le bord supérieur (*y*) du frame d’animation. Exprimez ces coordonnées en pixels.                                                   |
| *Temps* | Facultatif. Valeur de type entier long spécifiant, en millisecondes, la vitesse de déplacement du cadre du caractère. La valeur par défaut est 1000. Si vous spécifiez zéro (0), le frame est déplacé sans qu’une animation ne soit lue. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Le serveur lit automatiquement l’animation appropriée assignée aux États **mobiles** . L’emplacement d’un caractère est basé sur l’angle supérieur gauche de son cadre.

Si vous déclarez une variable objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) . En outre, si l’animation associée n’a pas été chargée sur l’ordinateur local, le serveur définit la propriété d' [**État**](status-property.md) de l’objet de **requête** sur « failed » avec un numéro d’erreur approprié. Par conséquent, si vous utilisez le protocole HTTP pour accéder à des données de caractère ou d’animation, utilisez la méthode d' [**extraction**](get-method.md) pour charger les animations d’état de **déplacement** avant d’appeler la méthode **MoveTo** .

Même si l’animation n’est pas chargée, le serveur déplace toujours le frame.

> [!Note]  
> Si vous appelez **MoveTo** avec une valeur différente de zéro avant que le caractère ne soit affiché, un état d’échec est retourné si vous lui avez assigné un objet de [**requête**](/windows/desktop/lwef/the-request-object) , car la valeur différente de zéro indique que vous tentez de lire une animation lorsque le caractère n’est pas visible.

 

> [!Note]  
> L’effet réel du paramètre de *Vitesse* peut varier en fonction de la vitesse du processeur de l’ordinateur et de la priorité des autres tâches en cours d’exécution sur le système.

 

 

 