---
title: Interfaces de stockage
description: Interfaces de stockage
ms.assetid: bce0fd46-eeba-4a14-be1f-63d16885c28d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ad0cc646d45ca0b77a70ecaf47d28eadb4d136
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549264"
---
# <a name="storage-interfaces"></a><span data-ttu-id="41265-103">Interfaces de stockage</span><span class="sxs-lookup"><span data-stu-id="41265-103">Storage Interfaces</span></span>

<span data-ttu-id="41265-104">Les conteneurs de contrôle doivent être en mesure de prendre en charge les contrôles qui implémentent [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream)ou [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span><span class="sxs-lookup"><span data-stu-id="41265-104">Control containers must be able to support controls that implement [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), or [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit).</span></span> <span data-ttu-id="41265-105">Un conteneur peut éventuellement prendre en charge d’autres interfaces de persistance, telles que [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag)et [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) , pour les contrôles qui assurent la prise en charge.</span><span class="sxs-lookup"><span data-stu-id="41265-105">Optionally, a container can support any other persistence interfaces such as [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), and [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)) for those controls that provide support.</span></span>

<span data-ttu-id="41265-106">Une fois qu’un conteneur de contrôles ActiveX a choisi et initialisé une interface de stockage à utiliser ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc.), cette interface de stockage restera l’interface de stockage principal pour la durée de vie du contrôle, c’est-à-dire que le contrôle restera en possession du stockage.</span><span class="sxs-lookup"><span data-stu-id="41265-106">Once an ActiveX control container has chosen and initialized a storage interface to use ([**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream), [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit), etc), that storage interface will remain the primary storage interface for the lifetime of the control, i.e. the control will remain in possession of the storage.</span></span> <span data-ttu-id="41265-107">Cela n’empêche pas le conteneur d’enregistrer dans d’autres interfaces de stockage.</span><span class="sxs-lookup"><span data-stu-id="41265-107">This does not preclude the container from saving to other storage interfaces.</span></span>

<span data-ttu-id="41265-108">Les conteneurs de contrôles ActiveX n’ont pas besoin de prendre en charge un mécanisme d’enregistrement en tant que texte. par conséquent, l’utilisation de [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) et de l’interface côté conteneur associée [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) est facultative.</span><span class="sxs-lookup"><span data-stu-id="41265-108">ActiveX control containers do not need to support a save as text mechanism, thus using [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag) and the associated container-side interface [**IPropertyBag**](/windows/win32/api/oaidl/nn-oaidl-ipropertybag) are optional.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41265-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41265-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41265-110">Containers</span><span class="sxs-lookup"><span data-stu-id="41265-110">Containers</span></span>](containers.md)
</dt> </dl>

 

 