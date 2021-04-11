---
title: Utilisation du basculement de flux d’événements en temps réel
description: Utilisation du basculement de flux d’événements en temps réel
ms.assetid: fa8af007-2db6-438f-9551-8e748bb79ef4
keywords:
- Sélections de métafichiers Windows Media, basculement de flux d’événements en direct
- sélections, basculement de flux d’événements en direct
- sélections de métafichiers, basculement de flux d’événements en direct
- Sélections de métafichiers Windows Media, basculement de flux d’événements
- sélections, basculement de flux d’événements
- sélections de métafichiers, basculement de flux d’événements
- Sélections de métafichiers Windows Media, insertion de publicités
- sélections, insertion de publicités
- sélections de métafichiers, insertion de publicités
- Windows Media Player, basculement de flux d’événements en direct
- Lecteur Windows Media, basculement de flux d’événements
- Windows Media Player, insertion de publicités
- basculement de flux d’événements en direct
- basculement de flux d’événements
- insertion de publicité
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fd5c586e0f1ef2b36913dee822e461daeffbfcbf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104190961"
---
# <a name="using-live-event-stream-switching"></a>Utilisation du basculement de flux d’événements en temps réel

La diffusion multimédia en continu peut également être contrôlée par l’interaction des commandes de script incorporées dans un flux de média avec des éléments de métafichier Windows Media dans une sélection de métafichiers.

Un événement est un type particulier de commande de script incorporé dans un flux multimédia ou un fichier multimédia. Lorsque le contrôle du lecteur Windows Media reçoit la commande de script, il traite l’événement comme défini par l’élément d' **événement** dans la sélection du métafichier. Le lecteur Windows Media passe du flux actuel qu’il affiche et génère le rendu du contenu référencé dans l’élément d' **événement** de sélection de métafichiers. L’élément **Event** est généralement utilisé dans la production en direct.

Un élément d' **événement** ressemble à un élément d' **entrée** , mais chacun gère la lecture des flux et des fichiers multimédias différemment. L’élément **entry** est utilisé pour créer des sélections. Un fichier de flux ou de média référencé dans un élément d' **entrée** commence à être lu lorsque le flux ou le fichier multimédia référencé dans l' **entrée** précédente se termine. Un flux référencé dans un **événement** est lu uniquement lorsqu’une commande de script spécifique est reçue. Par exemple, lorsque le lecteur Windows Media reçoit une commande de script de type chaîne « EVENT » et la chaîne de commande « AdLINK », il recherche les éléments suivants dans la sélection.


```XML
<EVENT NAME="Adlink" WHENDONE="RESUME"> 
    <ENTRY HREF=mms://www.proseware.com/adlink.wma />
</EVENT>

```



Le lecteur Windows Media passe alors du flux en direct pour lire le fichier de flux ou de média contenu dans l' **événement**, dans ce cas Adlink. WMA. Le code `WHENDONE="RESUME"` indique au lecteur Windows Media de reprendre la lecture du flux précédent quand Adlink. WMA est terminé.

> [!Note]  
> Si vous ne gérez pas chaque événement incorporé dans un flux multimédia ou un fichier multimédia, vous risquez d’obtenir des résultats inattendus.

 

Si vous souhaitez utiliser le basculement de flux d’événements en temps réel, vous devez inclure un élément d' **événement** dans votre sélection pour gérer chaque commande de script d’événement incorporée dans les flux de média ou les fichiers multimédias de votre sélection. Avant de créer votre sélection, vous devez connaître les détails sur les commandes de script incorporées dans votre contenu multimédia numérique. S’il existe une commande de script d’événement que vous souhaitez que le lecteur Windows Media ignore, incluez un élément d' **événement** dans votre sélection pour gérer l’événement, mais faites référence à une URL factice dans le gestionnaire d’événements.

## <a name="ad-insertion"></a>Insertion de publicité

Cette technique peut être utilisée pour l’insertion d’AD. Par exemple, lors d’une diffusion en direct sur Internet d’un jeu de billes, une commande peut être envoyée au début de chaque pause commerciale qui indique à chaque client (lecteur Windows Media) de lire les commerciaux figurant dans sa playlist. Lorsque les clients terminent la lecture des publicités, la playlist demande à chaque client de repasser à la diffusion en direct. Le contenu du support d' **événement** est rendu uniquement lorsque le média de diffusion en continu qui est accédé diffuse des scripts incorporés avec le nom d' **événement** correspondant.

Les possibilités inhérentes au basculement d' **événements** sont plus appréciées en comparant la façon dont les publicités atteignent les visionneuses par le biais d’une diffusion standard, par voie hertzienne, avec la manière dont les publicités peuvent atteindre les spectateurs à l’aide des technologies Windows Media. Historiquement, les annonces Broadcast pouvaient uniquement être ciblées à peu près sur les spectateurs, en utilisant les données de classement comme critère principal. Les publicités envoyées à l’aide des technologies Windows Media peuvent être destinées directement à l’utilisateur cible, car les **événements** et les sélections peuvent être créés à la volée en fonction de l’entrée de l’utilisateur. Pour plus d’informations, consultez Personnalisation de la [distribution des médias](personalizing-media-delivery.md).

Vous pouvez également utiliser des sélections de métafichiers pour afficher des graphiques, du son et du texte personnalisés pour la publicité. Vous pouvez utiliser l’élément **bannière** comme élément enfant d’un **événement** pour afficher un graphique de message publicitaire. L’élément **Banner** fournit le chemin d’accès et le fichier contenant les graphiques de votre bannière publicitaire. Vous pouvez également fournir un lien vers un site ou un fichier à l’aide de l’élément enfant **moreinfo** . L’URL de l’élément **moreinfo** peut fournir un lien vers d’autres publications sur le Web. L’exemple suivant illustre l’utilisation de ces éléments.

Exemple de code


```XML
<BANNER HREF="SomePath\2.gif">
    <ABSTRACT>Read This Ad and Buy.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



L’exemple suivant insère le. WMA ad dans le flux de diffusion en continu de diffusion BallGame lorsqu’un client reçoit un **événement** de commande de script avec l’attribut de **nom** défini sur « délai d’attente ». **CLIENTSKIP** est défini sur non pour empêcher la publicité diffusée en continu d’être ignorée. Dans cet exemple, la publicité diffusée en continu doit être lue avant de retourner au flux d’origine. Une fois la publicité terminée, le client reprend le flux d’origine.

Exemple de code


```XML
<ASX VERSION="3.0">
    <ENTRY>
        <REF HREF="mms://proseware.com/BallGame" />
    </ENTRY>
    <EVENT NAME="Time-Out" WHENDONE="RESUME">
        <ENTRY>
            <REF HREF = "mms://proseware.com/Advert.wma" 
                CLIENTSKIP = "NO" />
       </ENTRY>
    </EVENT>
</ASX>

```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Sélections de métafichiers**](metafile-playlists.md)
</dt> <dt>

[**Utilisation des sélections de métafichiers**](using-metafile-playlists.md)
</dt> <dt>

[**Informations de référence sur les éléments de métafichier Windows Media**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Guide des métafichiers Windows Media**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




