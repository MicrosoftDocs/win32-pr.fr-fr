---
description: L’interface IKsPin fournit une méthode pour récupérer les supports pris en charge par un code confidentiel sur un filtre en mode noyau. IKsPin a des méthodes supplémentaires en plus de celle présentée ici, mais elles ne sont pas prises en charge pour DirectShow.
ms.assetid: 14d9bef2-e8f0-49d5-bd89-69a95814cf8c
title: Interface IKsPin (ksproxy. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IKsPin
api_type:
- COM
api_location:
- Strmiids.lib
- Strmiids.dll
ms.openlocfilehash: 8855378544bcc2ea7357af220b5d80d32edde74a50c304e973c9821aa8e9a41c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119792329"
---
# <a name="ikspin-interface"></a>Interface IKsPin

L' `IKsPin` interface fournit une méthode pour récupérer les supports pris en charge par un code confidentiel sur un filtre en mode noyau. `IKsPin`a des méthodes supplémentaires en plus de celles présentées ici, mais elles ne sont pas prises en charge pour DirectShow.

## <a name="members"></a>Membres

L’interface **IKsPin** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPin** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IKsPin** possède ces méthodes.



| Méthode                                          | Description                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Récupère les supports pris en charge par un code confidentiel.<br/> |



 

## <a name="remarks"></a>Remarques

Vous devez inclure KS. h avant ksproxy. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
