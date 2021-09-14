---
title: Interface IBackgroundCopyFile5 (Deliveryoptimization. h)
description: Utilisez cette interface pour récupérer ou définir les propriétés génériques des transferts de fichiers d’optimisation de la remise (DO).
ms.assetid: 2D729717-62D2-4C69-92FE-F4289EC48DF1
keywords:
- Interface IBackgroundCopyFile5
- Interface IBackgroundCopyFile5, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2f23fdb99ba24b4faeca7a65930bf83d4634a979
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852327"
---
# <a name="ibackgroundcopyfile5-interface"></a>Interface IBackgroundCopyFile5

Utilisez cette interface pour récupérer ou définir les propriétés génériques des transferts de fichiers d’optimisation de la remise (DO).

Pour obtenir un pointeur d’interface **IBackgroundCopyFile5** , appelez la méthode **IBackgroundCopyFile :: QueryInterface** à l’aide de __uuidof (IBackgroundCopyFile5) pour l’identificateur d’interface.

## <a name="members"></a>Membres

L’interface **IBackgroundCopyFile5** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile5** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyFile5** possède ces méthodes.



| Méthode                                                  | Description                                                         |
|:--------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetProperty**](ibackgroundcopyfile5-getproperty.md) | Obtient la valeur d’une propriété BackgroundCopyFile générique.<br/> |
| [**SetProperty**](ibackgroundcopyfile5-setproperty.md) | Définit la valeur d’une propriété BackgroundCopyFile générique.<br/> |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 est défini en tant que 85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

