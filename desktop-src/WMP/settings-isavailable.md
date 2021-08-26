---
title: Paramètres. isAvailable
description: La propriété isAvailable indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée. | Paramètres. isAvailable
ms.assetid: 89403125-545c-482b-a27e-6fee06abe247
keywords:
- Paramètres. isAvailable Lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.isAvailable
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df10026007dd9e04fe88d634a3da566074b0d6a88420ef444d5f2bae39a793fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002409"
---
# <a name="settingsisavailable"></a>Paramètres. isAvailable

La propriété **isAvailable** indique si un type spécifié d’informations est disponible ou si une action spécifiée peut être exécutée.

## <a name="syntax"></a>Syntaxe

Player. Settings. isAvailable (Name)

## <a name="parameters"></a>Paramètres

*name*

Chaîne contenant l’une des valeurs suivantes.



| String             | Description                                                    |
|--------------------|----------------------------------------------------------------|
| démarrage automatique          | Détermine si la propriété AutoStart peut être définie.          |
| Balance            | Détermine si la propriété de solde peut être définie.            |
| BaseURL            | Détermine si la propriété baseURL peut être définie.            |
| DefaultFrame       | Détermine si la propriété defaultFrame peut être définie.       |
| EnableErrorDialogs | Détermine si la propriété enableErrorDialogs peut être définie. |
| GetMode            | Détermine si la méthode getMode peut être appelée.           |
| InvokeURLs         | Détermine si la propriété invokeURLs peut être définie.         |
| Désactiver le son               | Détermine si la propriété muet peut être définie.               |
| PlayCount          | Détermine si la propriété playCount peut être définie.          |
| Tarif               | Détermine si la propriété rate peut être définie.               |
| SetMode            | Détermine si la méthode setMode peut être appelée.           |
| Volume             | Détermine si la propriété de volume peut être définie.             |



 

## <a name="return-values"></a>Valeurs de retour

Cette méthode retourne une valeur **booléenne** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





