---
description: Les objets WMContainer fournissent un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Composants WMContainer ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103952133"
---
# <a name="wmcontainer-asf-components"></a>Composants WMContainer ASF

Les objets WMContainer fournissent un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF (Advanced Systems Format).

Les [composants ASF de la couche de pipeline](pipeline-layer-asf-components.md) utilisent les objets WMContainer en interne. La plupart des applications doivent utiliser les composants de pipeline, plutôt que d’utiliser des objets WMContainer. Utilisez WMContainer uniquement si vous avez besoin d’un contrôle de bas niveau sur l’analyse et l’écriture d’un fichier ASF.

La couche WMContainer comprend les objets suivants :

-   [Profil ASF](asf-profile.md)
-   [Objet ASF ContentInfo](asf-contentinfo-object.md)
-   [Séparateur ASF](asf-splitter.md)
-   [Multiplexeur ASF](asf-multiplexer.md)
-   [Indexeur ASF](asf-index-object.md)

Les rubriques suivantes contiennent des instructions pas à pas sur l’utilisation de WMContainer pour lire ou écrire des fichiers ASF.

-   [Didacticiel : lecture d’un fichier ASF à l’aide d’objets WMContainer](tutorial--reading-an-asf-file.md)
-   [Didacticiel : copie de flux ASF à l’aide d’objets WMContainer](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [Didacticiel : écriture d’un fichier WMA à l’aide d’objets WMContainer](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a>À propos du conteneur WM

Les objets WMContainer interagissent directement avec les objets fichiers ASF. Le diagramme suivant illustre la structure de fichiers ASF et les objets WMContainer correspondants.

![Diagramme montrant la structure des fichiers ASF et les objets Media Foundation correspondants](images/asf-components01.png)

À l’exception du séparateur et du multiplexeur, chacun de ces objets prend en charge l’analyse (lecture) et l’écriture de fichiers ASF. Le séparateur est utilisé uniquement pour lire des fichiers ASF. Le multiplexeur est utilisé uniquement pour la création de fichiers ASF.

Toutes les opérations effectuées par les objets WMContainer sont synchrones, ce qui signifie qu’elles bloquent le thread appelant.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



