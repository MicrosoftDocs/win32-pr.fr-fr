---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727517"
---
# <a name="missingitemintaborder"></a>MissingItemInTabOrder

## <a name="text"></a>Texte

Cet élément semble être tabbable, mais il n’est pas dans l’ordre de tabulation.

## <a name="type"></a>Type

Error

## <a name="description"></a>Description

Un élément pouvant être actif n’est pas accessible à l’aide de la navigation au clavier standard (Tab ou Maj + Tab). Par exemple, l’élément n’a pas été marqué comme taquet de tabulation ou a assigné un index de tabulation. Ce problème provoque des problèmes pour les personnes qui reposent sur un lecteur d’écran et un clavier pour la navigation, car :

-   L’élément n’est pas détectable.
-   Si l’élément est un enfant d’un contrôle de liste personnalisé, les signaux indiquant que l’élément enfant peut être parcouru à l’aide des touches de direction ou de page sont peut-être manquants.

## <a name="possible-causes"></a>Causes possibles

-   Le rôle MSAA de l’élément ou de son parent n’est pas défini correctement. Par exemple, si tous les éléments de liste d’un contrôle List View ne sont pas exposés via MSAA comme un ListItem de système de rôle \_ \_ , la vérification échoue parce que les éléments de liste ne sont pas accessibles à l’aide de la touche Tab.
-   L’élément ou son parent est un contrôle personnalisé qui n’implémente pas correctement la tabulation. Par exemple, la propriété d’État MSAA n’est jamais définie sur STATE \_ System \_ Focusable.
-   Un élément qui joue le rôle d’un conteneur pour d’autres éléments a été sélectionné pour la vérification, mais ne prend pas en charge la navigation au clavier lui-même. Par exemple, une barre d’outils et ses éléments enfants ne sont pas accessibles à l’aide de la touche TAB.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recommandations en matière de conception d’interface utilisateur clavier](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 