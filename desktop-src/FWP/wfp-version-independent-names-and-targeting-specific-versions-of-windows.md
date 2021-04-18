---
title: Noms de Version-Independent WFP et ciblant des versions spécifiques de Windows
description: Dans de nombreux cas, l’API WFP (Windows Filtering Platform) fournit plusieurs versions d’une fonction ou d’une structure.
ms.assetid: FBDF53E5-F7DE-4DEB-AC18-6D2BB59FE670
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41be83a50b4786aa4b98cd7f8dd7405a33fe94be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106509368"
---
# <a name="wfp-version-independent-names-and-targeting-specific-versions-of-windows"></a>Noms de Version-Independent WFP et ciblant des versions spécifiques de Windows

Dans de nombreux cas, l’API WFP (Windows Filtering Platform) fournit plusieurs versions d’une fonction ou d’une structure.

La plupart des noms de données et de fonctions dans l’API WFP se terminent par un numéro de version, tel que « 0 » ou « 1 », même s’il n’y a qu’une seule version.

## <a name="version-mapping-in-fwpvih"></a>Mappage de version dans fwpvi. h

Le fichier d’en-tête fwpvi. h est inclus à partir du kit de développement logiciel (SDK) Windows 7 et de WDK. Ce fichier d’en-tête mappe le nom de l’API sans version à la version appropriée pour une utilisation avec un système d’exploitation donné.

Par exemple, voici un bref extrait de la version de fwpvi. h inclus dans le kit de développement logiciel (SDK) Windows 8.


```C++
#define FwpmNetEventCreateEnumHandle FwpmNetEventCreateEnumHandle0
#if (NTDDI_VERSION >= NTDDI_WIN8)
#define FwpmNetEventEnum FwpmNetEventEnum2
#elif (NTDDI_VERSION >= NTDDI_WIN7)
#define FwpmNetEventEnum FwpmNetEventEnum1
#else
#define FwpmNetEventEnum FwpmNetEventEnum0
#endif
```



Comme indiqué ci-dessus, il n’existe qu’une seule version de **FwpmNetEventCreateEnumHandle** – [**FwpmNetEventCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventcreateenumhandle0) : tout appel à **FwpmNetEventCreateEnumHandle** appellera toujours **FwpmNetEventCreateEnumHandle0**, quel que soit le système d’exploitation ciblé.

Toutefois, il existe trois versions de **FwpmNetEventEnum**: [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0), [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1)et [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2). Le fichier d’en-tête fwpvi. h garantit qu’un appel à **FwpmNetEventEnum** appellera la version la plus appropriée pour le système d’exploitation ciblé :

-   [**FwpmNetEventEnum2**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum2) pour Windows 8 (ou version ultérieure)
-   [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) pour Windows 7 est ciblé
-   [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) pour les systèmes d’exploitation antérieurs (tels que Windows Vista ou Windows Vista avec Service Pack 1 (SP1))

## <a name="calling-version-independent-functions-and-structures"></a>Appel de fonctions et de structures Version-Independent

Les développeurs WFP ciblant une version de système d’exploitation ou WDK particulière sont encouragés à toujours programmer les macros indépendantes de la version. Cette opération sélectionne automatiquement la dernière version prise en charge dans le système d’exploitation que vous ciblez. L’utilisation des fichiers d’en-tête les plus récents est recommandée, même lorsque vous ciblez un système d’exploitation antérieur. Cela permet de garantir que la dernière version prise en charge est utilisée et peut également faciliter la maintenance et la mise à jour de votre code.

La [documentation de référence sur les API WFP](fwp-reference.md) décrit chaque version d’une API numérotée. Si plusieurs versions existent, le système d’exploitation ciblé est noté. Toutefois, les développeurs veulent généralement appeler les API indépendantes de la version (sans nombre) et indiquer le système d’exploitation ciblé (tel que **NTDDI \_ win6** pour Windows Vista ou **NTDDI \_ WIN8** pour Windows 8).

Pour garantir une gestion correcte des fonctions qui acceptent des paramètres différents dans différentes versions, vous pouvez inclure des blocs conditionnels tels que `#if (NTDDI_VERSION >= NTDDI_WIN7)` .

 

 




