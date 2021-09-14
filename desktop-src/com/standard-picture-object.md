---
title: Objet image standard
description: Objet image standard
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221820"
---
# <a name="standard-picture-object"></a>Objet image standard

L’objet image standard fournit une abstraction indépendante du langage pour les images GDI : les bitmaps, les icônes, les reformateurs et les sous-fichiers améliorés. Comme avec l’objet de police standard, le système fournit une implémentation standard de cet objet. Ses interfaces principales sont [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) et [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), ce qui est dérivé de **IDispatch** pour fournir l’accès aux propriétés de l’image par le biais d’OLE Automation. Un objet image est créé avec [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

L’objet image prend également en charge l’interface de l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) pour permettre à un client de déterminer quand les propriétés de l’image changent. En conséquence, l’objet image prend également en charge [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) et un point de connexion pour **IPropertyNotifySink**.

L’objet image prend également en charge [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) de sorte qu’il puisse s’enregistrer et se charger à partir d’une instance de [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Un objet qui utilise un objet image en interne enregistre et charge l’image dans le cadre de la gestion de la persistance de l’objet. La fonction [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) simplifie la création d’un objet image basé sur le contenu du flux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Propriétés du contrôle](control-properties.md)
</dt> </dl>

 

 