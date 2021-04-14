---
title: Contrôles ActiveX
description: Contrôles ActiveX
ms.assetid: e491b66c-d6ba-4476-8413-7a9e41c05e8d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b75aabfbf2b81b4a4d3a45a1868a6eebf6fd4e6
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382911"
---
# <a name="activex-controls"></a><span data-ttu-id="07ef1-103">Contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="07ef1-103">ActiveX Controls</span></span>

<span data-ttu-id="07ef1-104">La technologie des contrôles ActiveX repose sur une Fondation composée d’objets COM, connectables, de documents composés, de pages de propriétés, d’Automation OLE, de persistance d’objets et d’objets de police et d’image fournis par le système.</span><span class="sxs-lookup"><span data-stu-id="07ef1-104">ActiveX controls technology rests on a foundation consisting of COM, connectable objects, compound documents, property pages, OLE automation, object persistence, and system-provided font and picture objects.</span></span> <span data-ttu-id="07ef1-105">Comme résumé ci-dessous, chacune de ces technologies de base joue un rôle dans les contrôles.</span><span class="sxs-lookup"><span data-stu-id="07ef1-105">As summarized below, each of these core technologies plays a role in controls.</span></span>

<dl> <dt>

<span data-ttu-id="07ef1-106"><span id="COM"></span><span id="com"></span>COM</span><span class="sxs-lookup"><span data-stu-id="07ef1-106"><span id="COM"></span><span id="com"></span>COM</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-107">Un contrôle est essentiellement un objet COM qui expose l’interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) , par l’intermédiaire de laquelle les clients peuvent obtenir des pointeurs vers ses autres interfaces.</span><span class="sxs-lookup"><span data-stu-id="07ef1-107">A control is essentially a COM object that exposes the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface, through which clients can obtain pointers to its other interfaces.</span></span> <span data-ttu-id="07ef1-108">Les contrôles peuvent prendre en charge la gestion des licences via [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) et l’auto-inscription.</span><span class="sxs-lookup"><span data-stu-id="07ef1-108">Controls can support licensing through [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2) and self-registration.</span></span> <span data-ttu-id="07ef1-109">Pour plus d’informations sur COM, les licences et l’inscription automatique, consultez [modèle d’objet de composant](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-109">See [The Component Object Model](the-component-object-model.md) for more information on COM, licensing, and self-registration.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Objets connectables</span><span class="sxs-lookup"><span data-stu-id="07ef1-110"><span id="Connectable_objects"></span><span id="connectable_objects"></span><span id="CONNECTABLE_OBJECTS"></span>Connectable objects</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-111">Les contrôles peuvent prendre en charge les interfaces sortantes via des objets connectables afin que le contrôle puisse communiquer avec son client.</span><span class="sxs-lookup"><span data-stu-id="07ef1-111">Controls can support outgoing interfaces through connectable objects so that the control can communicate with its client.</span></span> <span data-ttu-id="07ef1-112">Par exemple, une interface sortante peut déclencher une action dans le client, notifier le client d’une modification du contrôle ou demander une autorisation au client avant que le contrôle ne prenne une mesure.</span><span class="sxs-lookup"><span data-stu-id="07ef1-112">For example, an outgoing interface can trigger an action in the client, can notify the client of some change in the control, or can request permission from the client before the control takes some action.</span></span> <span data-ttu-id="07ef1-113">Pour plus d’informations sur le fonctionnement des objets connectables, consultez [événements dans com et objets connectables](events-in-com-and-connectable-objects.md) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-113">See [Events in COM and Connectable Objects](events-in-com-and-connectable-objects.md) for more information on how connectable objects work.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Transfert de données uniforme</span><span class="sxs-lookup"><span data-stu-id="07ef1-114"><span id="Uniform_data_transfer"></span><span id="uniform_data_transfer"></span><span id="UNIFORM_DATA_TRANSFER"></span>Uniform data transfer</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-115">Les contrôles peuvent prendre en charge les glisser-déplacer dans un conteneur avec l’aide de leur conteneur.</span><span class="sxs-lookup"><span data-stu-id="07ef1-115">Controls can support being dragged and dropped within a container with help from their container.</span></span> <span data-ttu-id="07ef1-116">Pour plus d’informations sur le glisser-déplacer, consultez [**IOleInPlaceObjectWindowless :: GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-116">See [**IOleInPlaceObjectWindowless::GetDropTarget**](/windows/desktop/api/OCIdl/nf-ocidl-ioleinplaceobjectwindowless-getdroptarget) for more information on drag and drop.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Documents composés</span><span class="sxs-lookup"><span data-stu-id="07ef1-117"><span id="Compound_documents"></span><span id="compound_documents"></span><span id="COMPOUND_DOCUMENTS"></span>Compound documents</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-118">Un contrôle peut être un objet actif sur place qui peut être incorporé dans un client contenant.</span><span class="sxs-lookup"><span data-stu-id="07ef1-118">A control can be an in-place active object that can be embedded in a containing client.</span></span> <span data-ttu-id="07ef1-119">Un utilisateur final active le contrôle pour lancer une action dans l’application conteneur.</span><span class="sxs-lookup"><span data-stu-id="07ef1-119">An end-user activates the control to initiate an action in the container application.</span></span> <span data-ttu-id="07ef1-120">Pour plus d’informations sur l’activation sur place et d’autres interfaces de document composé, consultez [documents composés](compound-documents.md) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-120">See [Compound Documents](compound-documents.md) for more information on in-place activation and other compound document interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Pages de propriétés</span><span class="sxs-lookup"><span data-stu-id="07ef1-121"><span id="Property_pages"></span><span id="property_pages"></span><span id="PROPERTY_PAGES"></span>Property pages</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-122">Les contrôles peuvent fournir des pages de propriétés afin que les utilisateurs finaux puissent afficher et modifier les propriétés du contrôle.</span><span class="sxs-lookup"><span data-stu-id="07ef1-122">Controls can provide property pages so end users can view and change the control's properties.</span></span> <span data-ttu-id="07ef1-123">Pour plus d’informations sur le fonctionnement des pages de propriétés, consultez pages de propriétés [et feuilles de propriétés](property-pages-and-property-sheets.md) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-123">See [Property Pages and Property Sheets](property-pages-and-property-sheets.md) for more information on how property pages work.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE Automation</span><span class="sxs-lookup"><span data-stu-id="07ef1-124"><span id="OLE_automation"></span><span id="ole_automation"></span><span id="OLE_AUTOMATION"></span>OLE automation</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-125">Les contrôles peuvent assurer la programmabilité via OLE Automation afin que les clients puissent tirer parti des fonctionnalités du contrôle par le biais d’un langage de programmation fourni par le client.</span><span class="sxs-lookup"><span data-stu-id="07ef1-125">Controls can provide programmability through OLE automation so clients can take advantage of the control's features through a programming language supplied by the client.</span></span> <span data-ttu-id="07ef1-126">Pour plus d’informations sur l’automatisation OLE, consultez la section OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="07ef1-126">See the OLE Automation section for more information on OLE automation.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Stockage persistant</span><span class="sxs-lookup"><span data-stu-id="07ef1-127"><span id="Persistent_storage"></span><span id="persistent_storage"></span><span id="PERSISTENT_STORAGE"></span>Persistent storage</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-128">Un contrôle peut implémenter une ou plusieurs des interfaces de persistance multiples pour prendre en charge la persistance de son état.</span><span class="sxs-lookup"><span data-stu-id="07ef1-128">A control can implement one or more of several persistence interfaces to support persistence of its state.</span></span> <span data-ttu-id="07ef1-129">L’implémenteur de contrôle doit décider quels types de persistance sont les plus importants et implémenter les interfaces de persistance appropriées.</span><span class="sxs-lookup"><span data-stu-id="07ef1-129">The control implementer must decide what kinds of persistence are most important and implement the appropriate persistence interfaces.</span></span> <span data-ttu-id="07ef1-130">Le client décide de l’interface qu’il préfère utiliser.</span><span class="sxs-lookup"><span data-stu-id="07ef1-130">The client decides which interface it prefers to use.</span></span> <span data-ttu-id="07ef1-131">Pour plus d’informations sur toutes les interfaces de persistance, consultez [modèle d’objet de composant](the-component-object-model.md) .</span><span class="sxs-lookup"><span data-stu-id="07ef1-131">See [The Component Object Model](the-component-object-model.md) for more information on all the persistence interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="07ef1-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Objets de police et d’image</span><span class="sxs-lookup"><span data-stu-id="07ef1-132"><span id="Font_and_picture_objects"></span><span id="font_and_picture_objects"></span><span id="FONT_AND_PICTURE_OBJECTS"></span>Font and picture objects</span></span>
</dt> <dd>

<span data-ttu-id="07ef1-133">Les contrôles peuvent utiliser ces objets fournis par le système pour fournir une représentation visuelle d’eux-mêmes au sein du client.</span><span class="sxs-lookup"><span data-stu-id="07ef1-133">Controls can use these system provided objects to provide a visual representation of themselves within the client.</span></span> <span data-ttu-id="07ef1-134">L’objet font implémente plusieurs interfaces, y compris [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) et [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span><span class="sxs-lookup"><span data-stu-id="07ef1-134">The font object implements several interfaces, including [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) and [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp).</span></span> <span data-ttu-id="07ef1-135">Un objet font peut être créé avec [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span><span class="sxs-lookup"><span data-stu-id="07ef1-135">A font object can be created with [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect).</span></span> <span data-ttu-id="07ef1-136">L’objet Picture implémente également plusieurs interfaces, notamment [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) et [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span><span class="sxs-lookup"><span data-stu-id="07ef1-136">The picture object also implements several interfaces, including [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp).</span></span> <span data-ttu-id="07ef1-137">Un objet image peut être créé à l’aide de [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) et peut être chargé à partir d’un flux avec [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span><span class="sxs-lookup"><span data-stu-id="07ef1-137">A picture object can be created using [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect) and can loaded from a stream with [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture).</span></span>

</dd> </dl>

<span data-ttu-id="07ef1-138">Il est important de comprendre que ces fonctionnalités peuvent être utilisées dans n’importe quel objet OLE.</span><span class="sxs-lookup"><span data-stu-id="07ef1-138">It is important to understand that these features can be used in any OLE object.</span></span> <span data-ttu-id="07ef1-139">Il n’est pas nécessaire d’implémenter un contrôle pour pouvoir utiliser ces fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="07ef1-139">One does not need to implement a control in order to use these features.</span></span> <span data-ttu-id="07ef1-140">En outre, la seule interface requise sur un contrôle est IUnknown.</span><span class="sxs-lookup"><span data-stu-id="07ef1-140">Also, the only required interface on a control is IUnknown.</span></span> <span data-ttu-id="07ef1-141">Le contrôle prend éventuellement en charge d’autres interfaces en fonction de la nécessité de prendre en charge les fonctionnalités associées.</span><span class="sxs-lookup"><span data-stu-id="07ef1-141">The control optionally supports other interfaces based on the need to support the related features.</span></span>

<span data-ttu-id="07ef1-142">Outre ces fonctionnalités, les interfaces et fonctions suivantes sont spécifiques à la technologie des contrôles : [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**IsimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)et [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span><span class="sxs-lookup"><span data-stu-id="07ef1-142">In addition to these features, the following interfaces and functions are specific to controls technology: [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol), [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite), [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor).</span></span> <span data-ttu-id="07ef1-143">En outre, certains contrôles sont un ensemble de normes pour les propriétés et les méthodes qu’un contrôle ou un conteneur de contrôle peut prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="07ef1-143">Also specific to controls are a set of standards for properties and methods that a control or a control container can support.</span></span>

> [!Note]  
> <span data-ttu-id="07ef1-144">La bibliothèque système OleAut32.dll contient des implémentations des fonctions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture)et [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span><span class="sxs-lookup"><span data-stu-id="07ef1-144">The system library OleAut32.dll contains implementations of the functions ([**OleCreatePropertyFrame**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframe), [**OleCreatePropertyFrameIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepropertyframeindirect), [**OleCreateFontIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatefontindirect), [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect), [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture), and [**OleTranslateColor**](/windows/desktop/api/OleCtl/nf-olectl-oletranslatecolor)).</span></span> <span data-ttu-id="07ef1-145">En outre, OleAut32.dll contient les implémentations des objets de police et d’image standard, ainsi qu’une bibliothèque de types pour toutes les interfaces utilisées avec les contrôles, ainsi que les structures de données et types de données supplémentaires.</span><span class="sxs-lookup"><span data-stu-id="07ef1-145">In addition, OleAut32.dll contains the implementations of the standard font and picture objects, as well as a type library for all the interfaces used with controls as well as the additional data structures and data types.</span></span>

 

<span data-ttu-id="07ef1-146">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="07ef1-146">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="07ef1-147">Architecture des contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="07ef1-147">ActiveX Controls Architecture</span></span>](activex-controls-architecture.md)
-   [<span data-ttu-id="07ef1-148">Interfaces de contrôles ActiveX</span><span class="sxs-lookup"><span data-stu-id="07ef1-148">ActiveX Controls Interfaces</span></span>](activex-controls-interfaces.md)
-   [<span data-ttu-id="07ef1-149">Propriétés et méthodes</span><span class="sxs-lookup"><span data-stu-id="07ef1-149">Properties and Methods</span></span>](properties-and-methods.md)
-   [<span data-ttu-id="07ef1-150">Événements de contrôle</span><span class="sxs-lookup"><span data-stu-id="07ef1-150">Control Events</span></span>](control-events.md)
-   [<span data-ttu-id="07ef1-151">Représentation visuelle</span><span class="sxs-lookup"><span data-stu-id="07ef1-151">Visual Representation</span></span>](visual-representation.md)
-   [<span data-ttu-id="07ef1-152">Gestion du clavier pour les contrôles</span><span class="sxs-lookup"><span data-stu-id="07ef1-152">Keyboard Handling for Controls</span></span>](keyboard-handling-for-controls.md)
-   [<span data-ttu-id="07ef1-153">Persistance</span><span class="sxs-lookup"><span data-stu-id="07ef1-153">Persistence</span></span>](persistence.md)
-   [<span data-ttu-id="07ef1-154">Inscription et licences</span><span class="sxs-lookup"><span data-stu-id="07ef1-154">Registration and Licensing</span></span>](registration-and-licensing.md)

## <a name="related-topics"></a><span data-ttu-id="07ef1-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="07ef1-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="07ef1-156">Instructions relatives au contrôle ActiveX et au conteneur de contrôles</span><span class="sxs-lookup"><span data-stu-id="07ef1-156">ActiveX Control and Control Container Guidelines</span></span>](activex-control-and-control-container-guidelines.md)
</dt> </dl>

 

 