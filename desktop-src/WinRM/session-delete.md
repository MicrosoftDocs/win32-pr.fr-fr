---
title: Session. Delete, méthode (WSManDisp. h)
description: Supprime la ressource spécifiée dans l’URI de ressource.
ms.assetid: 8803d35d-674c-483d-866b-37129102c7ce
ms.tgt_platform: multiple
keywords:
- supprimer la méthode Windows Remote Management
- Delete, méthode Windows Remote Management, objet Session
- Windows Remote Management d’objet de Session, méthode Delete
topic_type:
- apiref
api_name:
- Session.Delete
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 769ef3f462fa542e9afc6859b564e1a32ed87578894df4008fb6a19ad8aadad8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858669"
---
# <a name="sessiondelete-method"></a>Session. Delete, méthode

Supprime la ressource spécifiée dans l’URI de ressource.

## <a name="syntax"></a>Syntaxe


```VB
Session.Delete( _
  ByVal resourceUri, _
  [ ByVal flags ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*resourceuri* \[ dans\]
</dt> <dd>

URI de la ressource à supprimer. Vous pouvez également utiliser un objet [**ResourceLocator**](resourcelocator.md) pour spécifier la ressource.

</dd> <dt>

*indicateurs* \[ dans, facultatif\]
</dt> <dd>

Réservé pour un usage futur. Doit avoir la valeur 0.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

La syntaxe suivante est utilisée pour appeler cette méthode.


```VB
session.Delete("<resourceUri>")
```



## <a name="examples"></a>Exemples

L’exemple de code VBScript suivant supprime les écouteurs configurés pour le transport HTTP.


```VB
Set objWsman = CreateObject( "WSMan.Automation" )
Set objSession = objWsman.CreateSession
strResource = "http://schemas.microsoft.com/wbem/wsman/1/" &_
  "config/Listener?Address=*+Transport=HTTP"
objSession.Delete(strResource)
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

[**session**](session.md)
</dt> </dl>

 

 





