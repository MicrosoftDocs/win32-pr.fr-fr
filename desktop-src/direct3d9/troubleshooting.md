---
description: Cette rubrique répertorie les catégories courantes de problèmes que vous pouvez rencontrer lors de l’écriture d’applications Direct3D et comment les empêcher.
ms.assetid: 27b87f0f-7118-4252-b6e8-6ea18a9399e4
title: Résolution des problèmes (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6726e761dd8c15e2da18e6c370472a73e82cef0b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513115"
---
# <a name="troubleshooting-direct3d-9"></a>Résolution des problèmes (Direct3D 9)

Cette rubrique répertorie les catégories courantes de problèmes que vous pouvez rencontrer lors de l’écriture d’applications Direct3D et comment les empêcher.

## <a name="device-creation"></a>Création de l’appareil

Si votre application échoue lors de la création de l’appareil, recherchez les erreurs courantes suivantes.

-   Veillez à vérifier les fonctionnalités de l’appareil, en particulier les profondeurs de rendu.
-   Examinez le code d’erreur. D3DERR \_ OUTOFVIDEOMEMORY est toujours possible.
-   Utilisez les bibliothèques de liens dynamiques (dll) de débogage DirectX et passez en revue les messages de sortie sous le débogueur.

## <a name="using-lit-vertices"></a>Utilisation des vertex allumés

Les applications qui utilisent des vertex allumés doivent désactiver le moteur d’éclairage Direct3D en affectant la \_ **valeur false** à l’état de rendu d’éclairage D3DRS. Par défaut, lorsque l’éclairage est activé, le système définit la couleur de tout vertex qui ne contient pas de vecteur normal à 0 (noir), même si le vertex d’entrée contenait une valeur de couleur différente de zéro. Étant donné que lit-vertex ne contient pas, par nature, un sommet normal, toutes les informations de couleur transmises à Direct3D sont perdues pendant le rendu si le moteur d’éclairage est activé.

Évidemment, la couleur de vertex est importante pour toute application qui effectue sa propre lumière. Pour empêcher le système d’imposer les valeurs par défaut, veillez à définir l' \_ éclairage D3DRS sur **false**.

Si votre application s’exécute mais que rien n’est visible, recherchez les erreurs courantes suivantes.

-   Assurez-vous que vos triangles ne sont pas dégénérées.
-   Assurez-vous que vos triangles ne sont pas éliminés.
-   Assurez-vous que vos transformations sont cohérentes en interne.
-   Vérifiez les paramètres de la fenêtre d’affichage pour vous assurer qu’ils permettent d’afficher vos triangles.

## <a name="debugging"></a>Débogage

Le débogage d’une application Direct3D peut s’avérer difficile. Essayez les techniques suivantes, en plus de vérifier toutes les valeurs de retour, un Conseil particulièrement important dans la programmation Direct3D, qui dépend des implémentations matérielles très différentes.

-   Basculez vers les dll de débogage.
-   Forcez un périphérique logiciel uniquement, en désactivant l’accélération matérielle, même lorsqu’elle est disponible.
-   Forcez les surfaces dans la mémoire système.
-   Créez une option pour qu’elle s’exécute dans une fenêtre, afin que vous puissiez utiliser un débogueur intégré.

Les deuxième et troisième options de cette liste peuvent vous aider à éviter le verrou Win16 qui peut entraîner le blocage de votre débogueur.

Essayez également d’ajouter les entrées suivantes à Win.ini.


```
[Direct3D] 
debug=3 
[DirectDraw] 
debug=3 
```



## <a name="borland-floating-point-initialization"></a>Initialisation de Borland Floating-Point

Les compilateurs de Borland signalent des exceptions de virgule flottante d’une manière incompatible avec Direct3D. Pour résoudre ce problème, incluez un \_ Gestionnaire d’exceptions matherr comme suit :


```
// Borland floating point initialization 
#include <math.h>
#include <float.h>

void initfp(void)
{
    // Disable floating point exceptions
    _control87(MCW_EM,MCW_EM);
}

int _matherr(struct _exception  *e)
{
    e;               // Dummy reference to catch the warning
    return 1;        // Error has been handled
}
```



## <a name="parameter-validation"></a>Validation des paramètres

Pour des raisons de performances, la version de débogage du runtime en mode immédiat Direct3D effectue plus de validation de paramètres que la version commerciale, qui n’effectue parfois aucune validation. Cela permet aux applications d’effectuer un débogage robuste avec le composant d’exécution de débogage le plus lent avant d’utiliser la version commerciale la plus rapide pour le réglage des performances et la version finale.

Bien que plusieurs méthodes Direct3D en mode immédiat imposent des limites aux valeurs qu’elles peuvent accepter, ces limites ne sont souvent vérifiées et appliquées que par la version Debug du mode exécution Direct3D. Les applications doivent être conformes à ces limites, ou des résultats imprévisibles et indésirables peuvent se produire lors de l’exécution sur la version commerciale de Direct3D. Par exemple, la méthode [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) accepte un paramètre (PrimitiveCount) qui indique le nombre de primitives que la méthode restituera. La méthode peut uniquement accepter des valeurs comprises entre 0 et D3DMAXNUMPRIMITIVES. Dans la version Debug de Direct3D, si vous transmettez plus de primitives D3DMAXNUMPRIMITIVES, la méthode échoue correctement, en imprimant un message d’erreur dans le journal des erreurs et en renvoyant une valeur d’erreur à votre application. À l’inverse, si votre application génère la même erreur lorsqu’elle s’exécute avec la version commerciale du runtime, le comportement n’est pas défini. Pour des raisons de performances, la méthode ne valide pas les paramètres, ce qui se traduit par un comportement imprévisible et complet lorsqu’ils ne sont pas valides. Dans certains cas, l’appel peut fonctionner et, dans d’autres cas, il peut provoquer une erreur de mémoire dans Direct3D. Si un appel non valide fonctionne de manière cohérente avec une configuration matérielle spécifique et une version de DirectX, il n’existe aucune garantie qu’il continuera à fonctionner sur un autre matériel ou avec des versions ultérieures de DirectX.

Si votre application rencontre des échecs inexpliqués lors de l’exécution avec le fichier d’exécution Direct3D de vente au détail, effectuez des tests sur la version de débogage et recherchez attentivement les cas où votre application transmet des paramètres non valides. Utilisez l’applet du panneau de configuration DirectX, basculez vers le runtime de débogage si nécessaire, puis activez l’option « arrêter sur D3DError ». Cette option force le runtime à utiliser la méthode Windows DebugBreak afin de forcer l’arrêt de l’application lorsqu’un bogue de l’application est détecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 
