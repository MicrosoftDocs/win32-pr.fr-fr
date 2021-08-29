---
description: La \_ propriété de sécurité de l’objet SWbemObjectSet est utilisée pour obtenir ou définir les paramètres de sécurité d’un objet SWbemObjectSet. Cette propriété est un objet SWbemSecurity.
ms.assetid: ee2ad6d5-c0aa-4510-ba1b-4a152d56011f
ms.tgt_platform: multiple
title: SWbemObjectSet.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectSet.Security_
- ISWbemObjectSet.Security_
- ISWbemObjectSet.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 7e0725fc6aa35043a3a40220b1fb43a3624cfd6ef5b55775adf5f41d26fafe85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857209"
---
# <a name="swbemobjectsetsecurity_-property"></a>Propriété SWbemObjectSet. Security \_

La propriété de **\_ sécurité** de l’objet [**SWbemObjectSet**](swbemobjectset.md) est utilisée pour obtenir ou définir les paramètres de sécurité d’un objet **SWbemObjectSet** . Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> La définition de la propriété de [**\_ sécurité**](swbemobject-security-.md) d’un objet [**SWbemObjectSet**](swbemobjectset.md) sur **null** accorde à tout moment un accès illimité à tous les utilisateurs. Pour plus d’informations sur les implications d’un accès illimité, consultez [**SWbemSecurity**](swbemsecurity.md).

 

Pour une explication de cette syntaxe, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectSet.Security_ As Object
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
| CLSID<br/>                    | CLSID \_ SWbemObjectSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemObjectSet<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemObjectSet**](swbemobjectset.md)
</dt> <dt>

[Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Sécurisation des clients de script](securing-scripting-clients.md)
</dt> </dl>

 

 




