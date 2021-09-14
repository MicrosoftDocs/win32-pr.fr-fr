---
title: Événement Player. commande
description: L’événement commande se produit lors de la réception d’une commande ou d’une URL synchronisée. | Événement Player. commande
ms.assetid: d3aec4e2-1b0e-414e-8113-0af4fcd37e3b
keywords:
- Lecteur Windows Media d’événements commande
- Lecteur Windows Media d’événements commande, classe Player
- Lecteur Windows Media de classe Player, événement commande
topic_type:
- apiref
api_name:
- Player.ScriptCommand
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f9ca7ec22694956e1d91d055e8db057a91ecca4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008357"
---
# <a name="playerscriptcommand-event"></a>Événement Player. commande

L’événement **commande** se produit lors de la réception d’une commande ou d’une URL synchronisée.

## <a name="syntax"></a>Syntaxe


```JScript
Player.ScriptCommand(
  scType,
  Param
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*scType* 
</dt> <dd>

Chaîne spécifiant le type de commande de script.

</dd> <dt>

*Envoyés* 
</dt> <dd>

**Chaîne** spécifiant la commande de script.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Cet événement ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

les commandes peuvent être incorporées parmi les sons et les images d’un fichier ou d’un flux de média Windows. Les commandes sont une paire de chaînes Unicode associées à une heure désignée dans le flux. lorsque le flux atteint l’heure associée à la commande, le contrôle Lecteur Windows Media envoie un événement **commande** avec deux paramètres. Un paramètre spécifie le type de commande en cours d’envoi, tandis que l’autre paramètre spécifie la commande. Le type de paramètre est utilisé pour déterminer la façon dont le paramètre de commande est traité. Tout type de commande peut être incorporé dans un fichier ou un flux à gérer par l’événement **commande** .

le tableau suivant répertorie les types de commande de script qui sont traités automatiquement par Lecteur Windows Media.



| Type                   | Description                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CAPTION                | Le contrôle affiche le texte associé dans la balise DIV spécifiée par *ClosedCaption*. **captioningID**.                                                                  |
| ÉVÉNEMENT                  | Indique au contrôle d’exécuter les instructions définies pour l’événement spécifié.                                                                                          |
| FILENAME               | Le contrôle réinitialise sa propriété **URL** , tente d’ouvrir le fichier spécifié et commence à lire immédiatement le nouveau flux.                                        |
| OPENEVENT              | Met en mémoire tampon la commande de type d’événement associée pour l’exécution en temps opportun du script d’événement.                                                                                 |
| SYNCHRONIZEDLYRICLYRIC | Le paramètre *param* contient le texte Lyric synchronisé. Lecteur Windows Media affiche le texte lyric dans la zone de légende fermée de la fonctionnalité de **diffusion** en cours. |
| TEXT                   | Le contrôle affiche le texte associé dans la balise DIV spécifiée par *ClosedCaption*. **captioningID**.                                                                  |
| URL                    | le contrôle ouvre automatiquement l’URL spécifiée à l’aide du navigateur Internet par défaut si le *Paramètres*. la propriété **invokeURLs** a la valeur true.                      |



 

Vous pouvez incorporer n’importe quel autre type de commande tant que vous fournissez du code réciproque pour gérer la commande. bien que les commandes inconnues soient ignorées par le contrôle Lecteur Windows Media, elles sont toujours transmises à l’événement **commande** .

les commandes d’URL reçues par le contrôle Lecteur Windows Media sont automatiquement appelées dans votre navigateur Web par défaut si le *Paramètres*. la propriété **invokeURLs** a la valeur true. vous pouvez utiliser la *Paramètres*. propriété **defaultFrame** pour spécifier le frame cible dans lequel la page Web s’affiche.

l’url envoyée à Lecteur Windows Media est traitée par rapport à l’url de base spécifiée par le *Paramètres*. propriété **baseURL** . L’URL de base est concaténée avec l’URL relativement spécifiée, ce qui génère une URL entièrement spécifiée qui est transmise en tant que paramètre de commande par l’événement **commande** .

le contrôle Lecteur Windows Media traite toujours les commandes de type URL entrantes de la manière suivante :

1.  Une commande de type URL est reçue.
2.  *Paramètres*. **baseURL** est utilisé pour créer une URL complète à partir de l’URL relative spécifiée dans la commande de script.
3.  *Commande* est appelé.
4.  une fois *commande* retourné, *Paramètres*. **invokeURLs** est activé.
5.  si *Paramètres*. **invokeURLs** a la valeur true et la commande est un type d’URL, l’URL spécifiée est appelée. si *Paramètres*. **invokeURLs** a la valeur false ou, si la commande n’est pas un type d’URL, la commande est ignorée.

lors de la création d’un fichier multimédia Windows, vous pouvez spécifier le cadre dans lequel la nouvelle URL est affichée en concaténant deux et et le nom du cadre dans le champ paramètre. L’exemple ci-dessous illustre les paramètres *commande* typiques. Il spécifie que l’URL *MyPage* doit être lancée dans le frame *MyFrame* .


```JScript
scType = "URL"
Param = https://myweb/mypage.html&&myframe

```



L’événement commande n’est pas appelé si le fichier est en cours d’analyse (transfert rapide ou retour rapide).

la valeur des paramètres d’événement est spécifiée par Lecteur Windows Media, et est accessible ou passée à une méthode dans un fichier JScript importé à l’aide du nom de paramètre donné. Ce nom de paramètre doit être tapé exactement comme indiqué, y compris la mise en majuscules.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure.<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet Player**](player-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> <dt>

[**Paramètres. baseURL**](settings-baseurl.md)
</dt> <dt>

[**Paramètres. defaultFrame**](settings-defaultframe.md)
</dt> <dt>

[**Paramètres. invokeURLs**](settings-invokeurls.md)
</dt> </dl>

 

 





