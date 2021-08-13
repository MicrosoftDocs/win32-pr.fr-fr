---
description: Le ControlEvent, IgnoreChange est publié par le contrôle DirectoryList lorsque le dossier sélectionné passe d’un répertoire à un autre dans le contrôle. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8efc2750c4d1e2bd85f7c31348f507917f828725de95658095e964b22a110a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118634457"
---
# <a name="ignorechange-controlevent"></a>IgnoreChange ControlEvent,

Le ControlEvent, IgnoreChange est publié par le [contrôle DirectoryList](directorylist-control.md) lorsque le dossier sélectionné passe d’un répertoire à un autre dans le contrôle. Cet événement doit être créé dans la [table EventMapping](eventmapping-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

[DirectoryList](directorylist-control.md)

## <a name="argument"></a>Argument

Ce ControlEvent, n’utilise pas d’argument.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Ce ControlEvent, n’effectue pas d’action sur les abonnés.

## <a name="typical-use"></a>Utilisation courante

Le [contrôle DirectoryCombo](directorycombo-control.md) utilise généralement le ControlEvent, IgnoreChange.

 

 



