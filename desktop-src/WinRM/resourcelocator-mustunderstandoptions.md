---
title: ResourceLocator. MustUnderstandOptions, propriété (WSManDisp. h)
description: Obtient ou définit la valeur MustUnderstandOptions de l’objet ResourceLocator.
ms.assetid: d366696c-9128-4cbd-98d0-6c2d16c75d59
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la propriété MustUnderstandOptions
- Windows Remote Management de la propriété MustUnderstandOptions, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, propriété MustUnderstandOptions
topic_type:
- apiref
api_name:
- ResourceLocator.MustUnderstandOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2945efd1a224c333f45956a29df779efc98e944f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942711"
---
# <a name="resourcelocatormustunderstandoptions-property"></a>ResourceLocator. MustUnderstandOptions, propriété

Obtient ou définit la valeur **MustUnderstandOptions** de l’objet [**ResourceLocator**](resourcelocator.md) . Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.MustUnderstandOptions As boolean
```



## <a name="property-value"></a>Valeur de la propriété

Indique, lorsque la **valeur est true**, que le service qui implémente l' [protocole WS-Management](ws-management-protocol.md) doit retourner une erreur s’il ne peut pas traiter l’option.

## <a name="remarks"></a>Notes

**IWSManResourceLocator :: MustUnderstandOptions** est la propriété C++ correspondante.

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

[**ResourceLocator**](resourcelocator.md)
</dt> </dl>

 

 





