---
title: Interrupt, méthode
description: Interrupt, méthode
ms.assetid: b8442e25-a629-47c7-acdd-1d28e74d78a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05e66814963bb3de3db95d60cbc25777244626168e95ceee4bd3d8d76992dd72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118749256"
---
# <a name="interrupt-method"></a>Interrupt, méthode

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Interrompt l’animation pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»)._ *  *Demande* d’interruption



| Partie      | Description                                                                  |
|-----------|------------------------------------------------------------------------------|
| *Requête* | Objet de [**demande**](/windows/desktop/lwef/the-request-object) pour un appel d’animation particulier. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Vous pouvez l’utiliser pour synchroniser l’animation entre les caractères. Par exemple, si un autre caractère se trouve dans une animation de bouclage, cette méthode arrête la boucle et passe à l’animation suivante dans la file d’attente du caractère. Vous ne pouvez pas interrompre une animation de caractères que vous n’utilisez pas (que vous n’avez pas chargée).

Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez interrompre :


```
   Dim GenieRequest as Object
   Dim RobbyRequest as Object
   Dim Genie as Object
   Dim Robby as Object

   Sub FormLoad()

      MyAgent1.Characters.Load "Genie", "Genie.acs"

      MyAgent1.Characters.Load "Robby", "Robby.acs"

      Set Genie = MyAgent1.Characters ("Genie")
      Set Robby = MyAgent1.Characters ("Robby")

      Genie.Show

      Genie.Speak "Just a moment"

      Set GenieRequest = Genie.Play ("Processing")

      Robby.Show
      Robby.Play "confused"
      Robby.Speak "Hey, Genie. What are you doing?"
      Robby.Interrupt GenieRequest

      Genie.Speak "I was just checking on something."

   End Sub
```



Vous ne pouvez pas interrompre l’animation du même caractère que celui que vous spécifiez dans cette méthode, car le serveur met en file d’attente la méthode d' **interruption** dans la file d’attente d’animation de ce caractère. Par conséquent, vous ne pouvez utiliser l' **interruption** que pour arrêter l’animation d’un autre caractère que vous avez chargé.

Si vous déclarez une référence d’objet et que vous la définissez sur cette méthode, elle retourne un objet de [**requête**](/windows/desktop/lwef/the-request-object) .

> [!Note]  
> **Interrupt** n’efface pas la file d’attente du caractère ; il arrête l’animation existante et passe à l’animation suivante dans la file d’attente du caractère. Pour arrêter et vider la file d’attente d’un caractère, utilisez la méthode [**Stop**](stop-method.md) .

 

## <a name="see-also"></a>Voir aussi

[**Stop, méthode**](stop-method.md)


 

 