---
description: Le message de fermeture du téléphone TAPI \_ est envoyé lorsqu’un appareil téléphonique ouvert a été fermé de force dans le cadre de la récupération des ressources. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.
ms.assetid: 84650abf-235e-4792-a67d-2f0f08b85a32
title: Message PHONE_CLOSE (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d9a7641b437a10098806fc7ad52aa64200ca015
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127011103"
---
# <a name="phone_close-message"></a>Message de fermeture du téléphone \_

Le message **de \_ fermeture du téléphone** TAPI est envoyé lorsqu’un appareil téléphonique ouvert a été fermé de force dans le cadre de la récupération des ressources. Le descripteur d’appareil n’est plus valide une fois que ce message a été envoyé.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hPhone* 
</dt> <dd>

Handle vers l’appareil téléphonique ouvert qui a été fermé. Le descripteur n’est plus valide une fois que ce message a été envoyé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel de l’application fournie lors de l’ouverture du périphérique téléphonique.

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

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **\_ fermeture du téléphone** est envoyé à une application uniquement après la fermeture forcée d’un téléphone ouvert. Cela peut être fait pour empêcher une seule application de monopoliser un appareil téléphonique pendant trop longtemps. Si le téléphone peut être rouvert immédiatement après une fermeture forcée est spécifique à l’appareil.

Un appareil téléphonique ouvert peut également être fermé de force une fois que l’utilisateur a modifié la configuration de ce téléphone ou de son pilote. Si l’utilisateur souhaite que les modifications de configuration soient effectives immédiatement (par opposition à après le redémarrage du système suivant), et que ces modifications affectent la vue actuelle de l’application de l’appareil (par exemple, une modification des fonctionnalités de l’appareil), un fournisseur de services peut forcer la fermeture de l’appareil téléphonique.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




