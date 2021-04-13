---
title: RegistrationInfo. URI, propriété
description: Pour les scripts, obtient ou définit l’URI de la tâche.
ms.assetid: 49085ee4-65e1-412c-ac1c-9c0f9efe5679
keywords:
- Planificateur de tâches de propriété URI
- Propriété URI Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété URI
topic_type:
- apiref
api_name:
- RegistrationInfo.URI
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77598d556fdec29f41004529471c8098314a6faf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509053"
---
# <a name="registrationinfouri-property"></a>RegistrationInfo. URI, propriété

Pour les scripts, obtient ou définit l’URI de la tâche.

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.URI As String
```



## <a name="property-value"></a>Valeur de la propriété

URI de la tâche.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’URI de tâche est spécifié à l’aide de l’élément [**URI**](taskschedulerschema-uri-registrationinfotype-element.md) du schéma planificateur de tâches.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





