---
title: WSMan. Error, propriété (WSManDisp. h)
description: Obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode WSMan si Windows Remote Management Service n’a pas pu créer un objet de session, un objet ConnectionOptions ou un objet ResourceLocator.
ms.assetid: 72d05ef9-672c-4693-b7c9-6d689858acd4
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de propriétés d’erreur
- Windows Remote Management de propriété Error, objet WSMan
- Objet WSMan Windows Remote Management, propriété Error
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
ms.openlocfilehash: 9f9e7ffd42d67807f2f7b6096a89ed91e3d95af8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103804"
---
# <a name="wsmanerror-property"></a>WSMan. Error, propriété

Obtient des informations supplémentaires sur l’erreur, dans un flux XML, pour l’appel précédent à une méthode [**WSMan**](wsman.md) si Windows Remote Management Service n’a pas pu créer un objet de [**session**](session.md) , un objet [**ConnectionOptions**](connectionoptions.md) ou un objet [**ResourceLocator**](resourcelocator.md) .

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

 

 





