---
description: Représente la fonctionnalité de réassociation de l’historique des fichiers, qui permet à un utilisateur de rétablir une relation avec une cible de sauvegarde qui a été utilisée par le même utilisateur dans le passé. La réassociation est effectuée en appelant les méthodes de l’interface IFhReassociation.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: FhReassociation, classe (Fhcfg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 1e303799a792e788fcb948ad6d3c6e2fd732e26e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516377"
---
# <a name="fhreassociation-class"></a>FhReassociation, classe

Représente la fonctionnalité de réassociation de l’historique des fichiers, qui permet à un utilisateur de rétablir une relation avec une cible de sauvegarde qui a été utilisée par le même utilisateur dans le passé. La réassociation est effectuée en appelant les méthodes de l’interface [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Quand implémenter

L’API d’historique des fichiers implémente cette classe. Pour créer une instance de cette classe, utilisez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
