---
title: Paramètres. baseURL
description: La propriété baseURL spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec les commandes de script d’URL incorporées dans les éléments multimédias.
ms.assetid: bb2db144-6d1e-4ed6-baed-dc5dbff44aa0
keywords:
- Paramètres. baseURL Lecteur Windows Media
topic_type:
- apiref
api_name:
- Settings.baseURL
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69e06275a3028df6b90d25665e11aab3c2a0961dfa6c525cde0636434f06986b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995379"
---
# <a name="settingsbaseurl"></a>Paramètres. baseURL

La propriété **baseURL** spécifie ou récupère l’URL de base utilisée pour la résolution de chemin d’accès relative avec les commandes de script d’URL incorporées dans les éléments multimédias.

## <a name="syntax"></a>Syntaxe

Player. Settings. baseURL

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est une **chaîne** en lecture/écriture.

## <a name="remarks"></a>Remarques

Cette propriété spécifie l’URL HTTP de base qui est transmise en tant que paramètre de commande par l’événement **commande** . L’URL de base est concaténée avec l’URL relative, comme suit :

1.  Une barre oblique finale (/) est ajoutée à la valeur de la propriété **baseURL** .
2.  Un point de début, une barre oblique inverse ou une barre oblique (., \\ et/) sont supprimés de l’URL relative.
3.  L’URL relative est ajoutée à la fin de l’URL de base.
4.  Toutes les barres obliques de l’URL complète résultante sont pointées dans la même direction (converties en barres obliques ou en arrière) en fonction de la direction de la première barre oblique rencontrée dans la nouvelle URL.

**Remarque**

Le contrôle de lecteur ne prend pas en charge l’utilisation de deux points (..) dans l’URL relative pour indiquer le parent de l’emplacement actuel.

**Lecteur Windows Media 10 Mobile**: cette propriété est en lecture seule et retourne toujours une chaîne vide.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Événement Player. commande**](player-player-scriptcommand.md)
</dt> <dt>

[**Paramètres Dessin**](settings-object.md)
</dt> </dl>

 

 





