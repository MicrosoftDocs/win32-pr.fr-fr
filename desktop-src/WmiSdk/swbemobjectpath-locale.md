---
description: La propriété locale de l’objet SWbemObjectPath contient les paramètres régionaux du chemin d’accès à l’objet.
ms.assetid: cde4ebac-b112-48b5-a274-802e6d3fbfbf
ms.tgt_platform: multiple
title: Propriété SWbemObjectPath. locale (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Locale
- ISWbemObjectPath.Locale
- ISWbemObjectPath.get_Locale
- ISWbemObjectPath.put_Locale
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: eb9d2641aa92a4771867eef5cdd2b76d2729c3ea35a32e46d68212bf683bf2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119503899"
---
# <a name="swbemobjectpathlocale-property"></a>Propriété SWbemObjectPath. locale

La propriété **locale** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) contient les paramètres régionaux du chemin d’accès à l’objet.

Lorsque la propriété **SWbemObjectPath. locale** fait partie d’un objet [**SWbemObjectPath**](swbemobjectpath.md) autonome, elle est en lecture/écriture et peut être utilisée pour définir le composant de paramètres régionaux du moniker.

Lorsque la propriété **SWbemObjectPath. locale** est accessible dans le cadre d’une propriété [**SWbemObject. \_ path**](swbemobject-path-.md) , elle est en lecture seule et signale la valeur des paramètres régionaux utilisés dans la liaison à l’espace de noms à partir duquel l’objet a été obtenu.

Pour les identificateurs de paramètres régionaux Microsoft, le format de la chaîne est « MS \_ xxxx », où xxxx est une chaîne au format hexadécimal qui indique le LCID. Par exemple, l’identificateur de paramètres régionaux anglais américain est « MS \_ 409 ».

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectPath.Locale As String
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



 

 




