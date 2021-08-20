---
title: Interface IWMDRMLicenseBackupRestoreStatus
description: L’interface IWMDRMLicenseBackupRestoreStatus fournit une méthode permettant de récupérer des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence. Cette interface est fournie avec les événements de progression générés pendant les opérations de sauvegarde et de restauration de la licence.
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- Format Windows Media de l’interface IWMDRMLicenseBackupRestoreStatus
- Interface IWMDRMLicenseBackupRestoreStatus format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 26583a2911545cd256598025806d238c2f98f84434b4f23d9f13f952bfd15927
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117847038"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a>Interface IWMDRMLicenseBackupRestoreStatus

L’interface **IWMDRMLicenseBackupRestoreStatus** fournit une méthode permettant de récupérer des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.

Cette interface est fournie avec les événements de progression générés pendant les opérations de sauvegarde et de restauration de la licence. Plusieurs événements **MEWMDRMLicenseBackupProgress** sont générés au cours d’une sauvegarde de licence, chacun d’entre eux disposant d’une instance de cette interface. Il en va de même pour les événements **MEWMDRMLicenseRestoreProgress** , générés lors de la restauration de la licence.

Pour récupérer un pointeur vers une instance de l’interface **IWMDRMLicenseBackupRestoreStatus** , vous devez d’abord appeler la méthode **IMFMediaEvent :: GetValue** de l’événement Progress. La valeur récupérée à partir de l’événement est un pointeur vers l’interface **IUnknown** de l’objet qui implémente l’interface **IWMDRMLicenseBackupRestoreStatus** .

## <a name="members"></a>Membres

L’interface **IWMDRMLicenseBackupRestoreStatus** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseBackupRestoreStatus** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMLicenseBackupRestoreStatus** possède ces méthodes.



| Méthode                                                          | Description                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [**GetStatus**](iwmdrmlicensebackuprestorestatus-getstatus.md) | Récupère des informations d’État détaillées sur une opération de sauvegarde ou de restauration de licence.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

