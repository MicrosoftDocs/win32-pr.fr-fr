---
title: Méthode ResourceLocator. ClearOptions (WSManDisp. h)
description: Supprime toutes les options de l’objet ResourceLocator.
ms.assetid: 1b4d7f15-c56f-4b0d-9614-8376012abca7
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode ClearOptions
- méthode ClearOptions Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode ClearOptions
topic_type:
- apiref
api_name:
- ResourceLocator.ClearOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef695b949c62c0d56de45914e1a54996d4d7599f029d136ad78b03ac687365aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118112910"
---
# <a name="resourcelocatorclearoptions-method"></a>Méthode ResourceLocator. ClearOptions

Supprime toutes les [*options*](windows-remote-management-glossary.md) de l’objet [**ResourceLocator**](resourcelocator.md) . Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.ClearOptions()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="remarks"></a>Remarques

**IWSManResourceLocator :: ClearOptions** est la méthode C++ correspondante.

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

 

 





