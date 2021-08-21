---
title: Événement ListenStart
description: Événement ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0017b628af3ca266058de74508d379bd665c94f94c64207f4d7bef5487a0f4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976109"
---
# <a name="listenstart-event"></a>Événement ListenStart

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le mode d’écoute (reconnaissance vocale) commence.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sous** - *agent. * * * ListenStart (ByVal* *  *CharacterID * * *)**



| Partie          | Description                                            |
|---------------|--------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère d’écoute sous la forme d’une chaîne. |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Cet événement est envoyé à tous les clients lorsque le mode d’écoute commence parce que l’utilisateur a appuyé sur la touche d’écoute ou sur le client d’entrée-actif appelé la méthode [**Listen**](listen-method.md) avec la **valeur true**. Vous pouvez utiliser cet événement pour éviter que votre caractère ne parle alors que le mode d’écoute est activé.

Si vous activez le mode d’écoute avec la méthode [**Listen**](listen-method.md) , puis que l’utilisateur appuie sur la touche d’écoute, le mode d’écoute se réinitialise et se poursuit jusqu’à ce que le délai d’attente de la clé d’écoute se termine, que la clé d’écoute soit libérée ou que l’utilisateur finisse de parler, selon la date ultérieure. Dans ce cas, lorsque le mode d’écoute est déjà activé, vous n’obtiendrez pas d’événement **ListenStart** supplémentaire lorsque l’utilisateur appuie sur la touche d’écoute.

L’événement retourne le caractère aux clients pour lesquels ce caractère est actuellement chargé. Tous les autres clients reçoivent un caractère null (chaîne vide).

### <a name="see-also"></a>Voir aussi

[**Événement ListenComplete**](listencomplete-event.md), [ **méthode Listen**](listen-method.md)


 

 




