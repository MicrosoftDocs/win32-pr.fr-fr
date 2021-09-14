---
description: Le \_ type de données handle SCESVC est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité.
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: SCESVC_HANDLE (scesvc. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011117"
---
# <a name="scesvc_handle"></a>\_handle SCESVC

Le type de données **\_ handle SCESVC** est un handle opaque fourni par le jeu de l’outil de configuration de la sécurité. Elle est utilisée par les méthodes des interfaces [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) et [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) pour transmettre des informations entre le composant logiciel enfichable Configuration de la sécurité et l’extension du composant logiciel enfichable.


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Scesvc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




