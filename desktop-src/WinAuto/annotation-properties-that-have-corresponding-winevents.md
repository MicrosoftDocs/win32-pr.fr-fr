---
title: Propriétés d’annotation qui ont des WinEvents correspondants
description: Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, State, value et, pour certains contrôles, les propriétés Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 753a17498daf9966ed1c3dfa98dc64fbdb2290011842c4fe9c194f50bf408ee1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098509"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Propriétés d’annotation qui ont des WinEvents correspondants

Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, [**State**](state-property.md), [**value**](value-property.md)et, pour certains contrôles, les propriétés [**Name**](name-property.md) ).

Dans de nombreux cas, en particulier pour les contrôles utilisateur et ComCtl, le WinEvent signalant une modification de propriété est envoyé avant que le propriétaire du contrôle soit notifié (généralement via la [ \_ notification WM](../controls/wm-notify.md)). La mise à jour de la propriété à l’aide de [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) dans le \_ Gestionnaire WM Notify sera trop tardive ; les clients utilisant le raccordement in-context auront déjà accédé à l’ancienne valeur.

Vous pouvez gérer ces types de propriétés à l’aide d’objets de serveur de rappel (à l’aide de [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Toutefois, le serveur ne peut pas utiliser un État mis à jour dans le \_ Gestionnaire WM Notify, car ce gestionnaire n’a pas encore été appelé. Par exemple, au lieu d’utiliser une variable de valeur actuelle mise en cache qui est mise à jour dans le \_ Gestionnaire WM Notify et qui est obsolète, l’objet de rappel [**IAccPropServer :: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) doit envoyer un message directement au contrôle pour obtenir sa vraie valeur actuelle afin de générer la propriété requise.

 

 