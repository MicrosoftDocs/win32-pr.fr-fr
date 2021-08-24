---
description: Fournit des informations sur une opération d’interruption de l’application.
ms.assetid: B380AEA2-6486-46CC-AD0A-CF25C144DC01
title: Interface ISuspendingOperation (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: f17cd3d3b1eab67d0abfea200e657d8c4a17d8df9e3bb850e4ea361a760d19df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758629"
---
# <a name="isuspendingoperation-interface"></a>Interface ISuspendingOperation

Fournit des informations sur une opération d’interruption de l’application.

## <a name="members"></a>Membres

L’interface **ISuspendingOperation** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingOperation** a également les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’interface **ISuspendingOperation** possède ces méthodes.



| Méthode                                                  | Description                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [**GetDeferral**](isuspendingoperation-getdeferral.md) | Demande que l’opération d’interruption de l’application soit retardée.<br/> |



 

### <a name="properties"></a>Propriétés

L’interface **ISuspendingOperation** possède les propriétés suivantes.



| Propriété                                                     | Type d’accès           | Description                                                                             |
|:-------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------|
| [**Échéance**](isuspendingoperation-deadline.md)<br/> | Lecture/écriture<br/> | Obtient le temps restant avant qu’une opération d’interruption de l’application retardée se poursuive.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| En-tête<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> </dl>

 

 
