---
title: Propriétés d’annotation qui ont des WinEvents correspondants
description: Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, State, value et, pour certains contrôles, les propriétés Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010716"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a>Propriétés d’annotation qui ont des WinEvents correspondants

Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, [**State**](state-property.md), [**value**](value-property.md)et, pour certains contrôles, les propriétés [**Name**](name-property.md) ).

Dans de nombreux cas, en particulier pour les contrôles utilisateur et ComCtl, le WinEvent signalant une modification de propriété est envoyé avant que le propriétaire du contrôle soit notifié (généralement via la [ \_ notification WM](../controls/wm-notify.md)). La mise à jour de la propriété à l’aide de [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) dans le \_ Gestionnaire WM Notify sera trop tardive ; les clients utilisant le raccordement in-context auront déjà accédé à l’ancienne valeur.

Vous pouvez gérer ces types de propriétés à l’aide d’objets de serveur de rappel (à l’aide de [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Toutefois, le serveur ne peut pas utiliser un État mis à jour dans le \_ Gestionnaire WM Notify, car ce gestionnaire n’a pas encore été appelé. Par exemple, au lieu d’utiliser une variable de valeur actuelle mise en cache qui est mise à jour dans le \_ Gestionnaire WM Notify et qui est obsolète, l’objet de rappel [**IAccPropServer :: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) doit envoyer un message directement au contrôle pour obtenir sa vraie valeur actuelle afin de générer la propriété requise.

 

 