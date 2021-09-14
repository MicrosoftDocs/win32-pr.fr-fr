---
title: Interface IBackgroundCopyFile (Deliveryoptimization. h)
description: IBackgroundCopyFile contient des informations sur un fichier qui fait partie d’un travail. Par exemple, vous pouvez utiliser les méthodes IBackgroundCopyFile pour récupérer les noms locaux et distants du fichier et transférer les informations de progression.
ms.assetid: 463ED61A-D7C5-4B44-97CF-FDAA138CE9E3
keywords:
- Interface IBackgroundCopyFile
- Interface IBackgroundCopyFile, Description
topic_type:
- apiref
api_name:
- IBackgroundCopyFile
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3e4a54a66dee87770326d2456cb384e9d77f15e6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126921768"
---
# <a name="ibackgroundcopyfile-interface"></a>Interface IBackgroundCopyFile

**IBackgroundCopyFile** contient des informations sur un fichier qui fait partie d’un travail. Par exemple, vous pouvez utiliser les méthodes **IBackgroundCopyFile** pour récupérer les noms locaux et distants du fichier et transférer les informations de progression.

Pour récupérer un pointeur d’interface **IBackgroundCopyFile** , appelez la méthode [**IBackgroundCopyError :: GetFile**](ibackgroundcopyerror-getfile-method.md) ou la méthode [**IEnumBackgroundCopyFiles :: Next**](ienumbackgroundcopyfiles-next.md) .

## <a name="members"></a>Membres

L’interface **IBackgroundCopyFile** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IBackgroundCopyFile** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IBackgroundCopyFile** possède ces méthodes.



| Méthode                                                            | Description                                             |
|:------------------------------------------------------------------|:--------------------------------------------------------|
| [**GetLocalName**](ibackgroundcopyfile-getlocalname-method.md)   | Récupère le nom local du fichier.<br/>        |
| [**GetProgress**](ibackgroundcopyfile-getprogress-method.md)     | Récupère la progression du transfert de fichier.<br/> |
| [**GetRemoteName**](ibackgroundcopyfile-getremotename-method.md) | Récupère le nom distant du fichier.<br/>       |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1709 \[ uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur, version 1709 \[ applications de bureau uniquement\]<br/>                                       |
| En-tête<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>DeliveryOptimization. idl</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Dosvc. lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile est défini en tant que 01B7BD23-FB88-4A77-8490-5891D3E4653A<br/>              |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IBackgroundCopyError**](ibackgroundcopyerror.md)
</dt> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> <dt>

[**Méthode ibackgroundcopyjob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

