---
title: Activate, méthode
description: Activate, méthode
ms.assetid: 8111139d-1453-416e-8f08-38c06669ff4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5032c7c7f2faf7ec53028a0cc0ce55847fe300864bb531968fc8190b4e00d164
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753158"
---
# <a name="activate-method"></a>Activate, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>[**Descriptive**](../wmformat/description.md)
</dt> <dd>

Définit le client ou le caractère actif.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Activer_ l' *  \[ *État*\]



| Partie    | Description                                                                                                                                                                           |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *State* | Facultatif. Vous pouvez spécifier les valeurs suivantes pour ce paramètre : 0 n’est pas le client actif.<br/> 1 le client actif. <br/> 2 (valeur par défaut) le caractère le plus haut.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque plusieurs caractères sont visibles, un seul des caractères reçoit les entrées vocales à la fois. De même, lorsque plusieurs applications clientes partagent le même caractère, un seul des clients reçoit l’entrée de la souris (par exemple, les événements Click ou Drag du contrôle Microsoft Agent). Le jeu de caractères pour recevoir l’entrée de la souris et de la parole est le caractère le plus élevé et le client qui reçoit l’entrée est le client actif de ce caractère. (La fenêtre du caractère supérieur s’affiche également en haut de l’ordre de plan de la fenêtre de caractères.) En règle générale, l’utilisateur détermine le caractère supérieur en sélectionnant explicitement le caractère. Toutefois, l’activation de niveau supérieur change également lorsqu’un caractère est affiché ou masqué (le caractère devient ou n’est plus le premier niveau, respectivement).

Vous pouvez également utiliser cette méthode pour gérer explicitement quand votre client reçoit une entrée dirigée vers le caractère, par exemple lorsque votre application est elle-même active. Par exemple, la définition de l' *État* sur 2 rend le caractère le plus haut et votre client reçoit tous les événements d’entrée de la souris et de la parole générés par l’interaction de l’utilisateur avec le caractère. Par conséquent, il rend également votre client le client d’entrée-actif du caractère.

Toutefois, vous pouvez également vous définir comme client actif pour un caractère sans rendre le caractère le plus haut, en définissant l' *État* sur 1. Cela permet à votre client de recevoir l’entrée dirigée vers ce caractère lorsque le caractère devient le plus haut. De même, vous pouvez configurer votre client pour qu’il ne soit pas le client actif (et non recevoir l’entrée) lorsque le caractère devient le plus haut, en définissant l' *État* sur 0.

Évitez d’appeler cette méthode directement après une méthode [**Show**](/previous-versions/visualstudio/foxpro/d79z7xxa(v=vs.71)) . **Afficher** définit automatiquement le client d’entrée-actif. Lorsque le caractère est masqué, l’appel d' [**activation**](/previous-versions/visualstudio/foxpro/01ayxx68(v=vs.71)) peut échouer s’il est traité avant la fin de la méthode **Show** .

Si vous appelez cette méthode sur une fonction, elle retourne une valeur booléenne qui indique si la méthode a réussi. Toute tentative d’appel à cette méthode avec le paramètre d' *État* défini sur la valeur 2 lorsque le caractère spécifié est masqué échoue. De même, si vous affectez à l' *État* la valeur 0 et que votre application est le seul client, cet appel échoue parce qu’un caractère doit toujours avoir un client le plus haut.


```
   Dim Genie as Object

   Sub FormLoad()

   Agent1.Characters.Load "Genie", "Genie.acs"

   Set Genie = Agent1.Characters ("Genie")

   If (Genie. Activate = True) Then
      'I'm active

   Else
      'I must be hidden or something

   End If 
   
   End Sub
```



> [!Note]  
> L’appel de cette méthode avec un *État* défini sur 1 ne génère généralement pas d’événement [**ActivateInput**](https://www.bing.com/search?q=**ActivateInput**) , sauf si aucun autre caractère n’est chargé ou si votre application est déjà en entrée-active.

 

## <a name="see-also"></a>Voir aussi

[**Événement ActivateInput**](activateinput-event.md), [ **événement DeactivateInput**](deactivateinput-event.md)


 

