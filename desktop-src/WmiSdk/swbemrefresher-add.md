---
description: La méthode SWbemRefresher. Add ajoute un nouvel objet SWbemRefreshableItem à la collection dans l’objet SWbemRefresher. Objet SWbemRefreshableItem à la collection dans l’objet SWbemRefresher.
ms.assetid: 92d11a18-1eed-4958-b74a-2f9de4907dd0
ms.tgt_platform: multiple
title: Méthode SWbemRefresher. Add (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.Add
- ISWbemRefresher.Add
- ISWbemRefresher.Add
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ebe9da221314252b2b143bf674cd7bb7177329b5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "106524769"
---
# <a name="swbemrefresheradd-method"></a>SWbemRefresher. Add, méthode

La méthode **SWbemRefresher. Add** ajoute un nouvel objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) à la collection dans l’objet [**SWbemRefresher**](swbemrefresher.md) .

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objRefreshItem = .Add( _
  ByVal objWbemService, _
  ByVal strInstancePath, _
  [ ByVal iFlags ], _
  [ ByVal objWbemNamedvalueSet ] _
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*objWbemService* 
</dt> <dd>

Obligatoire. Objet [**SWbemServices**](swbemservices.md) qui représente une connexion à l’espace de noms dans lequel réside l’objet ajouté à l’actualisateur.

</dd> <dt>

*strInstancePath* 
</dt> <dd>

Obligatoire. Chaîne qui contient le chemin d’accès relatif de l’objet dans l’espace de noms. Le chemin d’accès doit contenir une instance. La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’objet dans la collection d’actualisations.

</dd> <dt>

*IFlags* \[ facultatif\]
</dt> <dd>

Chaîne qui contient le chemin d’accès de l’objet pour lequel la méthode est exécutée.

</dd> <dt>

*objWbemNamedvalueSet* \[ facultatif\]
</dt> <dd>

En général, ce n’est pas défini. Dans le cas contraire, il s’agit d’un objet [**SWbemNamedValueSet**](swbemnamedvalueset.md) dont les éléments représentent les informations de contexte qui peuvent être utilisées par le fournisseur qui sert la demande. Un fournisseur qui prend en charge ou requiert ces informations doit documenter les noms de valeur reconnus, le type de données de la valeur, les valeurs autorisées et la sémantique.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’appel réussit, un objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) qui contient un objet actualisable unique est retourné.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemRefresher<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemRefresher<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemRefresher**](swbemrefresher.md)
</dt> </dl>

 

 




