---
title: Player. playerApplication
description: la propriété playerApplication récupère l’objet playerApplication lorsqu’un contrôle Lecteur Windows Media distant est en cours d’exécution.
ms.assetid: 09a8a63f-455f-4f81-8fdb-7de337139dea
keywords:
- Lecteur Windows Media Player. playerApplication
topic_type:
- apiref
api_name:
- Player.playerApplication
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c47400fcba1cb1cd1679e747d4fdd49b155df921ec33a721f74df2ec25259600
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995849"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

la propriété **playerApplication** récupère l’objet **playerApplication** lorsqu’un contrôle Lecteur Windows Media distant est en cours d’exécution.

## <a name="syntax"></a>Syntaxe

**playerApplication**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet **PlayerApplication** en lecture seule ou la valeur null.

## <a name="remarks"></a>Remarques

cette propriété est utilisée uniquement lors de la communication à distance du Windows multimédia Playercontrol. si la valeur est null, le Windows multimédia Playercontrol n’est pas incorporé en mode distant.

Cette propriété est accessible uniquement dans le code C++ ou dans le code de script des habillages via la variable globale playerApplication.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Attributs globaux**](global-attributes.md)
</dt> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Objet PlayerApplication**](playerapplication-object.md)
</dt> <dt>

[**Utilisation à distance du contrôle Windows Media Player**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 





