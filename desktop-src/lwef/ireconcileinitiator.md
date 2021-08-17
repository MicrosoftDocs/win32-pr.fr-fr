---
title: Interface IReconcileInitiator
description: Expose des méthodes qui fournissent le réconciliateur de porte-documents avec le moyen d’informer l’initiateur de sa progression, de définir un objet de fin et de demander une version donnée d’un document. L’initiateur est responsable de l’implémentation de cette interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator
- fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator, description
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff81862e5ff0b27b75f952749957e6559306257240f2a02aca5f34e3efc870cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749139"
---
# <a name="ireconcileinitiator-interface"></a>Interface IReconcileInitiator

Expose des méthodes qui fournissent le réconciliateur de porte-documents avec le moyen d’informer l’initiateur de sa progression, de définir un objet de fin et de demander une version donnée d’un document. L’initiateur est responsable de l’implémentation de cette interface.

## <a name="members"></a>Membres

L’interface **IReconcileInitiator** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IReconcileInitiator** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IReconcileInitiator** possède ces méthodes.



| Méthode                                                                 | Description                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetAbortCallback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | Définit l’objet par le biais duquel l’initiateur peut arrêter de manière asynchrone un rapprochement. Un réconciliateur de porte-documents définit généralement cet objet pour les réconciliations qui sont longues ou qui impliquent une interaction avec l’utilisateur. <br/>                                                                                              |
| [**SetProgressFeedback**](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | Indique la progression du réconciliateur de porte-documents sur la réalisation du rapprochement. Le montant est une fraction et est calculé comme le quotient des paramètres *ulProgress* et *ulProgressMax* . Les réviseurs doivent appeler cette méthode périodiquement au cours de leur processus de rapprochement. <br/> |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,0 ou ultérieure)</dt> </dl> |



 

