---
description: L’interface IWiaTransferCallback reçoit des rappels pendant un transfert de données.
ms.assetid: 8fcaccf5-4d7b-4984-97ec-ec8c838a8360
title: Interface IWiaTransferCallback (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransferCallback
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 918482ebcb24f2638a006ab1bbc452ea28ff61e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113294"
---
# <a name="iwiatransfercallback-interface"></a>Interface IWiaTransferCallback

L’interface **IWiaTransferCallback** reçoit des rappels pendant un transfert de données.

## <a name="members"></a>Membres

L’interface **IWiaTransferCallback** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransferCallback** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaTransferCallback** possède ces méthodes.



| Méthode                                                                 | Description                                                              |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------|
| [**GetNextStream**](-wia-iwiatransfercallback-getnextstream.md)       | Obtient un nouveau flux pour l’élément spécifié. <br/>                    |
| [**TransferCallback**](-wia-iwiatransfercallback-transfercallback.md) | Fournit la progression et d’autres notifications pendant un transfert. <br/> |



 

## <a name="remarks"></a>Notes

Les développeurs de filtres de traitement d’images doivent implémenter cette interface et l’interface [**IWiaImageFilter**](-wia-iwiaimagefilter.md) .

L’interface **IWiaTransferCallback** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



| Méthodes IUnknown                                        | Description                               |
|---------------------------------------------------------|-------------------------------------------|
| [IUnknown :: QueryInterface](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) | Retourne des pointeurs aux interfaces prises en charge. |
| [IUnknown :: AddRef](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)                 | Incrémente le décompte de références.               |
| [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)               | Décrémente le décompte de références.               |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
