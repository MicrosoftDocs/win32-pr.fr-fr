---
description: Remplacements de fréquence
ms.assetid: 0e45d0a6-3c3e-462c-a8dc-c4f25b614b85
title: Remplacements de fréquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57177e4990cb40be271fc551718964faf1696d2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520660"
---
# <a name="frequency-overrides"></a>Remplacements de fréquence

Un effort considérable a été passé pour s’assurer que les fréquences de diffusion et les affectations standard de couleur sont correctes pour chaque pays/région. Même dans ce cas, il y a des situations où les tables de fréquence ne sont pas suffisantes, qui contiennent des erreurs ou qui deviennent obsolètes. Pour résoudre ce problème, les fréquences listées dans les tables de fréquence du filtre Tuner TV peuvent être substituées sélectivement, à l’aide de la clé de Registre suivante :

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Microsoft** \\ **TV System services** \\ **TVAutoTune** \\ **TS0-1**

> [!Note]  
> À compter de Windows 7, la clé de Registre redirigée suivante est utilisée pour les applications x86 s’exécutant sur les versions x64 de Windows :

 

**HKEY \_ Logiciel de l' \_ ordinateur local** \\  \\ **Wow6432Node** \\ **Microsoft** \\ **TV System services** \\ **TVAutoTune** \\ **TS0-1**

Les remplacements de fréquence sont regroupés dans des « espaces de paramétrage » définis par l’application, qui sont identifiés par un nombre. L’exemple suivant montre un exemple de substitution :

``` syntax
HKEY_LOCAL_MACHINE\Software\Microsoft\TV System Services\TVAutoTune\TS0-1
"12"=dword:04022750
```

Dans ce cas, « TS0-1 » indique l’espace de réglage 0 pour les fréquences de câble. Le premier numéro identifie l’espace de réglage. Le deuxième nombre est 0 pour les fréquences de diffusion ou 1 pour les fréquences de câble.

La sous-clé nommée « 12 » remplace la valeur de fréquence pour la fréquence à l’index 12 dans la table de fréquence actuelle. La valeur de la sous-clé est une valeur **DWORD** qui spécifie la fréquence en Hertz (Hz). Dans cet exemple, la fréquence est définie sur 67,25 MHz. Les remplacements peuvent être définis pour tous les nombres de canaux compris entre 1 et 999 inclus. Si le matériel de paramétrage ne prend pas en charge une fréquence donnée, la demande de réglage échoue.

Ce mécanisme peut également être utilisé pour créer des numéros de canaux en dehors de la plage existante dans la table Frequency. La méthode [**IAMTuner :: ChannelMinMax**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-channelminmax) retourne la plage de canaux étendue. Par exemple, si la plage de canaux d’origine était comprise entre 1 et 158 et qu’une substitution de canal de « 200 » est ajoutée au registre, la méthode **ChannelMinMax** retourne 200 comme canal maximal. Dans ce cas, les numéros de canaux de la plage comprise entre 159 et 199 n’ont aucune fréquence affectée. par conséquent, les demandes de paramétrage de cette plage échouent automatiquement.

La méthode [**IAMTuner ::p ut \_ TuningSpace**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_tuningspace) permet à l’application de choisir le jeu de remplacements et les informations de réglage précis à utiliser. Les numéros d’espace de paramétrage sont arbitraires. L’application est responsable de la gestion de la relation entre l’espace de réglage et la table de fréquence. L’approche la plus simple consiste à utiliser le code de pays/région comme nombre d’espaces de réglage. Ensuite, chaque fois que l’application bascule vers un nouveau code de pays/région, elle bascule également vers le même espace de paramétrage (dans cet ordre).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réglage de la TV analogique internationale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



