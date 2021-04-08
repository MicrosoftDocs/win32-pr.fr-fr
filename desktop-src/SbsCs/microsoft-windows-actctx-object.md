---
description: L’objet Microsoft. Windows. ActCtx fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte. L’objet Microsoft. Windows. ActCtx peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Objet Microsoft. Windows. ActCtx
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Microsoft.Windows.ActCtx
api_type:
- COM
api_location: ''
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864213"
---
# <a name="microsoftwindowsactctx-object"></a>Objet Microsoft. Windows. ActCtx

L’objet **Microsoft. Windows. ActCtx** fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte. L’objet **Microsoft. Windows. ActCtx** peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants com.

L’objet **Microsoft. Windows. ActCtx** est fourni sous la forme d’un assembly dans Windows Server 2003. Il peut également être installé par les applications qui utilisent le Windows Installer pour l’installation et l’inclure en tant que module de fusion dans son package d’installation.

## <a name="members"></a>Membres

L’objet **Microsoft. Windows. ActCtx** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Microsoft. Windows. ActCtx** possède les méthodes suivantes.



| Méthode                               | Description                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | Crée un objet dans le contexte du manifeste actuel.<br/>            |
| [**GetObject**](getobject.md)       | Obtient une instance d’un objet **Microsoft. Windows. ActCtx** existant.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **Microsoft. Windows. ActCtx** possède les propriétés suivantes.



| Propriété                                | Type d’accès          | Description                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Du**](manifest.md)<br/> | Lecture seule<br/> | Obtient le contexte d’activation actif.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/> |



 

 




