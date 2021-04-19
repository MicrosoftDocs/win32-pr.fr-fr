---
description: Gère une opération d’interruption d’application retardée.
ms.assetid: 9F40659E-9B16-4FC9-B320-5679BB8A8161
title: Interface ISuspendingDeferral (Windows. ApplicationModel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingDeferral
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: e4f1801960f2d3b9183550e18fb76378bf4f17f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515854"
---
# <a name="isuspendingdeferral-interface"></a>Interface ISuspendingDeferral

Gère une opération d’interruption d’application retardée.

## <a name="members"></a>Membres

L’interface **ISuspendingDeferral** hérite de [**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable). **ISuspendingDeferral** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ISuspendingDeferral** possède ces méthodes.



| Méthode                                           | Description                                                                                  |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------|
| [**Terminé**](isuspendingdeferral-complete.md) | Indique au système que l’application a enregistré ses données et qu’elle est prête à être suspendue.<br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                                    |
| En-tête<br/>                   | <dl> <dt>Windows. ApplicationModel. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Windows. ApplicationModel. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IInspectable**](/windows/win32/api/inspectable/nn-inspectable-iinspectable)
</dt> <dt>

[**ISuspendingEventArgs**](isuspendingeventargs.md)
</dt> <dt>

[**ISuspendingOperation**](isuspendingoperation.md)
</dt> </dl>

 

 
