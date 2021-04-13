---
title: Propriétés d’annotation qui ont des WinEvents correspondants
description: Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, State, value et, pour certains contrôles, les propriétés Name).
ms.assetid: 2505d015-9381-4e1c-a10f-6db3fbb25ca3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a8849c66cb0067b63be1c846e9e140ae06f4b6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382204"
---
# <a name="annotation-properties-that-have-corresponding-winevents"></a><span data-ttu-id="f4d54-103">Propriétés d’annotation qui ont des WinEvents correspondants</span><span class="sxs-lookup"><span data-stu-id="f4d54-103">Annotation Properties That Have Corresponding WinEvents</span></span>

<span data-ttu-id="f4d54-104">Soyez prudent lors du remplacement des propriétés qui changent fréquemment, en particulier celles qui sont examinées par les clients à la suite d’un WinEvent (par exemple, [**State**](state-property.md), [**value**](value-property.md)et, pour certains contrôles, les propriétés [**Name**](name-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="f4d54-104">Be careful when overriding properties that change frequently, particularly those that are examined by clients as a result of a WinEvent (such as [**State**](state-property.md), [**Value**](value-property.md), and, for some controls, the [**Name**](name-property.md) properties).</span></span>

<span data-ttu-id="f4d54-105">Dans de nombreux cas, en particulier pour les contrôles utilisateur et ComCtl, le WinEvent signalant une modification de propriété est envoyé avant que le propriétaire du contrôle soit notifié (généralement via la [ \_ notification WM](../controls/wm-notify.md)).</span><span class="sxs-lookup"><span data-stu-id="f4d54-105">In many cases, especially for USER and ComCtl controls, the WinEvent signaling a property change is sent before the owner of the control is notified (typically via [WM\_NOTIFY](../controls/wm-notify.md)).</span></span> <span data-ttu-id="f4d54-106">La mise à jour de la propriété à l’aide de [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) dans le \_ Gestionnaire WM Notify sera trop tardive ; les clients utilisant le raccordement in-context auront déjà accédé à l’ancienne valeur.</span><span class="sxs-lookup"><span data-stu-id="f4d54-106">Updating the property using [**SetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropvalue) in the WM\_NOTIFY handler will be too late; clients using in-context hooking will already have accessed the old value.</span></span>

<span data-ttu-id="f4d54-107">Vous pouvez gérer ces types de propriétés à l’aide d’objets de serveur de rappel (à l’aide de [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); Toutefois, le serveur ne peut pas utiliser un État mis à jour dans le \_ Gestionnaire WM Notify, car ce gestionnaire n’a pas encore été appelé.</span><span class="sxs-lookup"><span data-stu-id="f4d54-107">You can handle these types of properties by using callback server objects (using [**SetPropServer**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropservices-setpropserver)); however, the server cannot use any state that is updated in the WM\_NOTIFY handler because that handler will not yet have been called.</span></span> <span data-ttu-id="f4d54-108">Par exemple, au lieu d’utiliser une variable de valeur actuelle mise en cache qui est mise à jour dans le \_ Gestionnaire WM Notify et qui est obsolète, l’objet de rappel [**IAccPropServer :: GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) doit envoyer un message directement au contrôle pour obtenir sa vraie valeur actuelle afin de générer la propriété requise.</span><span class="sxs-lookup"><span data-stu-id="f4d54-108">For example, instead of using a cached current value variable that is updated in the WM\_NOTIFY handler and will be out-of-date, the [**IAccPropServer::GetPropValue**](/windows/desktop/api/Oleacc/nf-oleacc-iaccpropserver-getpropvalue) callback object should send a message directly to the control to get its true current value to generate the required property.</span></span>

 

 