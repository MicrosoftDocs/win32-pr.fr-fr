---
title: RegistrationInfo. Author, propriété
description: Pour les scripts, obtient ou définit l’auteur de la tâche.
ms.assetid: ba355a3b-cda3-4d4f-8504-f77f3d9eb21a
keywords:
- Planificateur de tâches de propriété auteur
- Propriété Author Planificateur de tâches, objet RegistrationInfo
- Objet RegistrationInfo Planificateur de tâches, propriété Author
topic_type:
- apiref
api_name:
- RegistrationInfo.Author
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e7e940ff9da2cfccaa306ebf73080da2a28a091
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032310"
---
# <a name="registrationinfoauthor-property"></a>RegistrationInfo. Author, propriété

Pour les scripts, obtient ou définit l’auteur de la tâche.

## <a name="syntax"></a>Syntaxe


```VB
RegistrationInfo.Author As String
```



## <a name="property-value"></a>Valeur de la propriété

Auteur de la tâche.

## <a name="remarks"></a>Notes

Lors de la lecture ou de l’écriture de données XML pour une tâche, l’auteur de la tâche est spécifié à l’aide de l’élément [**Author**](taskschedulerschema-author-registrationinfotype-element.md) du schéma planificateur de tâches.

Lors de la définition de cette valeur de propriété, la valeur peut être un texte récupéré à partir d’un fichier Resource. dll. Une chaîne spécialisée est utilisée pour référencer le texte à partir du fichier de ressources. Le format de la chaîne est $ (@ \[ dll \] , \[ ResourceId \] ), où \[ dll \] est le chemin d’accès au fichier. dll qui contient la ressource et \[ ResourceId \] est l’identificateur du texte de la ressource. Par exemple, si vous affectez la valeur $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) à cette propriété, vous affectez à la propriété la valeur du texte de la ressource avec un identificateur égal à-101 dans le fichier% systemroot% \\ system32 \\ResourceName.dll.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 





