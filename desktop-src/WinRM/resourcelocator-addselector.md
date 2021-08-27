---
title: Méthode ResourceLocator. AddSelector (WSManDisp. h)
description: Ajoute un sélecteur à l’objet ResourceLocator. Le sélecteur spécifie une instance particulière d’une ressource.
ms.assetid: 4b513d39-a377-487f-a03b-f3c5ab0f0b5a
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode AddSelector
- méthode AddSelector Windows Remote Management, objet ResourceLocator
- Windows Remote Management objet ResourceLocator, méthode AddSelector
topic_type:
- apiref
api_name:
- ResourceLocator.AddSelector
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fc59aab6e5194716fa3b0cda98bb874d0045011c0159c5caaa3cbd53e7fbfd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121639"
---
# <a name="resourcelocatoraddselector-method"></a>Méthode ResourceLocator. AddSelector

Ajoute un [*Sélecteur*](windows-remote-management-glossary.md) à l’objet [**ResourceLocator**](resourcelocator.md) . Le sélecteur spécifie une instance particulière d’une *ressource*. Vous pouvez fournir un objet [**ResourceLocator**](resourcelocator.md) au lieu de spécifier un URI de ressource dans les opérations d’objet de [**session**](session.md) , telles que [**session. obtenir**](session-get.md), [**session. put**](session-put.md)ou [**session. Enumerate**](session-enumerate.md).

## <a name="syntax"></a>Syntaxe


```VB
ResourceLocator.AddSelector( _
  ByVal resourceSelName, _
  ByVal selValue _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceSelName* \[ dans\]
</dt> <dd>

Nom du sélecteur. Par exemple, lors de la demande de données WMI, ce paramètre est la propriété de clé pour une classe WMI.

</dd> <dt>

*selValue* \[ dans\]
</dt> <dd>

Valeur du sélecteur. Par exemple, pour les données WMI, ce paramètre contient une valeur pour une propriété de clé qui identifie une instance spécifique.

</dd> </dl>

## <a name="remarks"></a>Remarques

**IWSManResourceLocator :: AddSelector** est la méthode C++ correspondante.

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

 

 





