---
description: Le programme d’installation utilise cet événement pour publier des données sur la dernière action. Les données peuvent être affichées dans une boîte de dialogue par un contrôle de texte qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 3c0ab7d0-35f2-4966-8eff-f9f0419d8eed
title: ActionData ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13bbfe27a59dbe0eda27e7a24e654711d1999188
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106521538"
---
# <a name="actiondata-controlevent"></a>ActionData ControlEvent,

Le programme d’installation utilise cet événement pour publier des données sur la dernière action. Les données peuvent être affichées dans une boîte de dialogue par un [contrôle de texte](text-control.md) qui s’abonne à ce ControlEvent,. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) . Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Les abonnés sont masqués lorsqu’une nouvelle action démarre et s’affichent quand de nouvelles données d’action arrivent du programme d’installation.

## <a name="typical-use"></a>Utilisation courante

Un [contrôle de texte](text-control.md) sur une boîte de dialogue non modale s’abonne à cet événement par le biais de la [table EventMapping](eventmapping-table.md). L' [attribut de contrôle de texte](text-control-attribute.md) est listé dans le champ attributs de ce tableau pour recevoir les données d’action actuelles. Généralement utilisé pour afficher les noms des fichiers copiés lors de la copie de fichiers.

 

 



