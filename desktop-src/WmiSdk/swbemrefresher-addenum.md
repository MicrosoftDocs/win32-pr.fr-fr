---
description: Ajoute un nouvel énumérateur à l’objet SWbemRefresher. Cet énumérateur concerne toutes les instances de la classe qui est spécifiée dans le paramètre strClass.
ms.assetid: 0fa22a47-4050-43ae-aad3-3a8ebbf5e9b2
ms.tgt_platform: multiple
title: Méthode SWbemRefresher. AddEnum (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
- ISWbemRefresher.AddEnum
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: cffa406a3a45869038f5e6fed12b23b6b84fde27
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761401"
---
# <a name="swbemrefresheraddenum-method"></a>Méthode SWbemRefresher. AddEnum

La méthode **SWbemRefresher. AddEnum** ajoute un nouvel énumérateur à l’objet [**SWbemRefresher**](swbemrefresher.md) . Cet énumérateur concerne toutes les instances de la classe qui est spécifiée dans le paramètre *strClass* .

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Syntaxe


```VB
objRefreshEnum = .AddEnum( _
  ByVal objWbemService, _
  ByVal strClass, _
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

*strClass* 
</dt> <dd>

Obligatoire. Chaîne qui contient la classe ajoutée à l’actualisateur. Cette classe est utilisée comme un énumérateur des instances de la classe. La propriété d' [**index**](swbemrefreshableitem-index.md) de la [**SWbemRefreshableItem**](swbemrefreshableitem.md) retournée représente l’index de l’énumérateur dans la collection d’actualisations.

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

Si l’appel réussit, un objet [**SWbemRefreshableItem**](swbemrefreshableitem.md) qui contient un énumérateur pour toutes les instances de la classe spécifiée est retourné.

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

 

 




