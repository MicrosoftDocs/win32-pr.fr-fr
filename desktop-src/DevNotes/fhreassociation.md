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
ms.openlocfilehash: f4b8cb55ce4b374f7f17f16044811a930623fc777a028ee98b5d8726bf714cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538509"
---
# <a name="fhreassociation-class"></a>FhReassociation, classe

Représente la fonctionnalité de réassociation de l’historique des fichiers, qui permet à un utilisateur de rétablir une relation avec une cible de sauvegarde qui a été utilisée par le même utilisateur dans le passé. La réassociation est effectuée en appelant les méthodes de l’interface [**IFhReassociation**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Quand implémenter

L’API d’historique des fichiers implémente cette classe. Pour créer une instance de cette classe, utilisez la fonction [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Fhcfg. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Fhcfg. idl</dt> </dl> |



 

 
