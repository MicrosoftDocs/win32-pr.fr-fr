---
title: Événement ListenStart
description: Événement ListenStart
ms.assetid: 59feacd6-0b9f-4bf4-b544-48de49384312
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19b8cc19ad727f8e9c4606bbbfba7b2e03e7d638
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840673"
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

### <a name="remarks"></a>Notes

Cet événement est envoyé à tous les clients lorsque le mode d’écoute commence parce que l’utilisateur a appuyé sur la touche d’écoute ou sur le client d’entrée-actif appelé la méthode [**Listen**](listen-method.md) avec la **valeur true**. Vous pouvez utiliser cet événement pour éviter que votre caractère ne parle alors que le mode d’écoute est activé.

Si vous activez le mode d’écoute avec la méthode [**Listen**](listen-method.md) , puis que l’utilisateur appuie sur la touche d’écoute, le mode d’écoute se réinitialise et se poursuit jusqu’à ce que le délai d’attente de la clé d’écoute se termine, que la clé d’écoute soit libérée ou que l’utilisateur finisse de parler, selon la date ultérieure. Dans ce cas, lorsque le mode d’écoute est déjà activé, vous n’obtiendrez pas d’événement **ListenStart** supplémentaire lorsque l’utilisateur appuie sur la touche d’écoute.

L’événement retourne le caractère aux clients pour lesquels ce caractère est actuellement chargé. Tous les autres clients reçoivent un caractère null (chaîne vide).

### <a name="see-also"></a>Voir aussi

[**Événement ListenComplete**](listencomplete-event.md), [ **méthode Listen**](listen-method.md)


 

 




