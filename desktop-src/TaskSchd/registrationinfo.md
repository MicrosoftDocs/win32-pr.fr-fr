---
title: Objet RegistrationInfo
description: Objet de script qui fournit les informations d’administration qui peuvent être utilisées pour décrire la tâche.
ms.assetid: 3d5a5545-5adc-4361-9ce8-fffd35ff6df7
keywords:
- informations d’inscription Planificateur de tâches, objet
- Objet RegistrationInfo Planificateur de tâches
- Planificateur de tâches d’objets RegistrationInfo, Description
topic_type:
- apiref
api_name:
- RegistrationInfo
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f85bb423ae27a3d0b0b15f7b04d287a749f4fe23f3a4b58f7c2462b487b8a705
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072649"
---
# <a name="registrationinfo-object"></a>Objet RegistrationInfo

Objet de script qui fournit les informations d’administration qui peuvent être utilisées pour décrire la tâche. Ces informations incluent des détails tels que la description de la tâche, l’auteur de la tâche, la date à laquelle la tâche est inscrite et le descripteur de sécurité de la tâche.

## <a name="members"></a>Membres

L’objet **RegistrationInfo** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’objet **RegistrationInfo** a ces propriétés.



| Propriété                                                                     | Type d’accès           | Description                                                                                                                                |
|:-----------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [**Auteur**](registrationinfo-author.md)<br/>                         | Lecture/écriture<br/> | Obtient ou définit l’auteur de la tâche.<br/>                                                                                            |
| [**Date**](registrationinfo-date.md)<br/>                             | Lecture/écriture<br/> | Obtient ou définit la date et l’heure d’enregistrement de la tâche.<br/>                                                                     |
| [**Description**](registrationinfo-description.md)<br/>               | Lecture/écriture<br/> | Obtient ou définit la description de la tâche.<br/>                                                                                       |
| [**Documentation**](registrationinfo-documentation.md)<br/>           | Lecture/écriture<br/> | Obtient ou définit toute documentation supplémentaire pour la tâche.<br/>                                                                         |
| [**SecurityDescriptor**](registrationinfo-securitydescriptor.md)<br/> |                       | Obtient ou définit le descripteur de sécurité de la tâche.<br/>                                                                               |
| [**Source**](registrationinfo-source.md)<br/>                         | Lecture/écriture<br/> | Obtient ou définit l’origine de la tâche. Par exemple, une tâche peut provenir d’un composant, d’un service, d’une application ou d’un utilisateur.<br/> |
| [**URI**](registrationinfo-uri.md)<br/>                               | Lecture/écriture<br/> | Obtient ou définit l’URI de la tâche.<br/>                                                                                               |
| [**Version**](registrationinfo-version.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit le numéro de version de la tâche.<br/>                                                                                    |
| [**XmlText**](registrationinfo-xmltext.md)<br/>                       | Lecture/écriture<br/> | Obtient ou définit une version au format XML des informations d’inscription pour la tâche.<br/>                                             |



 

## <a name="remarks"></a>Remarques

Les informations d’inscription peuvent être utilisées pour identifier une tâche par le biais de l’interface utilisateur Planificateur de tâches, ou en tant que critères de recherche lors de l’énumération des tâches inscrites.

Lors de la lecture ou de l’écriture de données XML pour une tâche, les informations d’inscription de la tâche sont spécifiées dans l’élément [**RegistrationInfo**](taskschedulerschema-registrationinfo-tasktype-element.md) du schéma planificateur de tâches.

## <a name="examples"></a>Exemples

Pour plus d’informations et pour obtenir un exemple de code pour cet objet de script, consultez [exemple de déclenchement temporel (script)](time-trigger-example--scripting-.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                    |
| Bibliothèque de types<br/>             | <dl> <dt>Taskschd. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



 

 





