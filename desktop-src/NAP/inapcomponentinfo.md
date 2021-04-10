---
title: Interface INapComponentInfo (NapCommon. h)
description: Fournit des méthodes que les composants de plug-in (tels que les Sha et les SHV) doivent implémenter pour que le système NAP communique avec eux.
ms.assetid: eeff4f57-72e0-465f-9a18-ed72dad82bc7
keywords:
- NAP de l’interface INapComponentInfo
- INapComponentInfo interface NAP, Description
topic_type:
- apiref
api_name:
- INapComponentInfo
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba38c71cb79eb7222f619e6702008b31c41e7e2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941920"
---
# <a name="inapcomponentinfo-interface"></a>Interface INapComponentInfo

> [!Note]  
> La plate-forme de protection d’accès réseau n’est pas disponible à partir de Windows 10

 

L’interface **INapComponentInfo** fournit des méthodes que les composants de plug-in (tels que les Sha et les SHV) doivent implémenter pour que le système NAP communique avec eux. Le système NAP appelle l’implémentation de ces méthodes pour récupérer des informations d’administration statiques (par exemple, un nom convivial ou des chaînes localisées).

## <a name="members"></a>Membres

L’interface **INapComponentInfo** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **INapComponentInfo** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **INapComponentInfo** possède ces méthodes.



| Méthode                                                                                                         | Description                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------|
| [**INapComponentInfo::ConvertErrorCodeToMessageId**](inapcomponentinfo-converterrorcodetomessageid-method.md) | Utilisé par le système NAP pour demander au client d’intégrité de convertir un code d’erreur HRESULT en ID de message.<br/> |
| [**INapComponentInfo :: GetDescription**](inapcomponentinfo-getdescription-method.md)                           | Utilisé par le système NAP pour obtenir la description d’un client d’intégrité.<br/>                                  |
| [**INapComponentInfo::GetFriendlyName**](inapcomponentinfo-getfriendlyname-method.md)                         | Utilisé par le système NAP pour obtenir le nom convivial d’un client d’intégrité.<br/>                                |
| [**INapComponentInfo::GetIcon**](inapcomponentinfo-geticon-method.md)                                         | Utilisé par le système NAP pour obtenir l’icône d’un client d’intégrité.<br/>                                         |
| [**INapComponentInfo::GetLocalizedString**](inapcomponentinfo-getlocalizedstring-method.md)                   | Utilisé par le système NAP pour récupérer les chaînes localisées.<br/>                                                   |
| [**INapComponentInfo::GetVendorName**](inapcomponentinfo-getvendorname-method.md)                             | Utilisé par le système NAP pour obtenir le nom du fournisseur d’un client d’intégrité.<br/>                                  |
| [**INapComponentInfo :: GetVersion**](inapcomponentinfo-getversion-method.md)                                   | Utilisé par le système NAP pour obtenir la version d’un client de contrôle d’intégrité.<br/>                                      |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>NapCommon. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>NapCommon. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces NAP](nap-interfaces.md)
</dt> <dt>

[Référence NAP](nap-reference.md)
</dt> </dl>

 

