---
description: L’objet RecordList est une collection d’objets record. Vous devez vérifier que l’objet RecordList existe et qu’il n’est pas vide avant de référencer ses propriétés.
ms.assetid: 7f5ac153-8da1-4dc8-9bb7-defd4e821142
title: Objet RecordList
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecordList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b3f09887333d8ddbf83de4bea2b2e654411883e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009711"
---
# <a name="recordlist-object"></a>Objet RecordList

L’objet **RecordList** est une collection d’objets [**Record**](record-object.md) . Vous devez vérifier que l’objet **RecordList** existe et qu’il n’est pas vide avant de référencer ses propriétés.

## <a name="members"></a>Membres

L’objet **RecordList** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **RecordList** a ces propriétés.



| Propriété                                     | Description                                                          |
|:---------------------------------------------|:---------------------------------------------------------------------|
| [**Saut**](recordlist-count.md)<br/> | Retourne le nombre d’éléments dans l’objet **RecordList** .<br/> |
| [**Élément**](recordlist-item.md)<br/>   | Retourne un enregistrement dans une collection d’objets **RecordList** .<br/>   |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IRecordList est défini en tant que 000C1096-0000-0000-C000-000000000046<br/>                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Enregistrement**](record-object.md)
</dt> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




