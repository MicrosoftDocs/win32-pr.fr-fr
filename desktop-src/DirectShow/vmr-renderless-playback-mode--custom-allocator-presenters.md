---
description: Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)
ms.assetid: 0381f862-2f16-4b4d-be48-40f7fe151585
title: Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad9cd4dcb5e5b2f1965d49c7f31b4ef8c9ebd78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127238955"
---
# <a name="vmr-renderless-playback-mode-custom-allocator-presenters"></a>Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)

En mode de lecture sans rendu, VMR n’effectue pas le rendu. Au lieu de cela, il utilise un allocateur-présentateur personnalisé fourni par l’application. Ce mode est utile pour les jeux et les autres types d’applications qui ont des effets vidéo sophistiqués. Le mode de lecture non rendu permet aux applications de créer et contrôler sa propre surface DirectDraw (VMR-7) ou la surface Direct3D (VMR-9) et d’accéder aux bits vidéo au moment de la présentation.

En mode sans rendu, VMR-9 ne charge pas automatiquement son composant mixer.

En mode de lecture sans rendu, l’application effectue les tâches suivantes :

-   Gère la fenêtre de lecture.
-   Alloue l’objet DirectDraw ou Direct3D et la mémoire tampon de frame finale.
-   Notifie le reste du système de lecture de l’objet utilisé.
-   Affiche la mémoire tampon de frame à l’heure correcte.
-   Gère toutes les modifications du mode de résolution, surveille les modifications et les pertes de surface. Il doit informer le reste du système de lecture de ces événements.

VMR effectue les opérations suivantes :

-   Gère tout le minutage lié à la présentation de l’image vidéo.
-   Fournit des informations de contrôle qualité à l’application et au reste du système de lecture.
-   Présente une interface cohérente aux composants en amont du système de lecture, qui ne savent pas que l’application fournit l’allocation de mémoire tampon de trame et effectue le rendu.
-   Fournit toute combinaison de flux vidéo qui peut être nécessaire avant le rendu.

Étant donné que l’opération de désentrelacement est effectuée par le mélangeur, l’allocateur-presenter a toujours reçu des frames désentrelacés. Pour plus d’informations, consultez [définition des préférences de désentrelacement](setting-deinterlace-preferences.md).

Pour plus d’informations sur la fourniture d’un Allocator-Presenter personnalisé, consultez les rubriques suivantes :

-   [Fourniture d’un Allocator-Presenter personnalisé pour VMR-7](supplying-a-custom-allocator-presenter-for-vmr-7.md)
-   [Fourniture d’un Allocator-Presenter personnalisé pour VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
-   [Synchronisation de VMR avec la fréquence d’actualisation du moniteur](synchronizing-the-vmr-to-the-monitors-refresh-rate.md)

 

 



