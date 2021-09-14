---
description: Le ControlEvent, IgnoreChange est publié par le contrôle DirectoryList lorsque le dossier sélectionné passe d’un répertoire à un autre dans le contrôle. Cet événement doit être créé dans la table EventMapping.
ms.assetid: 4d3128a1-cbe3-457c-83b5-8f6ec1a7ba29
title: IgnoreChange ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9db909552e97f29b8ebcd9d58ac8688474788ec0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021400"
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

 

 



