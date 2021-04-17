---
description: Un autre aspect du développement d’applications à prendre en compte est la différence de comportement entre les opérations locales, intracomputer et le comportement lorsque des opérations se produisent entre deux ordinateurs en réseau.
ms.assetid: e6f48446-948c-458c-8ecf-04ffb249c8a4
title: Comportement de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5a9b871a2c0535d9ef4220824651657332a224a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526212"
---
# <a name="application-behavior"></a>Comportement de l’application

Un autre aspect du développement d’applications à prendre en compte est la différence de comportement entre les opérations locales, intracomputer et le comportement lorsque des opérations se produisent entre deux ordinateurs en réseau. Il existe des comportements d’application qui peuvent fonctionner correctement bien sur un ordinateur local, mais lorsqu’ils sont exécutés sur un réseau, entraînent une dégradation significative des performances et la consommation des ressources. Les comportements d’application suivants doivent être évités lors du développement d’applications Windows Sockets.

## <a name="behaviors-to-avoid"></a>Comportements à éviter

-   Applications bavardes.

    Certaines applications effectuent de nombreuses petites transactions. En cas de combinaison avec la surcharge du réseau associée à chaque transaction, l’effet est multiplié. Dans la mise en réseau, les petites transactions peuvent consommer autant de ressources et autant de fois que de grandes transactions. Une meilleure approche consiste à combiner de nombreuses petites transactions en une seule transaction de grande taille.

-   Transactions sérialisées.

    Une sérialisation inutile des transactions peut entraîner des performances médiocres et un impact sur l’évolutivité. Par exemple, 1000 transactions sérialisées prennent au moins 1000 temps \* RTT pour se terminer. Une meilleure approche consiste à exécuter des transactions non liées en parallèle. Lorsque des applications sérialisées sont associées à des applications bavardes, la réactivité peut être sérieusement gênée.

    > [!Note]  
    > La désérialisation d’une application peut s’avérer difficile. Si la modification de la sérialisation en parallèle prouve trop difficile, envisagez de combiner plusieurs transactions en moins de transactions volumineuses.

     

-   Transactions FAT.

    Les applications qui envoient des octets inutiles sur le réseau sont considérées comme des applications FAT. Les applications qui envoient des octets inutiles sur le réseau augmentent la surcharge du réseau et les performances sont gênées. Cette situation provient souvent de structures de données inefficaces ou d’une diffusion de données inefficace. Pour y remédier, optimisez les structures de données ou envisagez d’utiliser la compression.

Les sections suivantes traitent des aspects du développement d’applications à prendre en compte.

-   [Problèmes spécifiques à TCP/IP](tcp-ip-specific-issues-2.md)
-   [Reconnaître les applications lentes](recognizing-slow-applications-2.md)
-   [Calcul de la surcharge avec netstat](calculating-overhead-with-netstat-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Applications Windows Sockets hautes performances](high-performance-windows-sockets-applications-2.md)
</dt> </dl>

 

 



