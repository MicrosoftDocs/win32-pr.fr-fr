---
description: L’événement SetTargetPath indique au programme d’installation de vérifier et de définir le chemin d’accès sélectionné. Si le chemin d’accès n’est pas valide pour l’écriture, le programme d’installation bloque tout autre ControlEvents associé au contrôle.
ms.assetid: 5649da99-1541-47ab-9d2e-b33a705998ec
title: SetTargetPath ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36812d291ab4410b08c577e6d118c3ff9e5dc0b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238614"
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

 

 



