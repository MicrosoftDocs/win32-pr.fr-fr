---
description: Réglage de la télévision analogique
ms.assetid: f4ae76e3-0f61-4a33-8ea4-ef14a117df6a
title: Réglage de la télévision analogique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b85d0826340b913df88cb20dc538bc85943949b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514728"
---
# <a name="analog-television-tuning"></a>Réglage de la télévision analogique

Le réglage est contrôlé par le filtre Tuner TV, via l’interface [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner) . L’interface IAMTVTuner hérite de IAMTuner. Pour obtenir un pointeur vers l’interface, appelez la méthode [**ICaptureGraphBuilder2 :: FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) comme suit :


```C++
IAMTVTuner *pTuner = NULL;
hr = pBuild->FindInterface(
    &LOOK_UPSTREAM_ONLY,  // Look upstream from pCap.
    NULL,                 // No particular media type.
    pCap,                 // Pointer to the capture filter.
    IID_IAMTVTuner, (void**)&pTuner);
if (SUCCEEDED(hr))
{
    // Use pTuner ...
    pTuner->Release();
}
```



Le premier paramètre indique d’effectuer une recherche dans le flux amont à partir du filtre de capture.

Tables de fréquence

En interne, le filtre Tuner TV conserve une liste de tables de fréquence. Chaque table de fréquence correspond aux fréquences de diffusion ou de câble pour un pays ou une région donné. Il existe également une table de fréquence « Unicable » générique, qui est utilisée quand un pays ou une région n’a pas d’affectations de fréquence standard.

Chaque table de fréquence contient une liste de fréquences de paramétrage. Pour certains pays ou régions, les index de la table correspondent directement aux numéros de canaux, en d’autres termes, la fréquence pour le canal n est la n ième entrée dans la table. Pour certains pays ou régions, toutefois, il n’existe pas de correspondance directe entre les numéros de canaux et les fréquences. Dans ce cas, l’application doit conserver une liste qui mappe les numéros de canaux (généralement choisis par l’utilisateur) aux entrées de la table de fréquence. Par exemple, ce que l’utilisateur voit comme « Channel 5 » peut être le numéro d’entrée 12 dans la table Frequency.

Pour plus d’informations, consultez réglage de la [TV analogique internationale](international-analog-tv-tuning.md).

Opérations de paramétrage de base

Si le tuner prend en charge plusieurs modes de réception, tels que la radio TV et FM, appelez [**IAMTuner ::p \_ mode ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_mode) pour sélectionner le mode. La méthode [**IAMTuner :: GetAvailableModes**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-getavailablemodes) retourne tous les modes que le tuner prend en charge. Par exemple, le code suivant vérifie si le tuner prend en charge la radio FM et, le cas échéant, bascule vers ce mode.


```C++
// Check whether the mode is supported.
long lModes = 0;
hr = m_pTuner->GetAvailableModes(&lModes);
if (SUCCEEDED(hr) && (lModes & AMTUNER_MODE_FM_RADIO))
{
    // Set the mode.
    hr = pTuner->put_Mode(AMTUNER_MODE_FM_RADIO);
}
```



Pour définir le pays ou la région, appelez la méthode [**IAMTuner ::p ut \_ CountryCode**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_countrycode) . Le tuner utilise cette valeur pour sélectionner la table de fréquence appropriée. Pour plus d’informations, consultez [affectations de pays/région](country-region-assignments.md) .

Pour définir le canal, appelez la méthode de [**\_ canal IAMTuner ::p ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) . L’argument de cette méthode n’est en fait pas un numéro de canal, mais plutôt un index dans la table de fréquence actuelle. Comme décrit précédemment, le numéro d’index peut ou ne peut pas correspondre à un numéro de canal. La méthode [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) renvoie les valeurs d’index minimale et maximale pour la table de fréquence actuelle.

Remplacement des entrées de fréquence

Il est possible que certaines entrées dans les tables de fréquence soient incorrectes ou deviennent obsolètes. Par conséquent, un mécanisme est fourni pour remplacer des entrées individuelles à l’aide de clés de registre.

Les spécificités sont expliquées dans la rubrique [réglage de TV analogique internationale](international-analog-tv-tuning.md). Chaque clé de Registre définit un « espace de paramétrage » qui contient une ou plusieurs sous-clés. Chaque sous-clé remplace une entrée de fréquence. Pour définir l’espace de réglage actuel, utilisez la méthode [**IAMTuner ::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) . L’activation de l’espace de réglage remplace les entrées de fréquence dans la table de fréquence actuelle. Par conséquent, il revient à l’application de maintenir une correspondance entre les espaces de réglage et les pays/régions. La meilleure approche consiste simplement à utiliser l’identificateur de pays/région comme nom de l’espace de réglage.

Réglage précis des entrées de fréquence

Les fréquences de diffusion peuvent être ajustées ou réduites plusieurs kHz par la station de diffusion pour réduire les interférences potentielles avec les canaux voisins. Compte tenu de la fréquence nominale, la carte tuner peut rechercher la fréquence exacte. Le filtre Tuner TV dispose d’un mécanisme permettant d’enregistrer les fréquences ajustées dans le registre.

Pour chaque entrée de la table Frequency, appelez la \_ méthode put Channel pour régler cette fréquence. Le tuner recherche la fréquence la plus précise. Vous pouvez vérifier si le tuner a atteint un verrou horizontal en appelant [**IAMTuner :: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent). Le filtre Tuner TV stocke également le résultat en interne.

Après avoir analysé toutes les fréquences, appelez la méthode [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) pour écrire les valeurs mises à jour dans le registre. Les valeurs mises à jour sont stockées sous l’entrée de Registre pour l’espace de paramétrage actuel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Télévision analogique](analog-television.md)
</dt> </dl>

 

 



