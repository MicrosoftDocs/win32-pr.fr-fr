---
title: Événement ListenComplete
description: Événement ListenComplete
ms.assetid: 29e3f424-17b4-4287-b644-ed62b80e0035
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d25e9bfbf23c6a2911c718b576c99395ef06fd802853b39b699384a9ab92429b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117883891"
---
# <a name="listencomplete-event"></a>Événement ListenComplete

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Se produit lorsque le mode d’écoute (reconnaissance vocale) est terminé.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

**Sub** *agent. * * * ListenComplete (ByVal* *  *CharacterID*, **ByVal** *cause * * *)**



| Partie          | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *CharacterID* | Retourne l’ID du caractère d’écoute sous la forme d’une chaîne.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *Cause*       | Retourne la cause de l’événement complet sous la forme d’un entier pouvant être l’un des suivants : 1 le mode d’écoute a été désactivé par le code de programme.<br/> 2 le mode d’écoute (activé par code de programme) a expiré.<br/> 3 le mode d’écoute (activé par la clé d’écoute) a expiré.<br/> 4 le mode d’écoute a été désactivé, car l’utilisateur a relâché la clé d’écoute.<br/> 5 mode d’écoute terminé, car l’utilisateur a terminé de parler.<br/> 6 mode d’écoute terminé car le client d’entrée-actif a été désactivé.<br/> 7 mode d’écoute terminé car le caractère par défaut a été modifié.<br/> 8 mode d’écoute terminé, car l’utilisateur a désactivé l’entrée vocale.<br/> |



 

</dd> </dl>

### <a name="remarks"></a>Remarques

Cet événement est envoyé à tous les clients lorsque le délai d’attente du mode d’écoute se termine, après que l’utilisateur a libéré la clé d’écoute, lorsque le client actif d’entrée appelle la méthode [**Listen**](listen-method.md) avec la **valeur false** ou que l’utilisateur a terminé de parler. Vous pouvez utiliser cet événement pour déterminer à quel moment reprendre la sortie de caractères parlés (audio).

Si vous activez le mode d’écoute à l’aide de la méthode [**Listen**](listen-method.md) , puis que l’utilisateur appuie sur la touche d’écoute, le mode d’écoute se réinitialise et se poursuit jusqu’à ce que le délai d’attente de la clé d’écoute se termine, que la clé d’écoute soit libérée ou que l’utilisateur finisse de parler, selon la date ultérieure. Dans ce cas, vous ne recevrez pas d’événement **ListenComplete** tant que le mode de la clé d’écoute n’est pas terminé.

L’événement retourne le caractère aux clients pour lesquels ce caractère est actuellement chargé. Tous les autres clients reçoivent un caractère null (chaîne vide).

### <a name="see-also"></a>Voir aussi

[**Événement ListenStart**](listenstart-event.md), [ **méthode Listen**](listen-method.md)


 

 





