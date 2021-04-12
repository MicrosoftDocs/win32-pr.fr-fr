---
description: L’interface IWiaTransfer fournit un transfert de données basé sur les flux.
ms.assetid: 7bc6d3b8-9bf0-4b77-aa2b-b7c64c5730c0
title: Interface IWiaTransfer (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaTransfer
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 623cc21591289f4c1fff33cabe1d504b3682708c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201489"
---
# <a name="iwiatransfer-interface"></a>Interface IWiaTransfer

L’interface **IWiaTransfer** fournit un transfert de données basé sur les flux.

## <a name="members"></a>Membres

L’interface **IWiaTransfer** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaTransfer** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaTransfer** possède ces méthodes.



| Méthode                                                                 | Description                                                                                 |
|:-----------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Annuler**](-wia-iwiatransfer-cancel.md)                             | Annule l’opération de transfert en cours. <br/>                                         |
| [**Télécharger**](-wia-iwiatransfer-download.md)                         | Lance un téléchargement de données vers l’appelant. <br/>                                        |
| [**\_Informations de format EnumWIA \_**](-wia-iwiatransfer-enumwia-format-info.md) | Crée un énumérateur pour les formats de transfert pris en charge par l’appareil WIA 2,0.<br/> |
| [**Télécharger**](-wia-iwiatransfer-upload.md)                             | Lance un chargement de données d’un élément unique à partir de l’appelant. <br/>                       |



 

## <a name="remarks"></a>Notes

L’interface **IWiaTransfer** , comme toutes les interfaces COM (Component Object Model), hérite des méthodes d’interface [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .



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



 

 
