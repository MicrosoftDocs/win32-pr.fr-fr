---
description: Ces fonctions assurent la prise en charge de l’implémentation de l’interface IUnknown dans DirectShow.
ms.assetid: 991e4c69-7d30-4ecf-9ccf-4920452c21d6
title: Fonctions d’assistance COM (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COM
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9522469ee1aa4f4efa63b4cff6ad73204973a622
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106529020"
---
# <a name="com-helper-functions"></a>Fonctions d’assistance COM

Ces fonctions assurent la prise en charge de l’implémentation de l’interface **IUnknown** dans DirectShow.



| Fonction                                               | Description                                                           |
|--------------------------------------------------------|-----------------------------------------------------------------------|
| [**DÉCLARER \_ IUnknown**](declare-iunknown.md)          | Déclare les trois méthodes de l’interface de base pour une nouvelle interface. |
| [**GetInterface**](getinterface.md)                   | Récupère un pointeur d’interface vers le client demandé.               |
| [**INonDelegatingUnknown**](inondelegatingunknown.md) | Version Nondelegating de l’interface **IUnknown** .                  |
| [**LoadOLEAut32**](loadoleaut32.md)                   | Charge la DLL Automation (OleAut32.dll).                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>ComBase. h (include streams. h)</dt> </dl>                                                                                   |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Fonctions utilitaires](utility-functions.md)
</dt> </dl>

 

 




