---
description: L’interface IWiaAppErrorHandler permet aux applications d’afficher des fenêtres d’erreur (pendant les transferts de données) à partir desquelles l’utilisateur peut choisir de continuer, d’annuler ou d’abandonner le transfert.
ms.assetid: ac2597e6-2857-4694-bea7-1ea65d63b365
title: Interface IWiaAppErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 6ccac7b689055bfaab926a8db46b4632606811d7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127522228"
---
# <a name="iwiaapperrorhandler-interface"></a>Interface IWiaAppErrorHandler

L’interface **IWiaAppErrorHandler** permet aux applications d’afficher des fenêtres d’erreur (pendant les transferts de données) à partir desquelles l’utilisateur peut choisir de continuer, d’annuler ou d’abandonner le transfert.

## <a name="members"></a>Membres

L’interface **IWiaAppErrorHandler** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaAppErrorHandler** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaAppErrorHandler** possède ces méthodes.



| Méthode                                                        | Description                                                                                                                                             |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetWindow**](-wia-iwiaapperrorhandler-getwindow.md)       | Obtient un handle vers la boîte de dialogue qui affiche les messages d’erreur et fournit un ou plusieurs boutons pour continuer, annuler ou abandonner l’application.<br/> |
| [**ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) | Gère l’état des appareils et les messages d’erreur pendant les transferts de données d’image et affiche les messages à l’utilisateur.<br/>                                  |



 

## <a name="remarks"></a>Notes

l’objet de gestion des erreurs ou de rappel qui implémente cette interface est passé dans [**IWiaTransfer ::D lécharger**](-wia-iwiatransfer-download.md) et [**IWiaTransfer :: Télécharger**](-wia-iwiatransfer-upload.md).

Cette interface n’est pas conçue pour gérer les erreurs rencontrées en dehors des transferts de données d’image, par exemple, les erreurs d’obtention ou de définition des propriétés d’appareil ou les rappels non renvoyés dans un pilote.

Un gestionnaire d’erreurs de pilote doit implémenter [**IWiaErrorHandler**](-wia-iwiaerrorhandler.md)au lieu de **IWiaAppErrorHandler**.

L’objet qui implémente cette interface doit également implémenter [**IWiaTransferCallback**](-wia-iwiatransfercallback.md).

Si vous souhaitez qu’un gestionnaire d’erreurs de pilote et un gestionnaire d’erreurs par défaut affichent des fenêtres de message d’erreur, mais que vous ne souhaitez pas créer de gestionnaire d’erreurs complet pour l’application, implémentez cette interface et implémentez également la méthode [**IWiaAppErrorHandler :: ReportStatus**](-wia-iwiaapperrorhandler-reportstatus.md) pour retourner l' \_ État WIA \_ non \_ géré.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 
