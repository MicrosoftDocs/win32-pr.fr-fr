---
title: Surcharge de IPropertyNotifySink
description: Surcharge de IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380273"
---
# <a name="overloading-ipropertynotifysink"></a><span data-ttu-id="5ffad-103">Surcharge de IPropertyNotifySink</span><span class="sxs-lookup"><span data-stu-id="5ffad-103">Overloading IPropertyNotifySink</span></span>

<span data-ttu-id="5ffad-104">De nombreux conteneurs de contrôles ActiveX implémentent une fenêtre de navigation des propriétés non modale.</span><span class="sxs-lookup"><span data-stu-id="5ffad-104">Many ActiveX control containers implement a modeless property browsing window.</span></span> <span data-ttu-id="5ffad-105">Si les propriétés d’un contrôle sont modifiées par le biais des pages de propriétés du contrôle, les propriétés du contrôle peuvent être désynchronisées avec la vue du conteneur de ces propriétés (le contrôle est toujours correct, bien sûr).</span><span class="sxs-lookup"><span data-stu-id="5ffad-105">If a control's properties are altered through the control's property pages, then the control's properties can get out of sync with the container's view of those properties (the control is always right, of course).</span></span> <span data-ttu-id="5ffad-106">Pour garantir qu’il a toujours les valeurs actuelles pour les propriétés d’un contrôle, un conteneur de contrôles ActiveX peut surcharger l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (liaison de données) et l’utiliser pour être informé qu’une propriété de contrôle a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="5ffad-106">To ensure that it always has the current values for a control's properties, an ActiveX control container can overload the [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) interface (data binding) and also use it to be notified that a control property has changed.</span></span> <span data-ttu-id="5ffad-107">Cette technique est facultative et n’est pas requise pour les conteneurs de contrôles ActiveX ou les contrôles ActiveX.</span><span class="sxs-lookup"><span data-stu-id="5ffad-107">This technique is optional and is not required of ActiveX control containers or ActiveX controls.</span></span>

<span data-ttu-id="5ffad-108">Notez qu’un contrôle doit utiliser [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) uniquement pour la liaison de données ; Il est libre d’utiliser [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) pour l’une ou les deux opérations.</span><span class="sxs-lookup"><span data-stu-id="5ffad-108">Note that a control should use [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) only for data binding; it is free to use [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) for either or both purposes.</span></span>

 

 




