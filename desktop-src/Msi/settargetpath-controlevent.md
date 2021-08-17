---
description: L’événement SetTargetPath indique au programme d’installation de vérifier et de définir le chemin d’accès sélectionné. Si le chemin d’accès n’est pas valide pour l’écriture, le programme d’installation bloque tout autre ControlEvents associé au contrôle.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e49e9447d7d2e67dce85e7d60638c18a949ecbc87800d12a60bc94d971cb30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118625069"
---
# <a name="settargetpath-controlevent"></a>SetTargetPath ControlEvent,

L’événement SetTargetPath indique au programme d’installation de vérifier et de définir le chemin d’accès sélectionné. Si le chemin d’accès n’est pas valide pour l’écriture, le programme d’installation bloque tout autre ControlEvents associé au contrôle.

Cet événement peut être publié par un [contrôle PUSHBUTTON](pushbutton-control.md)ou un [contrôle SelectionTree](selectiontree-control.md). Cet événement doit être créé dans la [table ControlEvent,](controlevent-table.md).

Ce ControlEvent, nécessite que l’interface utilisateur soit exécutée au niveau de l' [*interface utilisateur complète*](f-gly.md) . Cet événement ne fonctionne pas avec une interface utilisateur [*réduite*](r-gly.md) ou une [*interface utilisateur de base*](b-gly.md). Pour plus d’informations, consultez [niveaux d’interface utilisateur](user-interface-levels.md).

## <a name="published-by"></a>Publié par

Ce ControlEvent, est publié par le programme d’installation.

## <a name="argument"></a>Argument

Nom de la propriété contenant le chemin d’accès. Si la propriété est indirecte, le nom de la propriété est placé entre crochets.

## <a name="action-on-subscribers"></a>Action sur les abonnés

Aucun.

## <a name="typical-use"></a>Utilisation courante

Un contrôle [PUSHBUTTON](pushbutton-control.md) sur une boîte de dialogue de navigation est lié à cet événement dans la table [ControlEvent,](controlevent-table.md) pour vérifier le chemin d’accès sélectionné avant de revenir à la boîte de dialogue de sélection.

## <a name="remarks"></a>Remarques

N’essayez pas de configurer le chemin d’accès cible si les composants qui utilisent ces chemins d’accès sont déjà installés pour l’utilisateur actuel ou pour un autre utilisateur. Vérifiez la propriété [**ProductState**](productstate.md) avant de publier le ControlEvent, SetTargetPath pour déterminer si le produit contenant le composant est installé.

 

 



