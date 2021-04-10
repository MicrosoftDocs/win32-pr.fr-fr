---
title: Objet image standard
description: Objet image standard
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103941394"
---
# <a name="standard-picture-object"></a><span data-ttu-id="7e76c-103">Objet image standard</span><span class="sxs-lookup"><span data-stu-id="7e76c-103">Standard Picture Object</span></span>

<span data-ttu-id="7e76c-104">L’objet image standard fournit une abstraction indépendante du langage pour les images GDI : les bitmaps, les icônes, les reformateurs et les sous-fichiers améliorés.</span><span class="sxs-lookup"><span data-stu-id="7e76c-104">The standard picture object provides a language-neutral abstraction for GDI images: bitmaps, icons, metafiles, and enhanced metafiles.</span></span> <span data-ttu-id="7e76c-105">Comme avec l’objet de police standard, le système fournit une implémentation standard de cet objet.</span><span class="sxs-lookup"><span data-stu-id="7e76c-105">As with the standard font object, the system provides a standard implementation of this object.</span></span> <span data-ttu-id="7e76c-106">Ses interfaces principales sont [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) et [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), ce qui est dérivé de **IDispatch** pour fournir l’accès aux propriétés de l’image par le biais d’OLE Automation.</span><span class="sxs-lookup"><span data-stu-id="7e76c-106">Its primary interfaces are [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) and [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), the latter being derived from **IDispatch** to provide access to the picture's properties through OLE automation.</span></span> <span data-ttu-id="7e76c-107">Un objet image est créé avec [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span><span class="sxs-lookup"><span data-stu-id="7e76c-107">A picture object is created new with [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).</span></span>

<span data-ttu-id="7e76c-108">L’objet image prend également en charge l’interface de l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) pour permettre à un client de déterminer quand les propriétés de l’image changent.</span><span class="sxs-lookup"><span data-stu-id="7e76c-108">The picture object also supports the outgoing interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) so that a client can determine when picture properties change.</span></span> <span data-ttu-id="7e76c-109">En conséquence, l’objet image prend également en charge [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) et un point de connexion pour **IPropertyNotifySink**.</span><span class="sxs-lookup"><span data-stu-id="7e76c-109">Accordingly, the picture object also supports [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) and one connection point for **IPropertyNotifySink**.</span></span>

<span data-ttu-id="7e76c-110">L’objet image prend également en charge [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) de sorte qu’il puisse s’enregistrer et se charger à partir d’une instance de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="7e76c-110">The picture object also supports [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) such that it can save and load itself from an instance of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span> <span data-ttu-id="7e76c-111">Un objet qui utilise un objet image en interne enregistre et charge l’image dans le cadre de la gestion de la persistance de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7e76c-111">An object that uses a picture object internally would normally save and load the picture as part of the object's own persistence handling.</span></span> <span data-ttu-id="7e76c-112">La fonction [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifie la création d’un objet image basé sur le contenu du flux.</span><span class="sxs-lookup"><span data-stu-id="7e76c-112">The [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) function simplifies the creation of a picture object based on stream contents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7e76c-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7e76c-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7e76c-114">Propriétés du contrôle</span><span class="sxs-lookup"><span data-stu-id="7e76c-114">Control Properties</span></span>](control-properties.md)
</dt> </dl>

 

 