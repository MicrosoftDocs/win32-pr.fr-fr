---
title: Propriété RegistrationInfo. Description
description: Pour les scripts, obtient ou définit la description de la tâche.
ms.assetid: bb85fa09-155c-452b-bf6e-28ac4f60cc42
keywords:
- Propriété Description Planificateur de tâches
- Description, propriété Planificateur de tâches, objet RegistrationInfo
- Planificateur de tâches objet RegistrationInfo, propriété Description
topic_type:
- apiref
api_name:
- RegistrationInfo.Description
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea6f141eddc40b21f1cf49e490fe30df5844e6029f821d9811b0e62ea55fa8ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872459"
---
# <a name="registrationinfodescription-property"></a>Propriété RegistrationInfo. Description

Pour les scripts, obtient ou définit la description de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.Description As String
```



## <a name="property-value"></a>Valeur de la propriété

Description de la tâche.

## <a name="remarks"></a>Remarques

Lors de la lecture ou de l’écriture de données XML pour une tâche, la description de la tâche est spécifiée à l’aide de l’élément [**Description**](taskschedulerschema-description-registrationinfotype-element.md) du schéma planificateur de tâches.

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’une ressource .dll fichier. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier .dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





