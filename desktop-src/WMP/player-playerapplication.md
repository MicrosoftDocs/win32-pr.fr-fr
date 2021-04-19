---
title: Player. playerApplication
description: La propriété playerApplication récupère l’objet PlayerApplication lorsqu’un contrôle du lecteur Windows Media distant est en cours d’exécution.
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
ms.openlocfilehash: 401ebaae52efb746e7119419774d87d72c642fc4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106522798"
---
# <a name="playerplayerapplication"></a>Player. playerApplication

La propriété **playerApplication** récupère l’objet **playerApplication** lorsqu’un contrôle du lecteur Windows Media distant est en cours d’exécution.

## <a name="syntax"></a>Syntaxe

**playerApplication**

## <a name="possible-values"></a>Valeurs possibles

Cette propriété est un objet **PlayerApplication** en lecture seule ou la valeur null.

## <a name="remarks"></a>Notes

Cette propriété est utilisée uniquement lors de la communication à distance de Windows Media playercontrol. Si la valeur est null, le playercontrol Windows Media n’est pas incorporé en mode distant.

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

 

 





