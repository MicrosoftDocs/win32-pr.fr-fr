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
ms.openlocfilehash: 3d65e5ba5525b977ebae27da9964579614a1d653
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106516343"
---
# <a name="ikspin-interface"></a>Interface IKsPin

L' `IKsPin` interface fournit une méthode pour récupérer les supports pris en charge par un code confidentiel sur un filtre en mode noyau. `IKsPin` a des méthodes supplémentaires autres que celles indiquées ici, mais elles ne sont pas prises en charge pour DirectShow.

## <a name="members"></a>Membres

L’interface **IKsPin** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IKsPin** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IKsPin** possède ces méthodes.



| Méthode                                          | Description                                          |
|:------------------------------------------------|:-----------------------------------------------------|
| [**KsQueryMediums**](ikspin-ksquerymediums.md) | Récupère les supports pris en charge par un code confidentiel.<br/> |



 

## <a name="remarks"></a>Notes

Vous devez inclure KS. h avant ksproxy. h.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                    |
| En-tête<br/>                   | <dl> <dt>Ksproxy. h</dt> </dl>    |
| Bibliothèque<br/>                  | <dl> <dt>Strmiids. lib</dt> </dl> |



 

 
