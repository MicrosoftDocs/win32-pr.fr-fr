---
title: EVENT, élément (kit de développement logiciel (SDK) WMP)
description: L’élément EVENT définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement.
ms.assetid: d12af3bd-a63e-4022-aa84-0386eeef1390
keywords:
- Élément d’événement lecteur Windows Media
topic_type:
- apiref
api_name:
- EVENT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: befc5f8462f66c1b3fbe37f0acf1a35e7f704fbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545361"
---
# <a name="event-element"></a>Élément EVENT

L’élément **Event** définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement.

``` syntax
<EVENT   
   NAME = "text string"
   WHENDONE = "RESUME" | "NEXT" | "BREAK"
>
</EVENT>
```

## <a name="attributes"></a>Attributs

**Nom** (obligatoire)

Nom de l’événement.

**WHENDONE** (obligatoire)

Valeur qui définit ce que le lecteur Windows Media exécute après la lecture du contenu référencé.

Les valeurs suivantes sont possibles.



| Valeur  | Description                                                                                                                                                                                                                     |
|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RESUME | L’entrée actuelle (le clip interrompu par l’événement) reprend son exécution. Si le contenu est stocké, il reprend à l’endroit où il s’est arrêté ; Si le contenu est Broadcast, il reprend à la position actuelle.        |
| NEXT   | L’élément d' **entrée** suivant est lu comme si l’événement ne s’était pas produit et le lecteur Windows Media avait atteint la fin du clip en cours.                                                                                             |
| BREAK  | Si l’entrée actuelle se trouve dans une boucle **REPEAT** , la boucle se termine comme si le nombre de répétitions avait été terminé. Dans le cas contraire, le lecteur Windows Media passe à la fin de la sélection comme si la dernière entrée était terminée normalement. |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy       | Éléments                |
|-----------------|-------------------------|
| Éléments parents | **ASX**                 |
| Éléments enfants  | **entrée**, **ENTRYREF** |



 

## <a name="remarks"></a>Notes

Cet élément définit un comportement ou une action entreprise par le lecteur Windows Media lorsqu’il reçoit une commande de script appelée comme un événement. Un événement est un type particulier de commande de script incorporé dans un flux envoyé au lecteur Windows Media qui se compose d’une chaîne double. La première chaîne est le mot « Event » et la deuxième chaîne est le nom de l’événement. Le nom de l’événement dans la deuxième chaîne doit correspondre au nom de l’événement défini dans le métafichier. (La correspondance n’est pas sensible à la casse.) Les événements peuvent être envoyés au lecteur Windows Media recevant un flux en temps réel, ou enregistrés dans un fichier. ASF,. WMA ou. wmv qui est remis sous forme de flux de monodiffusion à la demande. Lorsque le lecteur Windows Media reçoit la commande de script, il traite l’événement comme défini par l’élément **Event** .

Cet élément définit une étendue d’éléments d' **entrée** ou de **ENTRYREF** qui sont traités chaque fois que le lecteur Windows Media reçoit la commande de script avec l’événement nommé. **ENTRYREF** peut être une URL qui pointe vers une page ASP. Avec cet élément, vous pouvez spécifier un comportement pour le basculement de flux en temps quasi-réel, par opposition aux modifications de flux précréées à l’aide de références à d’autres éléments de contenu ou de sous-fichiers Windows Media.

Lorsque vous utilisez des pages ASP pour générer des sélections, vous devez spécifier une valeur pour la *réponse*. Propriété **ContentType** et la *réponse*. **Expires** dans la page ASP en raison de problèmes de latence avec le lecteur Windows Media. *Réponse*. **ContentType** doit être une extension de nom de fichier valide pour les fichiers Windows Media. Les types valides sont. ASF,. asx,. WMA,. Wax,. wmv et. wvx.

Pour plus d’informations sur l’utilisation de l’objet **Response** dans ASP, consultez le kit de développement Platform SDK.

Cet élément peut apparaître n’importe où dans l’élément **ASX** . Si plusieurs éléments d' **événement** dans un élément **ASX** ont des valeurs identiques pour leurs attributs de **nom** , le lecteur Windows Media utilise la première occurrence dans l’élément **ASX** et ignore tous les autres. Lorsque les éléments d' **événement** ont des attributs de **nom** distincts, leur ordre dans l’élément **ASX** n’a pas d’importance.

Le lecteur Windows Media ignore les événements qu’il reçoit lors du traitement d’un autre événement. L’imbrication d’événements n’est pas prise en charge. Lorsque le lecteur Windows Media est en mode aperçu, le contenu de l’événement n’est pas imposé par l’élément **PREVIEWDURATION** ; la longueur totale du contenu de l’événement peut s’exécuter même si la durée de l’aperçu de l’élément d' **entrée** actif expire avant la fin de l’événement.

## <a name="examples"></a>Exemples

Dans cet exemple, lorsque le lecteur Windows Media reçoit l’événement de commande de script et la chaîne de commande « Adlink » dans le média de diffusion en continu qu’il restitue, il recherche un **EVENTNAME** « Adlink » dans la sélection. Le lecteur Windows Media passe du flux qu’il restitue et lit le contenu référencé dans l' **événement**« https://example.microsoft.com/adlink.htm ».

L’attribut d' **entrée** **CLIENTSKIP** a la valeur no pour empêcher l’omission du clip d' **événement** . Il doit être lu.

Le script `WHENDONE="RESUME"` indique à Windows Media Player de reprendre la lecture du média précédent à partir duquel il est passé à partir du moment où Adlink. ASF est terminé.


```XML
<ASX VERSION="3.0">
<ENTRY CLIENTSKIP="NO">
   <REF HREF="https://example.microsoft.com/clip1.asf" />
</ENTRY>
<EVENT NAME="Adlink" WHENDONE="RESUME">
   <ENTRYREF HREF="https://example.microsoft.com/adlink.htm" 
       CLIENTSKIP="NO" />
</EVENT>
</ASX>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Informations de référence sur les métafichiers Windows Media**](windows-media-metafile-reference.md)
</dt> <dt>

[**Modèle objet du lecteur Windows Media**](windows-media-player-object-model.md)
</dt> </dl>

 

 





