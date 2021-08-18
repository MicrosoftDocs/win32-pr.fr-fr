---
description: L’interface IWiaErrorHandler fournit des méthodes pour gérer les erreurs qui peuvent se produire lorsqu’une application demande des données d’image, qu’il s’agisse d’un aperçu ou de bits finaux.
ms.assetid: 33d8ccc5-6856-4a54-b1f0-d015933d63ab
title: Interface IWiaErrorHandler (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 6e97c5a146c23ce1ecdb2ba77cde5d37cd9091fc9d77e288042f02fc118816e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965588"
---
# <a name="iwiaerrorhandler-interface"></a>Interface IWiaErrorHandler

L’interface **IWiaErrorHandler** fournit des méthodes pour gérer les erreurs qui peuvent se produire lorsqu’une application demande des données d’image, qu’il s’agisse d’un aperçu ou de bits finaux.

## <a name="members"></a>Membres

L’interface **IWiaErrorHandler** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IWiaErrorHandler** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWiaErrorHandler** possède ces méthodes.



| Méthode                                                                     | Description                                                                                             |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**GetStatusDescription**](-wia-iwiaerrorhandler-getstatusdescription.md) | Retourne une chaîne qui décrit le code d’État.<br/>                                             |
| [**ReportStatus**](-wia-iwiaerrorhandler-reportstatus.md)                 | Gère les messages d’État et d’erreur pendant les transferts de données d’image et les affiche à l’utilisateur.<br/> |



 

## <a name="remarks"></a>Remarques

L’objet de rappel d’application peut implémenter **IWiaErrorHandler**.

Cette interface n’est pas conçue pour gérer les erreurs rencontrées en dehors des transferts de données d’image, par exemple, les erreurs d’obtention ou de définition des propriétés d’appareil ou les rappels non renvoyés dans un pilote.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
