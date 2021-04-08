---
title: Interface IReconcileInitiator
description: Expose des méthodes qui fournissent le réconciliateur de porte-documents avec le moyen d’informer l’initiateur de sa progression, de définir un objet de fin et de demander une version donnée d’un document. L’initiateur est responsable de l’implémentation de cette interface.
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- Fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator
- Fonctionnalités d’environnement Windows héritées de l’interface IReconcileInitiator, Description
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
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741597"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 4,0 ou ultérieure)</dt> </dl> |



 

