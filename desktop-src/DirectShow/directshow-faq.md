---
description: FAQ DirectShow
ms.assetid: 198758b9-025a-44af-958c-9ddea8cbb12d
title: FAQ DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7d0959c4abb24509edd9c26d111e80a5af221d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521796"
---
# <a name="directshow-faq"></a>FAQ DirectShow

Cet article répond à de nombreuses questions fréquemment posées sur Microsoft DirectShow.

**Quels sont les systèmes d’exploitation pris en charge par DirectShow ?**

DirectShow est disponible dans toutes les versions prises en charge de Windows.

**Combien de connaissances COM ai-je besoin pour programmer avec DirectShow ?**

Pour le développement d’applications, vous devez comprendre les principes de base de l’utilisation des objets COM : comment les instancier, accéder aux interfaces qu’elles exposent et gérer les décomptes de références sur ces interfaces. Le développement de filtres requiert davantage de connaissances COM.

**Quels sont les formats pris en charge par DirectShow ?**

Consultez [formats pris en charge dans DirectShow](supported-formats-in-directshow.md).

**Existe-t-il une liste de compatibilité matérielle (HCL) DirectShow ?**

Non. DirectShow utilise les fonctionnalités matérielles Microsoft DirectDraw et Microsoft DirectSound s’ils sont disponibles. Quand aucun matériel spécial n’est disponible, DirectShow utilise GDI pour dessiner une vidéo  et les \* API multimédias WaveOut pour la lecture audio.

**Quelles langues puis-je utiliser pour écrire une application DirectShow ?**

DirectShow est conçu principalement pour le développement C++. Un petit sous-ensemble de l’API DirectShow est exposé via Visual Basic 6,0 ; Toutefois, cette fonctionnalité est déconseillée.

**DirectShow sera-t-il jamais accessible via du code géré ?**

Microsoft n’a pas de plan actuel pour implémenter une API DirectShow gérée.

**Quel compilateur ai-je besoin pour le développement DirectShow ?**

Tout compilateur qui peut générer des objets COM (Component Object Model) doit fonctionner une fois que l’environnement du compilateur a été configuré correctement.

**Comment DirectShow est-il lié à Microsoft DirectX ?**

En interne, DirectShow utilise DirectSound et DirectDraw lorsque le matériel le prend en charge. Les filtres de mélangeur vidéo et de mixage de superposition utilisent des surfaces DirectDraw 3 et DirectDraw 5. Le convertisseur de mixage vidéo 7 (Windows XP uniquement) utilise des surfaces DirectDraw 7. Le convertisseur de mixage vidéo 9 et le convertisseur vidéo amélioré utilisent les API Microsoft Direct3D les plus récentes. Vous n’avez pas besoin d’utiliser les autres API DirectX pour écrire une application DirectShow, bien qu’il soit possible de les combiner.

**Comment DirectShow est-il lié à Microsoft ActiveMovie ?**

ActiveMovie était le nom d’origine de DirectShow. Le terme ActiveMovie n’est plus utilisé.

**Le code source de l’utilitaire GraphEdit est-il disponible ? GraphEdit peut-il être redistribué ?**

Non, la source n’est pas disponible et Graphedt.exe n’est pas redistribuable.

**DMOs remplacer les filtres DirectShow ?**

Microsoft DirectX Media Objects (DMOs) peut être utilisé dans une application DirectShow. Pour les encodeurs, les décodeurs et les effets, il est recommandé d’écrire un DMO au lieu d’un filtre DirectShow. (Remarque : Si vous souhaitez utiliser l’accélération vidéo DirectX dans votre décodeur, vous devez l’implémenter en tant que filtre.) À d’autres fins, un filtre DirectShow peut être plus approprié. Pour plus d’informations sur DMOs, consultez [objets multimédia DirectX](directx-media-objects.md).

**Je lit un fichier de format AVI avec le lecteur Windows Media. Je peux entendre le son, mais il semble qu’il n’y ait pas de vidéo. à la place, je ne vois que le noir. Qu'est-ce qui ne va pas?**

Probablement, le fichier a été encodé avec un codec qui n’est pas présent sur votre système. Bien que le format de fichier AVI soit courant, il est possible de créer des fichiers AVI avec de nombreux formats de compression (codecs). Si vous tentez de lire un fichier AVI qui utilise un codec non pris en charge, vous pouvez entendre le composant audio, mais la vidéo s’affichera sous la forme d’un écran noir ou le contenu de l’écran restera inchangé.

> [!Note]  
> Le lecteur Windows Media tente souvent de télécharger et d’installer un codec s’il n’est pas présent sur votre système.

 

**Comment faire générer mon application ? De quelles bibliothèques et fichiers d’en-tête ai-je besoin ?**

Consultez [configuration de l’environnement de génération](setting-up-the-build-environment.md).

**GraphEdit affiche un grand nombre de filtres qui ne sont pas documentés. Qu’est-ce que ces filtres ?**

GraphEdit énumère tous les filtres inscrits sur votre système dans une catégorie de filtre. Il peut s’agir de filtres installés par des applications tierces ou installés par d’autres technologies Microsoft, telles que Windows Media ou NetMeeting. En outre, certains filtres DirectShow jouent le rôle de wrappers pour les codecs ou les périphériques matériels, chaque codec ou périphérique étant considéré comme un filtre distinct. Le codec vidéo Microsoft H. 263 est utilisé par NetMeeting et n’est plus pris en charge dans DirectShow. Pour plus d’informations, consultez [énumération des appareils et des filtres](enumerating-devices-and-filters.md).

**Je ne parviens pas à créer mon graphique personnalisé par programmation.**

Essayez d’abord de créer le graphique de filtre avec GraphEdit. Cet outil vous permet de simuler un grand nombre de possibilités rapidement. GraphEdit est toujours l’emplacement idéal pour tester le graphique avant de tenter de le générer avec le code source.

Pour plus d’informations sur la création de graphiques, consultez les articles suivants :

-   [Génération du graphique de filtre](building-the-filter-graph.md)
-   [Énumération d’objets dans un graphique de filtre](enumerating-objects-in-a-filter-graph.md)

**Comment puis-je détecter si DirectShow est installé sur un ordinateur donné ?**

Appelez **CoCreateInstance** pour créer une instance du gestionnaire de graphique de filtre. Si cet appel se déroule correctement, DirectShow est installé sur l’ordinateur. Le code suivant illustre comment procéder :


```C++
IGraphBuilder *pGraph;

HRESULT hr = CoCreateInstance(CLSID_FilterGraph,
    NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void **) &pGraph);
```



**Comment faire modifier les paramètres d’un filtre sans afficher la page de propriétés ?**

La plupart des filtres exposent une ou plusieurs interfaces pour définir des propriétés sur le filtre. Consultez la page de référence du filtre en question. (Voir [filtres DirectShow](directshow-filters.md).)

**Puis-je tester le filtre avec GraphEdit ?**

Lorsque vous développez un filtre, GraphEdit peut vous aider à visualiser les connexions entre les filtres. Il peut également fournir un test rapide des fonctionnalités d’un filtre. Toutefois, il n’est pas conçu comme une plateforme de test robuste.

**À quel moment les filtres de l’anneau des privilèges sont-ils exécutés ?**

Les filtres s’exécutent à l’anneau 3, bien que certains filtres contrôlent les périphériques de diffusion en continu qui s’exécutent à l’anneau 0. Pour plus d’informations, voir [Comment les périphériques matériels participent au graphique de filtre](how-hardware-devices-participate-in-the-filter-graph.md).

**Ai-je besoin d’utiliser un débogueur de noyau ?**

Cela dépend de votre projet spécifique. L’installation des bibliothèques Runtime de débogage DirectX signifie que vous installez des pilotes de débogage et d’autres composants en mode noyau, et que si votre application provoque une assertion de débogage dans l’un de ces composants, votre ordinateur redémarre automatiquement, sauf si un débogueur de noyau est attaché à votre processus.

**Lorsque j’exécute mon application dans le débogueur, elle se bloque.**

Certains décodeurs sont conçus pour ne pas fonctionner pendant que l’application est attachée au débogueur. Essayez d’exécuter l’application en dehors du débogueur.

**Comment \_ fonctionne la macro GUID de définition ?**

La macro **définir le \_ GUID** résout le problème de la déclaration de `extern` références aux valeurs GUID dans votre code source. Supposons, par exemple, que votre projet comporte trois fichiers sources, src1. cpp, src2. cpp et Src3. cpp, et que les trois fichiers utilisent une certaine valeur GUID que vous avez définie. La valeur GUID doit être définie exactement une fois dans votre projet, et les autres fichiers sources doivent déclarer des `extern` références à celle-ci. Avec la macro **définir le \_ GUID** , vous pouvez utiliser le même fichier d’en-tête dans les deux cas. Dans votre fichier d’en-tête, déclarez le GUID comme suit :


```C++
DEFINE_GUID(CLSID_MyObject, 
0x00000000, 0x0000, 0x0000, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00);
```



(Où cet exemple a des zéros, placez les valeurs GUID réelles.) Vous pouvez utiliser l’utilitaire Guidgen.exe pour créer un nouveau GUID et le coller dans le fichier d’en-tête au format **\_ GUID** . Incluez ce fichier d’en-tête dans chaque fichier source qui référence le GUID. Dans exactement l’un des fichiers source, incluez le fichier d’en-tête Initguid. h avant votre fichier d’en-tête. Par exemple :


```C++
// Src1.cpp
#include <initguid.h>
#include "MyGuids.h"

// Src2.cpp
#include "MyGuids.h"

// Src3.cpp
#include "MyGuids.h"
```



Partout où le fichier d’en-tête Initguid. h n’est pas inclus, la macro **définir le \_ GUID** crée une `extern` référence à la valeur Guid. Lorsque le fichier d’en-tête Initguid. h est inclus, il redéfinit la macro **définir le \_ GUID** afin que **définir le \_ GUID** crée une déclaration de définition du GUID.

Si vous n’incluez pas Initguid. h dans aucun des fichiers sources, vous obtiendrez une erreur de lien « symbole externe non résolu ». Si vous incluez Initguid. h deux fois pour le même GUID, vous obtiendrez une erreur de compilation «redéfinition ; initialisation multiple.» Pour résoudre ces erreurs, assurez-vous que Initguid. h est inclus une seule fois. En outre, n’incluez pas Initguid. h dans un fichier d’en-tête précompilé, car en effet, l’en-tête précompilé est inclus dans chaque fichier source.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Présentation de DirectShow](introduction-to-directshow.md)
</dt> </dl>

 

 



