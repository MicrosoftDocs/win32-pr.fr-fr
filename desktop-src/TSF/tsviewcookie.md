---
title: TsViewCookie (Textstor. h)
description: Le type de données TsViewCookie identifie un affichage de contexte.
ms.assetid: e649b799-d0d6-4f2d-b9f1-28070eea9b16
keywords:
- TsViewCookie
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb43f888f76410e83e89d037f39ea665ca548ec9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511546"
---
# <a name="tsviewcookie"></a>TsViewCookie

Le type de données **TsViewCookie** identifie un affichage de contexte.


```C++
typedef DWORD TsViewCookie;
```



## <a name="remarks"></a>Notes

Une application doit fournir une valeur **TsViewCookie** unique pour chaque vue qu’elle crée.

Le gestionnaire TSF obtient cette valeur à partir de l’application en appelant [ITextStoreACP :: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview) ou [ITextStoreAnchor :: GetActiveView](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview). Le gestionnaire TSF utilise cette valeur pour identifier la vue lors de l’appel de différentes méthodes [ITextStoreACP](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp) ou [ITextStoreAnchor](/windows/desktop/api/Textstor/nn-textstor-itextstoreanchor) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                             |
| Composant redistribuable<br/>          | TSF 1,0 sur Windows 2000 professionnel<br/>                                         |
| En-tête<br/>                   | <dl> <dt>Textstor. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Textstor. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ITextStoreACP**](/windows/desktop/api/Textstor/nn-textstor-itextstoreacp)
</dt> <dt>

[**ITextStoreACP :: GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreacp-getactiveview)
</dt> <dt>

[**ITextStoreAnchor::GetActiveView**](/windows/desktop/api/Textstor/nf-textstor-itextstoreanchor-getactiveview)
</dt> </dl>

 

 





