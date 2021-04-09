---
title: Méthode WSMan. CreateConnectionOptions (WSManDisp. h)
description: Crée un objet ConnectionOptions qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session.
ms.assetid: 3669a5fe-8305-4fa3-aa75-fafefcd8b33d
ms.tgt_platform: multiple
keywords:
- Windows Remote Management de la méthode CreateConnectionOptions
- Méthode CreateConnectionOptions Windows Remote Management, objet WSMan
- Objet WSMan Windows Remote Management, méthode CreateConnectionOptions
topic_type:
- apiref
api_name:
- WSMan.CreateConnectionOptions
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e051b65e7ab85f11d6a10b94573082da8823ce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843313"
---
# <a name="wsmancreateconnectionoptions-method"></a>Méthode WSMan. CreateConnectionOptions

Crée un objet [**ConnectionOptions**](connectionoptions.md) qui spécifie le nom d’utilisateur et le mot de passe utilisés lors de la création d’une session.

## <a name="syntax"></a>Syntaxe


```VB
WSMan.CreateConnectionOptions()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Objet [**ConnectionOptions**](connectionoptions.md) utilisé pour spécifier une paire nom d’utilisateur/mot de passe utilisée pour identifier un utilisateur à des fins d’authentification.

## <a name="remarks"></a>Notes

La syntaxe suivante est utilisée pour appeler cette méthode.


```VB
Set options = wsman.CreateConnectionOptions
```



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
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> </dl>

 

 





