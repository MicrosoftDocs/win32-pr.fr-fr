---
description: Collecte d’informations de Fine-Tuning
ms.assetid: 0d9ea896-e0a9-411b-9a10-e366e3686a34
title: Collecte d’informations de Fine-Tuning
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7148724473504631431780f320b1c1852f6de9fe5f8d29b38dca94882f37f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084439"
---
# <a name="collecting-fine-tuning-information"></a>Collecte d’informations de Fine-Tuning

Bien que les fréquences de câble soient généralement exactes, les fréquences de diffusion peuvent être ajustées ou réduites plusieurs kHz par la station de diffusion pour réduire les interférences potentielles avec les canaux voisins.

Lorsque le filtre Tuner TV est réglé sur un canal, il recherche le signal le plus précis. Pour enregistrer ces informations dans le registre pour les opérations de paramétrage suivantes, procédez comme suit :

1.  Appelez [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) pour déterminer la plage d’entrées de fréquence dans la table de fréquence actuelle.
2.  Appelez la méthode [**IAMTuner ::p ut \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) une fois pour chaque index Frequency de la plage.
3.  Appelez [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) pour enregistrer les informations de réglage précis dans le registre. Les informations sont stockées sous la clé de Registre pour l’espace de réglage actuel.

Le code suivant illustre ces étapes :


```C++
long lMin = 0, lMax = 0;
hr = pTuner->ChannelMinMax(&lMin, &lMax);
if (SUCCEEDED(hr))
{
    for (long i = lMin; i <= lMax; i++)
    {
        pTuner->put_Channel(i, AMTUNER_SUBCHAN_DEFAULT,
            AMTUNER_SUBCHAN_DEFAULT)
    }
    pTuner->StoreAutoTune();
}
```



Avec les versions antérieures du filtre Tuner TV, la méthode [**IAMTVTuner :: Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) était recommandée pour le réglage précis. Toutefois, cette méthode ignore toutes les substitutions de fréquence, donc son utilisation n’est plus recommandée. Le code suivant est équivalent à la méthode **Autotune** , mais fonctionne correctement avec les remplacements de fréquence :


```C++
HRESULT MyAutoTune(IAMTVTuner *pTuner, long lIndex, long *plFoundSignal)
{
    long SignalStrength = AMTUNER_NOSIGNAL;
    HRESULT hr;
    hr = pTuner->put_Channel(lIndex, AMTUNER_SUBCHAN_DEFAULT, AMTUNER_SUBCHAN_DEFAULT);
    if (NOERROR == hr)
        pTuner->SignalPresent(&SignalStrength);
    *plFoundSignal = (SignalStrength != AMTUNER_NOSIGNAL);
        return hr;
}
```



Avec la réception par diffusion, il n’est pas toujours possible d’obtenir un verrou horizontal, bien que l’image soit visible. Dans ce cas, le matériel tuner aura un verrou de fréquence, mais le décodeur n’aura pas de verrou horizontal. Cette condition peut être détectée lors de l’utilisation de l' [**instruction Put \_ Channel**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) ou [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) en examinant le code de retour.



| Valeur    | Description                                                                                                                                                                               |
|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_OK    | L’opération de réglage a réussi et le tuner a obtenu un verrou de fréquence.                                                                                                                          |
| S \_ false | Aucune erreur ne s’est produite pendant l’opération de réglage, mais le tuner n’a pas pu obtenir un verrou de fréquence. Il est très improbable qu’il y ait un canal affichable résultant de cette opération. |



 

Tout autre code de retour indique qu’une erreur s’est produite.

Une valeur de retour de S \_ OK ne garantit pas que le décodeur a un verrou horizontal. La méthode [**Autotune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-autotune) met à jour le paramètre *FoundSignal* pour indiquer si le verrou horizontal a été atteint ou non. La méthode [**IAMTuner :: SignalPresent**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-signalpresent) retourne les mêmes informations.

Toutefois, lorsque la valeur de retour est \_ OK, l’application a la possibilité d’ignorer le paramètre *FoundSignal* , car le tuner signale un verrou de fréquence. Il existe une possibilité de verrou de fréquence sur le bruit, mais cette possibilité doit être pesée par rapport à la possibilité d’ignorer les canaux affichables.

## <a name="registry-conversion"></a>Conversion du Registre

Pour prendre en charge les remplacements de fréquence, le format interne de la clé de Registre qui contient des informations de réglage précis a changé. Le format d’origine est toujours pris en charge pour la compatibilité descendante, mais il ne prend pas en charge les remplacements de fréquence.

L’ancien format de Registre est converti au nouveau format chaque fois que la méthode [**IAMTVTuner :: StoreAutoTune**](/windows/desktop/api/Strmif/nf-strmif-iamtvtuner-storeautotune) est appelée. Si votre application ajoute des remplacements de fréquence, elle doit appeler la méthode **StoreAutoTune** pour effectuer la conversion vers le nouveau format de registre. Il n’est pas nécessaire de collecter des informations de réglage précis avant d’appeler **StoreAutoTune**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réglage de la TV analogique internationale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



