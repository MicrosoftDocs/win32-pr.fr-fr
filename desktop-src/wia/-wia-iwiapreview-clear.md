---
description: 'Libère l’image non filtrée mise en cache par la méthode IWiaPreview :: GetNewPreview. Il libère également le filtre de traitement d’image.'
ms.assetid: af94d27f-9d93-40e1-8d1a-e5546531a176
title: 'IWiaPreview :: Clear, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaPreview.Clear
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 1ac2cc1f12cf6fd59111d0159684459c2500a854
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295242"
---
# <a name="iwiapreviewclear-method"></a>IWiaPreview :: Clear, méthode

Libère l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Il libère également le filtre de traitement d’image.

## <a name="syntax"></a>Syntaxe


```C++
void Clear();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur de retour

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

sur **IWiaPreview :: Clear** la Windows composant acquisition d’images (WIA) 2,0 Preview libère tous les pointeurs d’interface qu’elle stocke. Le composant d’aperçu WIA 2,0 conserve les références à *pWiaItem2* et *PWiaTransferCallback* passées dans [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Pour être précis, le composant WIA 2,0 Preview conserve une référence à *pWiaItem2* et le filtre de traitement d’image du pilote, qui à son tour conserve une référence à *pWiaTransferCallback*. Sur **IWiaPreview :: Clear**, le composant WIA 2,0 Preview libère également sa référence à *pWiaItem2* et au filtre de traitement d’image, qui à son tour libère sa référence à *pWiaTransferCallback*. Le composant d’aperçu WIA 2,0 supprime l’image mise en cache et non filtrée qu’elle stocke en interne.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




