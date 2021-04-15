---
title: Interface IBackgroundCopyError (Deliveryoptimization. h)
description: Utilisez l’interface IBackgroundCopyError pour déterminer la cause d’une erreur et si le processus de transfert peut se poursuivre.
ms.assetid: 7DCB63CF-4180-4DC3-9093-07C4F8CF7A8E
keywords:
- Interface IBackgroundCopyError
- Interface IBackgroundCopyError, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f35365d56ce9391a746e479e1b59034342ebf62
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465078"
---
# <a name="ibackgroundcopyerror-interface"></a>Interface IBackgroundCopyError

Utilisez l’interface **IBackgroundCopyError** pour déterminer la cause d’une erreur et si le processus de transfert peut se poursuivre.

Crée un objet d’erreur uniquement lorsque l’état du travail est BG_JOB_STATE_ERROR ou BG_JOB_STATE_TRANSIENT_ERROR. NE créez pas d’objet d’erreur lorsqu’une méthode d’interface **IBackgroundCopyXXXX** échoue. L’objet d’erreur est disponible jusqu’à ce que commence à transférer les données (l’état du travail passe à BG_JOB_STATE_TRANSFERRING) pour le travail.

Pour récupérer un objet **IBackgroundCopyError** , appelez la méthode [**méthode ibackgroundcopyjob :: GetError**](ibackgroundcopyjob-geterror.md) .

## <a name="members"></a>Membres

L’interface **IBackgroundCopyError** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyError** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyError** possède ces méthodes.



| Méthode                                                   | Description                                                                                 |
|:---------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**GetError**](ibackgroundcopyerror-geterror-method.md) | Récupère le code d’erreur et identifie le contexte dans lequel l’erreur s’est produite.<br/> |
| [**GetFile**](ibackgroundcopyerror-getfile-method.md)   | Récupère un pointeur d’interface vers l’objet de fichier associé à l’erreur.<br/>     |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Server, version 1709, \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyError est défini en tant que 19C613A0-FCB8-4F28-81AE-897C3D078F81<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetError**](ibackgroundcopyjob-geterror.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob :: GetState**](ibackgroundcopyjob-getstate.md)
</dt> <dt>

[**IBackgroundCopyCallback::JobError**](ibackgroundcopycallback-joberror-method.md)
</dt> </dl>

 

