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
ms.openlocfilehash: 7b3ea9f5556f1f919336e4abb4085f9e0c32d81d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113895"
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



 

## <a name="remarks"></a>Notes

L’objet de rappel d’application peut implémenter **IWiaErrorHandler**.

Cette interface n’est pas conçue pour gérer les erreurs rencontrées en dehors des transferts de données d’image, par exemple, les erreurs d’obtention ou de définition des propriétés d’appareil ou les rappels non renvoyés dans un pilote.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>WIA. h</dt> </dl>       |
| MIDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl>     |
| Bibliothèque<br/>                  | <dl> <dt>Wiaguid. lib</dt> </dl> |



 

 
