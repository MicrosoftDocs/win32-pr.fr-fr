---
title: UI_PKEY_QuickAccessToolbarDock
description: Identifie la propriété QuickAccessToolbarDock de l’interface utilisateur \_ \_ .
ms.assetid: 77f7b0a8-f276-4501-9d53-fb5a3185edcc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ae48cb9ef2ee665739de2f3aacab197b461665
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382038"
---
# <a name="ui_pkey_quickaccesstoolbardock"></a><span data-ttu-id="1b3fa-103">IU \_ \_ QuickAccessToolbarDock</span><span class="sxs-lookup"><span data-stu-id="1b3fa-103">UI\_PKEY\_QuickAccessToolbarDock</span></span>

<span data-ttu-id="1b3fa-104">Identifie la propriété QuickAccessToolbarDock de l’interface utilisateur \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1b3fa-104">Identifies the UI\_PKEY\_QuickAccessToolbarDock property.</span></span>

```
propertyDescription
   name = UI_PKEY_QuickAccessToolbarDock
   shellPKey = UI_PKEY_QuickAccessToolbarDock
   formatID = 00001002-7363-696e-8441798acf5aebb7
   propID = 1002
   typeInfo
      type = UI_CONTROLDOCK
```

## <a name="remarks"></a><span data-ttu-id="1b3fa-105">Notes</span><span class="sxs-lookup"><span data-stu-id="1b3fa-105">Remarks</span></span>

<span data-ttu-id="1b3fa-106">L’interface utilisateur \_ \_ QuickAccessToolbarDock est utilisée par une application pour interroger l’état d’ancrage de la barre d’outils accès rapide (qat).</span><span class="sxs-lookup"><span data-stu-id="1b3fa-106">UI\_PKEY\_QuickAccessToolbarDock is used by an application to query the dock-state of the Quick Access Toolbar (QAT).</span></span>

<span data-ttu-id="1b3fa-107">La valeur de la propriété provient de l’énumération [**\_ CONTROLDOCK de l’interface utilisateur**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) .</span><span class="sxs-lookup"><span data-stu-id="1b3fa-107">The property value is from the [**UI\_CONTROLDOCK**](/windows/desktop/api/uiribbon/ne-uiribbon-ui_controldock) enumeration.</span></span>



|                         |                                                                                                                                                                                                                                                       |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3fa-108">CONTROLDOCK de l’interface utilisateur \_ \_ haut</span><span class="sxs-lookup"><span data-stu-id="1b3fa-108">UI\_CONTROLDOCK\_TOP</span></span>    | <span data-ttu-id="1b3fa-109">Le QAT est ancré dans la zone non cliente de l’application hôte du ruban, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-109">The QAT is docked in the nonclient area of the Ribbon host application, as shown in the following screen shot.</span></span>![capture d’écran de la barre d’outils accès rapide ancrée au-dessus du ruban dans la zone non cliente.](images/properties/qat-docktop.png)<br/> |
| <span data-ttu-id="1b3fa-111">\_CONTROLDOCK \_ bas de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="1b3fa-111">UI\_CONTROLDOCK\_BOTTOM</span></span> | <span data-ttu-id="1b3fa-112">Le QAT est ancré sous la forme d’une bande intégrale visuelle sous le ruban, comme illustré dans la capture d’écran suivante.</span><span class="sxs-lookup"><span data-stu-id="1b3fa-112">The QAT is docked as a visually integral band below the Ribbon, as shown in the following screen shot.</span></span> ![capture d’écran de la barre d’outils accès rapide ancrée sous le ruban.](images/properties/qat-dockbottom.png)<br/>                           |



 

## <a name="related-topics"></a><span data-ttu-id="1b3fa-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1b3fa-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b3fa-115">Propriétés du ruban</span><span class="sxs-lookup"><span data-stu-id="1b3fa-115">Ribbon Properties</span></span>](windowsribbon-reference-properties-ribbon.md)
</dt> </dl>

 

