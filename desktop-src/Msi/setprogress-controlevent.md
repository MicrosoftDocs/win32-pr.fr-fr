---
description: Le programme d’installation utilise l’événement SetProgress pour publier des informations sur la progression de l’installation.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22e36ecf5851713d7460f8f249b77871439c628f2adfce516aea29db52ad7942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625079"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent,

Le programme d’installation utilise l’événement SetProgress pour publier des informations sur la progression de l’installation. Un contrôle [ProgressBar](progressbar-control.md) ou un contrôle de tableau [blanc](billboard-control.md) doit s’abonner à l’événement via la [table EventMapping](eventmapping-table.md) en nommant l’action dont la progression est indiquée. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, peut être géré par une interface utilisateur qui s’exécute au niveau de l’interface utilisateur de [*base*](b-gly.md), de l' [*interface utilisateur réduite*](r-gly.md)ou de l’interface utilisateur [*complète*](f-gly.md) . Pour plus d’informations sur les niveaux d’interface utilisateur, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Aucun.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [ProgressBar](progressbar-control.md) sur une boîte de dialogue non modale s’abonne à cet événement à l’aide de l’attribut [Progress](progress-control-attribute.md) pour recevoir les informations de progression.

 

 



