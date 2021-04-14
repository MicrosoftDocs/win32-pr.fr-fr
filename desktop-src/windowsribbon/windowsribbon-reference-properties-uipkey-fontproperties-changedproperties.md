---
title: UI_PKEY_FontProperties_ChangedProperties
description: Identifie la \_ \_ propriété FontProperties ChangedProperties de l’interface utilisateur \_ .
ms.assetid: d96b89b5-af30-4e76-b6ec-03fbb8d28ab3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124b36d5e24f4e0c0122cffdbbed11669a4ea510
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382408"
---
# <a name="ui_pkey_fontproperties_changedproperties"></a><span data-ttu-id="df304-103">IU \_ \_ FontProperties \_ ChangedProperties</span><span class="sxs-lookup"><span data-stu-id="df304-103">UI\_PKEY\_FontProperties\_ChangedProperties</span></span>

<span data-ttu-id="df304-104">Identifie la \_ \_ propriété FontProperties ChangedProperties de l’interface utilisateur \_ .</span><span class="sxs-lookup"><span data-stu-id="df304-104">Identifies the UI\_PKEY\_FontProperties\_ChangedProperties property.</span></span>

```
propertyDescription
   name = UI_PKEY_FontProperties_ChangedProperties
   shellPKey = UI_PKEY_FontProperties_ChangedProperties
   formatID = 00000312-7363-696e-8441798acf5aebb7
   propID = 13
   typeInfo
      type = IUISimplePropertySet
```

## <a name="remarks"></a><span data-ttu-id="df304-105">Notes</span><span class="sxs-lookup"><span data-stu-id="df304-105">Remarks</span></span>

<span data-ttu-id="df304-106">L’interface utilisateur \_ \_ FontProperties \_ ChangedProperties est utilisée par une application pour interroger uniquement les propriétés modifiées à partir de [l’IU \_ \_ FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span><span class="sxs-lookup"><span data-stu-id="df304-106">UI\_PKEY\_FontProperties\_ChangedProperties is used by an application to query only changed properties from [UI\_PKEY\_FontProperties](windowsribbon-reference-properties-uipkey-fontproperties.md).</span></span>

<span data-ttu-id="df304-107">L’appel de la méthode [**IUISimplePropertySet :: GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) sur cet objet [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) retourne un [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="df304-107">Calling the [**IUISimplePropertySet::GetValue**](/windows/desktop/api/uiribbon/nf-uiribbon-iuisimplepropertyset-getvalue) method on this [**IUISimplePropertySet**](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset) object returns an [IPropertyStore](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

<span data-ttu-id="df304-108">L’interface utilisateur \_ \_ FontProperties \_ ChangedProperties est passée en tant que dernier paramètre de l’appel [**IUICommandHandler :: Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) à l’application hôte du ruban.</span><span class="sxs-lookup"><span data-stu-id="df304-108">UI\_PKEY\_FontProperties\_ChangedProperties is passed as the last parameter of the [**IUICommandHandler::Execute**](/windows/desktop/api/uiribbon/nf-uiribbon-iuicommandhandler-execute) call to the Ribbon host application.</span></span>

<span data-ttu-id="df304-109">Cette clé de propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="df304-109">This property key is read-only.</span></span>

## <a name="related-topics"></a><span data-ttu-id="df304-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="df304-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df304-111">Propriétés du contrôle de police</span><span class="sxs-lookup"><span data-stu-id="df304-111">Font Control Properties</span></span>](windowsribbon-reference-properties-fontcontrol.md)
</dt> <dt>

[<span data-ttu-id="df304-112">**IUISimplePropertySet**</span><span class="sxs-lookup"><span data-stu-id="df304-112">**IUISimplePropertySet**</span></span>](/windows/desktop/api/uiribbon/nn-uiribbon-iuisimplepropertyset)
</dt> <dt>

[<span data-ttu-id="df304-113">Contrôle de police</span><span class="sxs-lookup"><span data-stu-id="df304-113">Font Control</span></span>](windowsribbon-controls-fontcontrol.md)
</dt> </dl>

 

 