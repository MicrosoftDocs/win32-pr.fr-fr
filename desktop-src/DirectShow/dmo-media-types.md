---
description: DMO Types de médias
ms.assetid: 40958e12-09c7-4ce5-aa4d-5ed8b1f40aa3
title: DMO Types de médias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1997abb1cc3c8eb10301778982ef7a46690855ed
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324924"
---
# <a name="dmo-media-types"></a>DMO Types de médias

Un type de média décrit le format associé à un flux de données multimédias. Cet article explique comment DMOs gère les types de médias. Il est principalement destiné aux développeurs qui écrivent leur propre DMOs personnalisé.

les types de média sont définis à l’aide de la structure de [**\_ \_ TYPE de média DMO**](/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type) . Cette structure comprend les informations suivantes :

-   Le *type principal* est un identificateur global unique (Guid) qui définit une catégorie étendue, telle que l’audio ou la vidéo.
-   Le *sous-type* est un GUID qui définit des aspects plus spécifiques du type. Par exemple, dans la vidéo, les sous-types sont les suivants : RVB 16 bits, RVB 24 bits, UYVY, vidéo encodée au format DV, etc.
-   Le *bloc de format* est une structure secondaire qui spécifie le format de manière complète. La disposition du bloc de format dépend du type de données. Par exemple, le son PCM utilise la structure **WAVEFORMATEX** . La vidéo utilise diverses autres structures, notamment **VIDEOINFOHEADER** et **VIDEOINFOHEADER2**. La disposition du bloc de format est identifiée par un GUID de type de format. Par exemple, \_ le format WaveFormatEx spécifie une structure **WaveFormatEx** .

quand un DMO est créé pour la première fois, les flux n’ont pas de type de média. avant que le DMO puisse traiter des données, le client doit définir un type de média pour chaque flux. Ce processus est décrit du point de vue du client dans la [définition des types de média sur un DMO](setting-media-types-on-a-dmo.md).

**Types de médias dans le registre**

un DMO pouvez ajouter une liste de types de médias qu’il prend en charge au registre, en appelant la fonction [**DMORegister**](/previous-versions/windows/desktop/api/Dmoreg/nf-dmoreg-dmoregister) . Une application peut utiliser ces informations pour rechercher des DMOs qui correspondent à un format particulier. Les informations du registre ne sont pas destinées à être complètes. en règle générale, vous incluez uniquement les types principaux que le DMO prend en charge. L’entrée de registre a des clés distinctes pour les types d’entrée et de sortie, mais elle ne fait pas la distinction entre les flux individuels.

la fonction **DMORegister** utilise l’DMO structure de type [**\_ \_ MEDIATYPE partielle**](/previous-versions/windows/desktop/api/Dmoreg/ns-dmoreg-dmo_partial_mediatype) pour décrire les types de médias. cette structure contient un sous-ensemble des informations trouvées dans la structure de **\_ \_ type de média DMO** , à savoir le type principal et le sous-type. Il n’inclut pas de bloc de format, car le bloc de format contient généralement des informations qui sont trop précises pour être incluses dans le registre, telles que la hauteur et la largeur d’une image vidéo.

**Types de médias préférés**

une fois que l’application a créé une DMO, elle peut interroger le DMO pour obtenir les types de média pris en charge. pour chaque flux, le DMO crée une liste de types de médias (éventuellement vides), classés par ordre de préférence. Les méthodes [**IMediaObject :: GetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getinputtype) et [**IMediaObject :: GetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-getoutputtype) énumèrent les types préférés. Les types préférés d’un flux peuvent changer dynamiquement lorsque l’application définit des types de média sur d’autres flux. Par exemple, la liste des types de sortie préférés peut changer une fois que le type d’entrée est défini, ou vice versa. toutefois, le DMO n’est pas requis pour mettre à jour ses types préférés de manière dynamique. L’application ne peut pas supposer que chaque type qu’elle reçoit est valide. Pour cette raison, les méthodes [**IMediaObject :: SetInputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setinputtype) et [**IMediaObject :: SetOutputType**](/previous-versions/windows/desktop/api/Mediaobj/nf-mediaobj-imediaobject-setoutputtype) prennent en charge un indicateur pour tester un type spécifique.

les méthodes **GetInputType** et **GetOutputType** retournent toutes deux une structure de **\_ \_ TYPE de média DMO** . la DMO peut laisser une partie des informations de cette structure vide pour indiquer une plage de types. Le type ou sous-type principal peut être un GUID \_ null, et le bloc de format peut être vide (zéro octet). Si le bloc de format est vide, le type de format doit être GUID \_ null.

une fois que l’application a défini tous les types d’entrée d’un DMO, le DMO doit généralement retourner au moins un type complet pour chaque flux de sortie. Un type de sortie complet facilite les tests, et les applications peuvent l’utiliser comme valeur par défaut raisonnable. l’application de test DMO s’appuie sur ce comportement. (Consultez [utilisation de l’application DMOTest](using-the-dmotest-application.md).)

**Définition des types de médias**

Les applications utilisent les méthodes **SetInputType** et **SetOutputType** pour tester, définir ou effacer des types dans un flux spécifié. L’application doit spécifier entièrement le type. le DMO vérifie s’il peut accepter le type proposé. La réponse peut dépendre des types qui ont été définis sur d’autres flux. le DMO \_ définir \_ l' \_ indicateur clear TYPEF efface le type d’un flux, de sorte que l’application peut « revenir en arrière » et essayer une autre combinaison.

**Exemples de scénarios**

Les exemples suivants décrivent certains scénarios typiques, afin d’illustrer les points des sections précédentes.

-   **Décodeurs vidéo.** Dans un décodeur vidéo classique, le type d’entrée détermine en partie le type de sortie. Par exemple, les deux flux doivent généralement avoir la même fréquence d’images et les mêmes dimensions d’image. L’une des options consiste à ne pas définir de types de sortie préférés tant que le type d’entrée n’est pas défini. Une autre option consiste à énumérer un ensemble de types incomplets, en omettant le bloc de format. Utilisez le sous-type pour indiquer les types non compressés pris en charge, tels que RVB 16 bits, RVB 24 bits, etc. En outre, les décodeurs vidéo ne prennent généralement pas en charge la définition du type de sortie avant le type d’entrée. Le scénario habituel consiste à décoder à partir d’un format d’entrée connu. cette limitation est donc raisonnable.
-   **Décodeurs audio.** Un décodeur audio peut prendre en charge un ensemble limité de formats de sortie. Dans ce cas, il peut être en mesure de créer une liste de formats de sortie préférés avant que le format d’entrée soit connu.
-   **Compresseurs.** Dans la plupart des cas, un compresseur vidéo ne peut pas spécifier entièrement ses formats de sortie préférés tant que l’application n’a pas défini le format d’entrée, et vice versa. au lieu de cela, le DMO doit retourner un type incomplet sans bloc de format. Pour la compression audio et vidéo, l’application doit généralement définir différents paramètres de sortie, tels que la vitesse de transmission. Toutefois, une fois que le type d’entrée est défini, le compresseur doit retourner au moins un type de sortie complet, pour les raisons mentionnées précédemment.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Écriture d’un DMO](writing-a-dmo.md)
</dt> </dl>

 

 



