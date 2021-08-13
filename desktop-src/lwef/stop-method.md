---
title: méthode Stop (fonctionnalités de l’environnement Windows héritées)
description: Stop, méthode
ms.assetid: 68372f72-db9c-447c-a3e4-488940c730d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 572a93db5697aaae0dcfed6b45a834323c106bba447d2d9a8e94109f788af25c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118745961"
---
# <a name="stop-method-legacy-windows-environment-features"></a>méthode Stop (fonctionnalités de l’environnement Windows héritées)

\[Microsoft Agent est déconseillé à partir de Windows 7 et peut ne pas être disponible dans les versions ultérieures de Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descriptive**
</dt> <dd>

Arrête l’animation pour le caractère spécifié.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Stockéesyntaxe**
</dt> <dd>

*agent ***. Caractères («**_CharacterID_*_»). Arrêter_ la *  \[ *requête*\]



| Partie      | Description                                                                                   |
|-----------|-----------------------------------------------------------------------------------------------|
| *Requête* | Facultatif. Objet de [**requête**](/windows/desktop/lwef/the-request-object) spécifiant un appel d’animation particulier. |



 

</dd> </dl>

## <a name="remarks"></a>Remarques

Pour spécifier le paramètre de requête, vous devez créer une variable et assigner la demande d’animation que vous souhaitez arrêter. Si vous ne définissez pas le paramètre de **requête** , le serveur arrête toutes les animations pour le caractère, y compris [**les appels de**](get-method.md) mise en file d’attente, et efface sa file d’attente d’animation, sauf si le caractère est en train de lire son **masquage** ou d' **Afficher** l’animation. Cette méthode n’arrête pas les appels d' **extraction** non mis en file d’attente.

Pour arrêter une animation ou [**obtenir**](get-method.md) un appel spécifique, déclarez une variable objet et affectez votre demande d’animation à cette variable :


```
   Dim MyRequest
   Dim Genie

   Agent1.Characters.Load "Genie", "https://agent.microsoft.com/characters/v2/genie/genie.acf"

   Set Genie = Agent1.Characters ("Genie")

   Genie.Get "state", "Showing"
   Genie.Get "animation", "Greet, GreetReturn"

   Genie.Show
   
   'This animation will never play
   Set MyRequest = Genie.Play ("Greet")
   
   Genie.Stop MyRequest
```



Cette méthode ne génère pas d’objet de [**requête**](/windows/desktop/lwef/the-request-object) .

## <a name="see-also"></a>Voir aussi

[**StopAll, méthode**](stopall-method.md)


 

 
