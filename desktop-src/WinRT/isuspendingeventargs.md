---
description: Fournit des données pour un événement d’interruption de l’application.
ms.assetid: 2590AFAA-679C-49F1-804F-D429BB971727
title: Interface ISuspendingEventArgs (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingEventArgs
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 687ecbb056a057338091b21a862816985ed0186a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514021"
---
# <a name="isuspendingeventargs-interface"></a>Interface ISuspendingEventArgs

Fournit des données pour un événement d’interruption de l’application.

## <a name="members"></a>Membres

L’interface **ISuspendingEventArgs** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingEventArgs** a également les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

L’interface **ISuspendingEventArgs** possède les propriétés suivantes.



| Propriété                                                                           | Type d’accès           | Description                                   |
|:-----------------------------------------------------------------------------------|:----------------------|:----------------------------------------------|
| [**SuspendingOperation**](isuspendingeventargs-suspendingoperation.md)<br/> | Lecture/écriture<br/> | Obtient l’opération d’interruption de l’application.<br/> |



 

## <a name="remarks"></a>Notes

Cet objet est accessible quand vous implémentez des gestionnaires d’événements tels que [**SuspendingEventHandler**](/uwp/api/windows.ui.webui.suspendingeventhandler?view=winrt-19041), [**SuspendingEventHandler**](/uwp/api/windows.ui.xaml.suspendingeventhandler?view=winrt-19041)et que vous [**Ajoutez la \_ suspension**](/previous-versions//hh438376(v=vs.85)) pour répondre aux événements d’interruption de l’application.

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

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> <dt>

[**ISuspendingDeferral**](isuspendingdeferral.md)
</dt> </dl>

 

 
