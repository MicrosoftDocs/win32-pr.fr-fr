---
title: Interface IWMPLibraryServices (VB et C) (WMP. h)
description: Fournit des méthodes pour énumérer des bibliothèques.
ms.assetid: f2a72731-6e61-4f78-b0ca-ae907004eb7d
keywords:
- IWMPLibraryServices (VB et C) interface Windows Media Player
- Interface IWMPLibraryServices (VB et C), le lecteur Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMPLibraryServices (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3493d5c94dcbd9db1e4f281a8fddfadbd2e336f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544071"
---
# <a name="iwmplibraryservices-vb-and-c-interface"></a>Interface IWMPLibraryServices (VB et C#)

Fournit des méthodes pour énumérer des bibliothèques.

## <a name="members"></a>Membres

L’interface **IWMPLibraryServices (VB et C#)** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMPLibraryServices (VB et C#)** possède ces méthodes.



| Méthode                                                                                               | Description                                                                                                        |
|:-----------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**getCountByType**](wmplibiwmplibraryservices-iwmplibraryservices-getcountbytype--vb-and-c.md)     | Retourne le nombre de bibliothèques disponibles d’un type spécifié.<br/>                                           |
| [**getLibraryByType**](wmplibiwmplibraryservices-iwmplibraryservices-getlibrarybytype--vb-and-c.md) | Retourne une interface **IWMPLibrary** qui représente la bibliothèque ayant le type et l’index spécifiés.<br/> |



 

Obtient une interface **IWMPLibraryServices** en effectuant un cast de l’objet retourné par la méthode **AxWindowsMediaPlayer. GetOcx** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>WMP. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces pour Visual Basic .NET et C #**](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[**Interface IWMPLibrary (VB et C#)**](iwmplibrary--vb-and-c.md)
</dt> </dl>

 

 





