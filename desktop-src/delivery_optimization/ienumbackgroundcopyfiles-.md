---
title: Interface IEnumBackgroundCopyFiles (Deliveryoptimization. h)
description: Utilisez l’interface IEnumBackgroundCopyFiles pour énumérer les fichiers contenus dans un travail. Pour récupérer un pointeur d’interface IEnumBackgroundCopyFiles, appelez la méthode EnumFiles méthode ibackgroundcopyjob.
ms.assetid: 539973BA-2756-4163-9D8B-4B7C0A708A8D
keywords:
- Interface IEnumBackgroundCopyFiles
- Interface IEnumBackgroundCopyFiles, Description
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7e46e94139a0c82e6c5b45f9397d76de8b4fdb43
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915647"
---
# <a name="ienumbackgroundcopyfiles-interface"></a>Interface IEnumBackgroundCopyFiles

Utilisez l’interface **IEnumBackgroundCopyFiles** pour énumérer les fichiers contenus dans un travail. Pour récupérer un pointeur d’interface **IEnumBackgroundCopyFiles** , appelez la méthode [**méthode ibackgroundcopyjob :: EnumFiles**](ibackgroundcopyjob-enumfiles.md) .

## <a name="members"></a>Membres

L’interface **IEnumBackgroundCopyFiles** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IEnumBackgroundCopyFiles** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IEnumBackgroundCopyFiles** possède ces méthodes.



| Méthode                                                | Description                                                                   |
|:------------------------------------------------------|:------------------------------------------------------------------------------|
| [**GetCount**](ienumbackgroundcopyfiles-getcount.md) | Récupère le nombre d’éléments dans l’énumération.<br/>                  |
| [**Suivant**](ienumbackgroundcopyfiles-next.md)         | Récupère un nombre spécifié d’éléments dans la séquence d’énumération.<br/> |
| [**Réinitialiser**](ienumbackgroundcopyfiles-reset.md)       | Réinitialise la séquence d'énumération au début.<br/>                  |
| [**Ignorer**](ienumbackgroundcopyfiles-skip.md)         | Ignore un nombre défini d'éléments dans la séquence d'énumération.<br/>     |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IEnumBackgroundCopyFiles est défini en tant que CA51E165-C365-424C-8D41-24AAA4FF3C40<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Méthode ibackgroundcopyjob :: EnumFiles**](ibackgroundcopyjob-enumfiles.md)
</dt> </dl>

 

