---
description: Avantages de DMOs
ms.assetid: 7ff3fd9c-9423-4915-8ce2-22783ed455fb
title: Avantages de DMOs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972b4f49ee19b271cbee970401933b6c7d6bd3ca
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111446"
---
# <a name="benefits-of-dmos"></a>Avantages de DMOs

DMOs offre les avantages suivants :

-   elles sont généralement plus petites et plus simples que les filtres DirectShow, car elles prennent en charge moins de fonctionnalités.
-   elles sont plus flexibles que les filtres de DirectShow, car elles ne nécessitent pas de graphique de filtre. vous pouvez les utiliser avec DirectShow lorsque vous avez besoin des services fournis par DirectShow, tels que la synchronisation, la connexion intelligente, le traitement automatique des données et la gestion des threads. Les clients qui n’ont pas besoin de ces services peuvent accéder directement à DMOs.
-   DMOs effectue toujours le traitement synchrone des données, ce qui élimine la plupart des problèmes de thread que vous devez prendre en compte si vous écrivez un filtre.
-   Contrairement aux codecs ACM et VCM traditionnels, les DMOs sont basés sur le modèle COM (Component Object Model), de sorte qu’ils peuvent être étendus via **QueryInterface**.
-   DMOs prennent en charge un modèle de diffusion en continu plus généralisé que les codecs ACM ou VCM. à l’instar des filtres DirectShow, DMOs peut prendre en charge plusieurs entrées et sorties.

Pour ces raisons, DMOs est maintenant recommandé comme solution pour écrire des encodeurs, des décodeurs et des effets audio. De nombreux autres scénarios sont également possibles, selon les besoins de l’application.

différences entre les DMOs et les filtres DirectShow

les filtres de DirectShow ne peuvent pas fonctionner en dehors d’un graphique de filtre DirectShow. dans DirectShow, le gestionnaire de Graph de filtre entre l’application et les filtres. les filtres de DirectShow effectuent la majeure partie du travail nécessaire pour diffuser des données en continu, notamment :

-   Allocation des tampons.
-   Négociation des types de médias et des connexions à d’autres filtres.
-   Transmission de données via le graphique de filtre.
-   envoi d’événements au gestionnaire de Graph de filtres.
-   Synchronisation de plusieurs threads.

en revanche, une DMO n’effectue aucune de ces opérations. Au lieu de cela, ces types de tâches sont la responsabilité du client à l’aide de l’DMO. Le client alloue des tampons, les remplit avec les données et les remet au DMO. le DMO traite les données et le client récupère les mémoires tampons de sortie résultantes.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de DMOs](about-dmos.md)
</dt> </dl>

 

 



