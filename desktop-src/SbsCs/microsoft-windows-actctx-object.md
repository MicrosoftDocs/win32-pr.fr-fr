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
ms.openlocfilehash: 58290ec9d36d8e8428000422d0e1014335870149
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011350"
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



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>          |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/> |



 

 




