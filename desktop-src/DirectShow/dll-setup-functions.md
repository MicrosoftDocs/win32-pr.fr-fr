---
description: Ces fonctions inscrivent un filtre.
ms.assetid: c9c4976f-d4c5-465e-8ad7-4294c05d0e0a
title: Fonctions de configuration des DLL (DLLSETUP. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DLL
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 449c6899c207365118a57e396bb52817282453ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539532"
---
# <a name="dll-setup-functions"></a>Fonctions de configuration des DLL

Ces fonctions inscrivent un filtre.



| Fonction                                                         | Description                                        |
|------------------------------------------------------------------|----------------------------------------------------|
| [**AMovieDllRegisterServer**](amoviedllregisterserver.md)       | Obsolète.                                          |
| [**AMovieDllRegisterServer2**](amoviedllregisterserver2.md)     | Inscrit et annule l’inscription des filtres.                 |
| [**AMovieDllUnregisterServer**](amoviedllunregisterserver.md)   | Obsolète.                                          |
| [**AMovieSetupRegisterFilter**](amoviesetupregisterfilter.md)   | Obsolète.                                          |
| [**AMovieSetupRegisterFilter2**](amoviesetupregisterfilter2.md) | Enregistre les mérites, les codes confidentiels et les types de média d’un filtre. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>DLLSETUP. h (include streams. h)</dt> </dl>                                                                                  |
| Bibliothèque<br/> | <dl> <dt>Strmbase. lib (versions commerciales); </dt> <dt>Strmbasd. lib (versions Debug)</dt> </dl> |



 

 




