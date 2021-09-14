---
description: Un objet SWbemMethodSet est une collection d’objets SWbemMethod. Les éléments sont récupérés à l’aide de la méthode Item. Pour plus d’informations, consultez accès à une collection. Cet objet ne peut pas être créé par l’appel VBScript CreateObject.
ms.assetid: 0ca2601f-ed40-472e-b4f2-eee750c8c8d1
ms.tgt_platform: multiple
title: Objet SWbemMethodSet (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemMethodSet
- ISWbemMethodSet
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: d47c4dc8335077d6f8568be4b56200558942ac39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918775"
---
# <a name="swbemmethodset-object"></a>Objet SWbemMethodSet

Un objet **SWbemMethodSet** est une collection d’objets [**SWbemMethod**](swbemmethod.md) . Les éléments sont récupérés à l’aide de la méthode [**Item**](swbemmethodset-item.md) . Pour plus d’informations, consultez [accès à une collection](accessing-a-collection.md). Cet objet ne peut pas être créé par l’appel VBScript **CreateObject** .

> [!Note]  
> Dans cette version de l’API, l’accès en écriture aux informations de méthode n’est pas pris en charge. Si vous souhaitez définir des méthodes ou modifier des définitions de méthode existantes, vous pouvez définir les modifications de méthode dans un fichier MOF et soumettre les modifications à l’aide du compilateur MOF. Vous pouvez également utiliser l’API COM WMI.

 

## <a name="members"></a>Membres

L’objet **SWbemMethodSet** possède les types de membres suivants :

-   [Méthodes](#swbemmethodset-object)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SWbemMethodSet** a ces méthodes.



| Méthode                              | Description                                                                                                                                  |
|:------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Élément**](swbemmethodset-item.md) | Récupère un objet [**SWbemMethod**](swbemmethod.md) de la collection. Il s’agit de la méthode Automation par défaut de cet objet.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SWbemMethodSet** a ces propriétés.



| Propriété                                         | Type d’accès          | Description                                       |
|:-------------------------------------------------|:---------------------|:--------------------------------------------------|
| [**Count**](swbemmethodset-count.md)<br/> | Lecture seule<br/> | Nombre d’éléments dans la collection<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Bibliothèque de types<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ SWbemMethodSet<br/>                                                        |
| IID<br/>                      | IID \_ ISWbemMethodSet<br/>                                                         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Scripts d’objets d’API](scripting-api-objects.md)
</dt> </dl>

 

 




