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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515467"
---
# <a name="iwiapreviewclear-method"></a>IWiaPreview :: Clear, méthode

Libère l’image non filtrée mise en cache par la méthode [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md) . Il libère également le filtre de traitement d’image.

## <a name="syntax"></a>Syntaxe


```C++
void Clear();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Sur **IWiaPreview :: Clear** le composant WIA (Windows Image Acquisition) 2,0 Preview libère tous les pointeurs d’interface qu’il stocke. Le composant d’aperçu WIA 2,0 conserve les références à *pWiaItem2* et *PWiaTransferCallback* passées dans [**IWiaPreview :: GetNewPreview**](-wia-iwiapreview-getnewpreview.md). Pour être précis, le composant WIA 2,0 Preview conserve une référence à *pWiaItem2* et le filtre de traitement d’image du pilote, qui à son tour conserve une référence à *pWiaTransferCallback*. Sur **IWiaPreview :: Clear**, le composant WIA 2,0 Preview libère également sa référence à *pWiaItem2* et au filtre de traitement d’image, qui à son tour libère sa référence à *pWiaTransferCallback*. Le composant d’aperçu WIA 2,0 supprime l’image mise en cache et non filtrée qu’elle stocke en interne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




