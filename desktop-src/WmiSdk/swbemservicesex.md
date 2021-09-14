---
description: Étend les fonctionnalités de SWbemServices.
ms.assetid: def514a9-eca4-41de-87cd-c9f964a71f68
ms.tgt_platform: multiple
title: Objet SWbemServicesEx (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemServicesEx
- ISWbemServicesEx
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8ed41cbab38e24958705c24aefc9ea5e9e67357e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403958"
---
# <a name="swbemservicesex-object"></a>Objet SWbemServicesEx

L’objet **SWbemServicesEx** étend les fonctionnalités de [**SWbemServices**](swbemservices.md). Les méthodes [**put**](swbemservicesex-put.md) et [**PutAsync**](swbemservicesex-putasync.md) permettent d’enregistrer une classe ou une instance dans plusieurs espaces de noms ou dans un espace de noms différent de celui dans lequel une instance a été créée. Cet objet ne peut pas être créé par l’appel VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) .

## <a name="members"></a>Membres

L’objet **SWbemServicesEx** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’objet **SWbemServicesEx** a ces méthodes.



| Méthode                                       | Description                                                                                                                                                                                                               |
|:---------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Posé**](swbemservicesex-put.md)           | Enregistre l’objet dans l’espace de noms lié à l’objet **SWbemServicesEx** et retourne un objet [**SWbemObjectPath**](swbemobjectpath.md) qui contient le chemin d’accès de l’objet dans lequel les données ont été écrites.<br/> |
| [**PutAsync**](swbemservicesex-putasync.md) | Enregistre un objet de façon asynchrone dans un espace de noms.<br/>                                                                                                                                                                 |



 

## <a name="remarks"></a>Notes

Les méthodes de cette classe peuvent être appelées en mode semi-synchrone ou en mode asynchrone. Pour plus d’informations, consultez [appel d’une méthode](calling-a-method.md).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ ISWbemServicesEx<br/>                                                      |
| IID<br/>                      | IID \_ ISWbemServicesEx<br/>                                                        |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> <dt>

[Appel d’une méthode](calling-a-method.md)
</dt> </dl>

 

