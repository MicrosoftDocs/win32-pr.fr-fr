---
title: Propriété Principal.Id
description: Pour les scripts, obtient ou définit l’identificateur du principal.
ms.assetid: 54112977-9c30-4c52-bffd-7625eeb79f82
keywords:
- Propriété ID Planificateur de tâches
- ID de propriété Planificateur de tâches, objet principal
- Planificateur de tâches de l’objet principal, propriété ID
topic_type:
- apiref
api_name:
- Principal.Id
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fb3561bb5266a649dc230f84b9e35e68e005d0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385008"
---
# <a name="principalid-property"></a>Propriété Principal.Id

Pour les scripts, obtient ou définit l’identificateur du principal.

## <a name="syntax"></a>Syntaxe


```VB
Principal.Id As String
```



## <a name="property-value"></a>Valeur de la propriété

Identificateur du principal.

## <a name="remarks"></a>Notes

Cet identificateur est également utilisé lors de la spécification de la propriété [**ActionCollection. Context**](actioncollection-context.md) .

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’identificateur de l’entité de sécurité est spécifié dans l’attribut ID de l’élément [**principal**](taskschedulerschema-principal-principaltype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**ActionCollection. Context**](actioncollection-context.md)
</dt> <dt>

[**Directeur**](principal.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





