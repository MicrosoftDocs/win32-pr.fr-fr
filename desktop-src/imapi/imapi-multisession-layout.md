---
title: Présentation de la multisession IMAPi
description: IMAPi offre aux développeurs d’applications la possibilité de créer des images de système de fichiers ISO 9660 et UDF et de les graver sur CD, DVD et Blu-Ray \ 8482 ; support optique.
ms.assetid: 691fdc3a-e762-4d6d-9980-e2d9227100a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68d816d293a3474f46dc3a48577a46615672103099dc2aa561d393953f29ccf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118249408"
---
# <a name="imapi-multisession-layout"></a>Présentation de la multisession IMAPi

IMAPi offre aux développeurs d’applications la possibilité de créer des images de système de fichiers ISO 9660 et UDF et de les graver sur CD, DVD et disques Blu-Ray™ support optique. avec Windows 7, imapi offre une prise en charge supplémentaire de la gravure multisession sur un DVD et un disque Blu-Ray™ des médias réinscriptibles.

La documentation suivante détaille la disposition du disque que IMAPi utilise pour implémenter la multisession. Ces informations doivent être utilisées pour garantir l’interopérabilité entre IMAPi et d’autres logiciels de gravure, ainsi que pour permettre aux développeurs de ce logiciel de créer des images de disque multisession compatibles IMAPi.

> [!Note]  
> Pour obtenir un exemple détaillant la création d’un disque multisession, consultez [création d’un disque multisession](creating-a-multisession-disc.md).

 

## <a name="multisession-on-sequential-media"></a>Multisession sur un support séquentiel

L’implémentation IMAPi de multisession sur un support séquentiel est prise en charge pour une utilisation avec des médias CD-R, CD-RW, DVD-R, DVD + R et Blu-Ray™. IMAPi utilise le mode d’enregistrement de session à la fois pour CD-RW, et par conséquent, dans ce scénario, le format est considéré comme un type de média séquentiel.

Dans un scénario impliquant la multisession sur un support séquentiel à l’aide de UDF, IMAPi écrit les structures d’ancrage (point de déscripteur de volume d’ancrage UDF-AVDP), les structures de volume (séquence de descripteur de volume UDF-VDS) et les structures de métadonnées du système de fichiers (descripteur de fichier UDF-FSD) au début de chaque nouvelle

![Diagramme qui affiche la structure de métadonnées du système de fichiers avec le point de montage « Import/F S » indiqué par une flèche rouge à l’ancre de la session physique 2.](images/multises1.png)

> [!Note]  
> Cette figure illustre la disposition du disque IMAPi lors de l’utilisation de UDF 2,50 avec des métadonnées redondantes.

 

Les données stockées sur un support enregistré de manière séquentielle consistent en plusieurs sessions physiques. Chaque session contient un système de fichiers complet représentant les données utilisateur sous la forme d’un ensemble de fichiers organisés dans des répertoires. Les métadonnées du système de fichiers se composent d’un certain nombre de structures de données organisées de façon hiérarchique. En haut de la hiérarchie points d’ancrage AVDP situés aux adresses de blocs logiques prédéfinies (LBAs). Les structures d’ancrage spécifient les emplacements des structures de niveau suivant qui n’ont pas d’adresses prédéfinies. Le niveau suivant de hiérarchie après les structures d’ancrage contient les structures de volume (VDS) qui décrivent les propriétés du volume et référencent les structures de métadonnées du système de fichiers (FSD), qui décrivent à leur tour les fichiers et répertoires individuels.

## <a name="multisession-on-rewritable-media"></a>Multisession sur un support réinscriptible

L’approche pour les médias séquentiels décrits dans la section précédente est incompatible avec les médias réinscriptibles (non séquentiels). Ces formats multimédias sont les suivants : DVD-RW, DVD + RW, DVD-RAM, Blu-ray™ réinscriptible et d’autres médias inscriptibles aléatoires, tels que les disques Iomega REV. Les médias réinscriptibles ne prennent pas en charge le concept de sessions physiques correspondant aux sessions logiques, qui sont des incréments individuels validés par une application de mastérisation. Une seule session physique est exposée, qui est une zone commençant au début du disque représentant la zone adressable entière qui a le potentiel de contenir plusieurs sessions logiques.

> [!Note]  
> Bien que DVD-RW soit une exception dans la mesure où il prend en charge le concept de session physique en mode séquentiel, cette fonctionnalité n’est actuellement pas prise en charge par IMAPi.

 

Pour résoudre l’absence de mappage un-à-un entre les sessions physiques et logiques dans les formats réinscriptibles, IMAPi met à jour de manière sélective les structures d’ancrage (AVDP) de la *première* session logique pour pointer vers les nouvelles structures de volume (VDS) et les structures de métadonnées du système de fichiers (FSD) au début de la *dernière* session logique, comme indiqué

![Diagramme qui affiche la structure de métadonnées du système de fichiers avec le point de montage « Import/F S » indiqué par une flèche rouge à l’ancre de la session logique 1.](images/multises2.png)

> [!Note]  
> Cette figure illustre la disposition du disque IMAPi lors de l’utilisation de UDF 2,50 avec des métadonnées redondantes.

 

Lors de l’ajout d’une nouvelle session logique à un disque réinscriptible, IMAPi détermine d’abord la fin de la dernière session logique en analysant les métadonnées de volume (VDS). IMAPi ajoute ensuite la nouvelle session logique, terminée avec les nouvelles (AVDP), le volume (VDS) et les structures de métadonnées du système de fichiers (FSD), physiquement contiguës à la session logique enregistrée précédemment. La dernière étape nécessite que les structures d’ancrage (AVDP) au début de la première session logique soient mises à jour pour pointer vers les structures de volume (VDS) de la *nouvelle* session logique. Le résultat opérationnel est le même que dans le cas d’un média séquentiel.

## <a name="additional-recommendations"></a>Autres recommandations

-   **Disposition de la partition**

    Pour obtenir une compatibilité IMAPi, il est recommandé que les développeurs de logiciels de gravure tiers utilisent les dispositions de disque décrites dans cette documentation. Les développeurs doivent éviter les mises en page avec des partitions de système de fichiers occupant la totalité du disque, car cela nécessite l’enregistrement d’applications pour localiser l’espace libre dans les partitions existantes chaque fois que des données doivent être ajoutées au disque. Souvent, les applications d’enregistrement réalisent cela en utilisant des marqueurs propriétaires sur le disque pour indiquer la quantité d’espace réellement occupée par les données utilisateur. Ces dispositions de disque ne sont pas compatibles avec IMAPi, car les marqueurs propriétaires ne sont pas reconnus en dehors de l’application pour laquelle ils ont été créés.

-   **Type de partition UDF**

    IMAPi utilise le type de partition UDF **en lecture seule** dans son implémentation de multisession sur un média réinscriptible. les développeurs de logiciels de gravure tiers doivent utiliser le type de partition UDF **en lecture seule** pour obtenir une compatibilité avec Windows la gravure maître via imapi. Si un autre type de partition UDF, tel que **réinscriptible** , est utilisé, IMAPI ne peut pas assurer la prise en charge de la maîtrise.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’un disque multisession](creating-a-multisession-disc.md)
</dt> <dt>

[**IMultisessionRandomWrite**](/windows/desktop/api/imapi2/nn-imapi2-imultisessionrandomwrite)
</dt> </dl>

 

 




