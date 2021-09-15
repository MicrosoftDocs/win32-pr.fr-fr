---
description: La propriété reconnexion automatique de l’objet SWbemRefresher est une valeur booléenne qui indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.
ms.assetid: 3be24128-8a35-44b0-befd-8b8937eff1b7
ms.tgt_platform: multiple
title: SWbemRefresher. reconnexion automatique, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemRefresher.AutoReconnect
- ISWbemRefresher.AutoReconnect
- ISWbemRefresher.get_AutoReconnect
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4faa02a4a77409bb8b1813ee433c326d1c45d1bd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518061"
---
# <a name="swbemrefresherautoreconnect-property"></a>SWbemRefresher. reconnexion automatique, propriété

La propriété **reconnexion automatique** de l’objet [**SWbemRefresher**](swbemrefresher.md) est une valeur booléenne qui indique si l’actualisateur se reconnecte automatiquement à un fournisseur distant si la connexion est interrompue.

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemRefresher.AutoReconnect As Boolean
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="remarks"></a>Notes

La modification de cette propriété affecte uniquement les objets de l’actualisateur qui sont sauvegardés par un fournisseur à hautes performances. Si le fournisseur n’est pas un fournisseur à hautes performances, l’affectation de la **valeur true** à la propriété **reconnexion automatique** n’a aucun effet, car l’objet [**SWbemRefresher**](swbemrefresher.md) ne se reconnecte jamais.

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

 

 




