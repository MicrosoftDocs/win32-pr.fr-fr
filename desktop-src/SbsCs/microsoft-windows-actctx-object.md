---
description: Microsoft. Windows. L’objet ActCtx fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte. Microsoft. Windows. L’objet ActCtx peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants COM.
ms.assetid: 818e175e-2c58-4c44-87ce-4e97352fc3f3
title: Librairie. Windows. Objet ActCtx
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
ms.openlocfilehash: 7e84eadbc7489ddd91c34c0c9494515e89205849829625e850ad31dce3e92fc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142002"
---
# <a name="microsoftwindowsactctx-object"></a>Librairie. Windows. Objet ActCtx

**Microsoft. Windows.** L’objet ActCtx fait référence aux manifestes et permet aux moteurs de script d’accéder aux assemblys côte à côte. **Microsoft. Windows.** L’objet ActCtx peut être utilisé pour créer une instance d’un assembly côte à côte avec des composants com.

**Microsoft. Windows.** l’objet ActCtx est fourni en tant qu’assembly dans Windows Server 2003. il peut également être installé par les applications qui utilisent le Windows Installer pour l’installation et l’inclure en tant que module de fusion dans son package d’installation.

## <a name="members"></a>Membres

**Microsoft. Windows.** L’objet ActCtx possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

**Microsoft. Windows.** L’objet ActCtx possède ces méthodes.



| Méthode                               | Description                                                                     |
|:-------------------------------------|:--------------------------------------------------------------------------------|
| [**CreateObject**](createobject.md) | Crée un objet dans le contexte du manifeste actuel.<br/>            |
| [**GetObject**](getobject.md)       | Obtient une instance d’un **Microsoft. Windows existant. Objet ActCtx** .<br/> |



 

### <a name="properties"></a>Propriétés

**Microsoft. Windows.** L’objet ActCtx a ces propriétés.



| Propriété                                | Type d’accès          | Description                                    |
|:----------------------------------------|:---------------------|:-----------------------------------------------|
| [**Du**](manifest.md)<br/> | Lecture seule<br/> | Obtient le contexte d’activation actif.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 




