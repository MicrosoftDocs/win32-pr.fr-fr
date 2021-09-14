---
title: Interface IBackgroundCopyFile2 (Deliveryoptimization. h)
description: Utilisez l’interface IBackgroundCopyFile2 pour spécifier un nouveau nom distant pour le fichier et récupérer la liste des plages à télécharger.
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- Interface IBackgroundCopyFile2
- Interface IBackgroundCopyFile2, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126855382"
---
# <a name="ibackgroundcopyfile2-interface"></a>Interface IBackgroundCopyFile2

Utilisez l’interface **IBackgroundCopyFile2** pour spécifier un nouveau nom distant pour le fichier et récupérer la liste des plages à télécharger.

L’interface **IBackgroundCopyFile2** hérite de l’interface [**IBackgroundCopyFile**](ibackgroundcopyfile.md) .

Pour obtenir un pointeur d’interface **IBackgroundCopyFile2** , appelez la méthode **IBackgroundCopyFile :: QueryInterface** à l’aide de __uuidof (IBackgroundCopyFile2) pour l’identificateur d’interface. Utilisez le pointeur d’interface **IBackgroundCopyFile2** pour appeler les méthodes [**IBackgroundCopyFile**](ibackgroundcopyfile.md) et **IBackgroundCopyFile2** .

## <a name="members"></a>Membres

L’interface **IBackgroundCopyFile2** hérite de [**IBackgroundCopyFile**](ibackgroundcopyfile.md). **IBackgroundCopyFile2** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyFile2** possède ces méthodes.



| Méthode                                                             | Description                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | Récupère le tableau de plages que vous souhaitez télécharger à partir de l’URL.<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | Remplace le nom distant par une nouvelle URL.<br/>                                 |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 est défini en tant que 83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





