---
description: La propriété de sécurité de l’objet SWbemObjectPath est utilisée pour récupérer ou définir les composants de sécurité d’un chemin d’accès d’objet.
ms.assetid: 26e5e990-3b78-41b6-83c4-ba0d8b0d2f00
ms.tgt_platform: multiple
title: SWbemObjectPath.Security_, propriété (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemObjectPath.Security_
- ISWbemObjectPath.Security_
- ISWbemObjectPath.get_Security_
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 000f3f5e334ef0eba3dbd687d7bdc4b594442305
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918708"
---
# <a name="swbemobjectpathsecurity_-property"></a>SWbemObjectPath. Security, \_ propriété

La propriété de **sécurité** de l’objet [**SWbemObjectPath**](swbemobjectpath.md) est utilisée pour récupérer ou définir les composants de sécurité d’un chemin d’accès d’objet. Notez qu’il n’est pas utilisé pour définir des attributs de sécurité de l’objet **SWbemObjectPath** lui-même. Il est utilisé uniquement pour représenter les composants de sécurité du chemin d’accès pour un objet [**SWbemLocator**](swbemlocator.md) . Cette propriété est un objet [**SWbemSecurity**](swbemsecurity.md) .

> [!Note]  
> La définition de la propriété de [**sécurité \_**](swbemobject-security-.md) d’un objet [**SWbemObjectPath**](swbemobjectset.md) sur la **valeur null** accorde à tout moment un accès illimité à tous les utilisateurs. Pour plus d’informations, consultez [**SWbemSecurity**](swbemsecurity.md).

 

Pour plus d’informations, consultez [conventions de document pour l’API de script](document-conventions-for-the-scripting-api.md).

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```VB
SWbemObjectPath.Security_ As Object
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemObjectPath<br/>                                                       |
| IID<br/>                      | IID \_ ISWbemObjectPath<br/>                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SWbemObjectPath**](swbemobjectpath.md)
</dt> <dt>

[Création d’une application ou d’un script WMI](creating-a-wmi-application-or-script.md)
</dt> <dt>

[Définition de la sécurité des processus d' \_ application cliente \_](setting-client-application-process-security.md)
</dt> </dl>

 

 




