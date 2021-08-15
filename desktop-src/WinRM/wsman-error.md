---
title: WSMan. Error, propriété (WSManDisp. h)
description: obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode WSMan si Windows Remote Management service n’a pas pu créer un objet de Session, un objet ConnectionOptions ou un objet ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de propriétés d’erreur
- Windows Remote Management de propriété Error, objet WSMan
- objet WSMan Windows Remote Management, propriété Error
topic_type:
- apiref
api_name:
- WSMan.Error
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14d72c99150d3c6ac95e91e6a9674ab6364e8ea46fabf3d58d50556e129933cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117742194"
---
# <a name="wsmanerror-property"></a>WSMan. Error, propriété

obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode [**WSMan**](wsman.md) si Windows Remote Management service n’a pas pu créer un objet de [**Session**](session.md) , un objet [**ConnectionOptions**](connectionoptions.md) ou un objet [**ResourceLocator**](resourcelocator.md) .

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
WSMan.Error As BSTR
```



## <a name="property-value"></a>Valeur de la propriété

Représentation XML des informations sur l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                 |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                           |
| En-tête<br/>                   | <dl> <dt>WSManDisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WSManDisp. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>WSManDisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WSMan**](wsman.md)
</dt> </dl>

 

 





