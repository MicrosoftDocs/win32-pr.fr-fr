---
description: Tables de fréquence
ms.assetid: 58a680ea-1f88-4900-8820-c30a2f3e3901
title: Tables de fréquence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 933152c7ac38eefe91468aff8bc3a8eb3ced05df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108542"
---
# <a name="frequency-tables"></a>Tables de fréquence

Le filtre Tuner TV (kstvtune.ax) dispose d’une liste interne de tables de fréquence. Chaque table de fréquence contient une liste de fréquences et correspond aux fréquences de diffusion ou de câble pour un pays ou une région donné. Une application s’adapte à une fréquence particulière en appelant la méthode de [**\_ canal IAMTuner ::p ut**](/windows/desktop/api/Strmif/nf-strmif-iamtuner-put_channel) avec l’index de la fréquence souhaitée.

Pour certains pays ou régions, les numéros d’index des tables de fréquence sont directement mappés aux numéros de canaux. Toutefois, les numéros de canaux fixes ne conviennent pas à tous les marchés. Par exemple, les numéros de canaux européens ne sont pas réellement utilisés par les consommateurs. Au lieu de cela, les consommateurs s’attendent à choisir et à attribuer leurs propres numéros de canaux pour les fréquences utilisées par les opérateurs de diffusion ou de câble dans leur région. Pour ces pays/régions, les applications ne doivent pas exposer les numéros d’index directement à l’utilisateur. Instread, l’application doit conserver un mappage interne entre les numéros de canaux (présenté à l’utilisateur) et les index de fréquence (pour le paramétrage).

La plupart des opérateurs de câble non américains sont libres de diffuser sur les fréquences de leur choix, en mélangeant souvent des fréquences de différentes normes dans la même gamme de canaux. Par conséquent, une table de fréquence « Unicable » est utilisée pour tout pays ou région qui ne dispose pas d’une autorité standard Cable Channel standards. En outre, un mécanisme est fourni pour remplacer les fréquences individuelles dans les tables de fréquence. Ce mécanisme est décrit dans la section suivante, [Overrides de fréquence](frequency-overrides.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Réglage de la TV analogique internationale](international-analog-tv-tuning.md)
</dt> </dl>

 

 



