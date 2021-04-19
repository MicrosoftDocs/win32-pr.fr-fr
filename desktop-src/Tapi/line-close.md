---
description: Le message de fermeture de la ligne TAPI \_ est envoyé lorsque l’appareil de ligne spécifié a été fermé de force. Le handle de périphérique de ligne ou les handles d’appel des appels sur la ligne ne sont plus valides une fois que ce message a été envoyé.
ms.assetid: f254e331-d574-4fa7-8447-6e4535d3d773
title: Message LINE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7f4fde53d1017b2dcd9fe4ea833803055d9f2dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532606"
---
# <a name="line_close-message"></a>Message de fermeture de ligne \_

Le message **de \_ fermeture** de la ligne TAPI est envoyé lorsque l’appareil de ligne spécifié a été fermé de force. Le handle de périphérique de ligne ou les handles d’appel des appels sur la ligne ne sont plus valides une fois que ce message a été envoyé.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle vers le périphérique de ligne qui a été fermé. Ce descripteur n’est plus valide.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Inutilisé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Inutilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **\_ fermeture de ligne** est envoyé à toute application uniquement après que le fournisseur de services TAPI (TSP) a fermé de force une ligne ouverte. Si la ligne peut ou non être rouverte immédiatement après une fermeture forcée, elle est spécifique à l’appareil.

La condition à l’origine du problème peut être un changement important de l’État, une erreur matérielle, une perte de connexion à un serveur, ou même potentiellement empêcher une application de monopoliser un appareil de ligne trop longtemps. Un périphérique de ligne peut également être fermé de force une fois que l’utilisateur a modifié la configuration de cette ligne ou de son pilote. Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et qu’elles affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut fermer l’appareil de ligne de force.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




