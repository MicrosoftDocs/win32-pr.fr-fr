---
description: Direct3D est une API de bas niveau pour le dessin de primitives avec le pipeline de rendu ou l’exécution d’opérations parallèles avec le nuanceur de calcul.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Bien démarrer avec Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2b5a579b589a747c4e7640b3c868d488a7e58f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106525084"
---
# <a name="getting-started-with-direct3d"></a>Bien démarrer avec Direct3D

Direct3D est une API de bas niveau pour le dessin de primitives avec le pipeline de rendu ou pour l’exécution d’opérations parallèles avec le nuanceur de calcul.

## <a name="what-is-direct3d"></a>Qu’est-ce que Direct3D ?

Direct3D est une API de bas niveau que vous pouvez utiliser pour dessiner des triangles, des lignes ou des points par cadre, ou pour démarrer des opérations hautement parallèles sur le GPU.

Direct3D

-   Masque différentes implémentations de GPU derrière une abstraction cohérente. Toutefois, vous devez encore savoir comment dessiner des graphiques 3D.
-   Est conçu pour conduire un processeur spécifique à des graphiques. Les cartes GPU plus récentes comportent des centaines ou des milliers de processeurs parallèles.
-   Met l’accent sur le traitement parallèle. Vous configurez une série d’États de rendu ou de calcul, puis démarrez une opération. Vous n’attendez pas les commentaires immédiats de l’opération. Vous ne mélangez pas les opérations du processeur et du GPU.

## <a name="which-direct3d-apis-can-you-use"></a>Quelles API Direct3D pouvez-vous utiliser ?

Les API Direct3D que vous choisissez dépendent du style de l’application que vous souhaitez écrire.

-   Si vous souhaitez écrire une application UWP, utilisez un sous-ensemble de l’API Direct3D 11, DXGI et HLSL. Pour obtenir la liste de ces API, consultez [API Win32 et com pour les applications UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). Pour savoir comment écrire une application Direct3D 11 du Windows Store, consultez [créer des graphiques 3D avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Si vous écrivez une application de bureau, vous pouvez utiliser l’ensemble complet des API Direct3D 11, DXGI et HLSL.
-   À compter de Windows 8, nous ne prenons plus en charge activement l’infrastructure XNA pour les applications de bureau. Toutefois, les applications du Windows Store, les applications UWP et les applications de bureau peuvent utiliser l’ensemble complet des API [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) et [DirectXMath](/windows/desktop/dxmath/directxmath-portal) . Les applications de bureau peuvent utiliser l’ensemble complet des API [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) , tandis que les applications du Windows Store et les applications UWP peuvent utiliser la plupart des API XInput. Pour plus d’informations, consultez [versions de XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Quelle version de Direct3D ?

La version de l’API Direct3D que vous choisissez dépend du système d’exploitation et du matériel que vous souhaitez cibler.

-   Si vous souhaitez cibler Windows 8 et versions ultérieures, utilisez les API Direct3D 11.
-   Utilisez les API Direct3D 9 avec Windows XP et versions ultérieures. Tout le matériel prend en charge les API Direct3D 9, même tout nouveau matériel Direct3D de niveau 11.
-   Utilisez les API Direct3D 10 avec Windows Vista et versions ultérieures. Seuls les matériels Direct3D 10 et versions ultérieures prennent en charge les API Direct3D 10.
-   Utilisez les API Direct3D 10,1 et Direct3D 11 avec Windows 7 et versions ultérieures. Vous pouvez également utiliser les API Direct3D 10,1 et Direct3D 11 avec Windows Vista avec Service Pack 2 (SP2) en téléchargeant [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Pipeline de rendu Direct3D

Dans le [pipeline de rendu](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)Direct3D, les données circulent à partir de plusieurs sources, telles que les « les ».

-   Certaines parties du fluide sont programmables.
-   Certaines parties ont des boutons et des cadrans.
-   Les sources de données sont soit des flux série de paquets (sommets), soit des tableaux indexables (ressources de nuanceur).
-   Les vertex et les ressources de nuanceur sont transmis dans des primitives, que vous pouvez amplifier.
-   Les primitives et les ressources de nuanceur sont transmises en opérations de pixels.

## <a name="direct3d-compute-shader"></a>Nuanceur de calcul Direct3D

Avec le [nuanceur de calcul](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)Direct3D, tous les processeurs du GPU s’exécutent en parallèle. Par conséquent, le nuanceur de calcul se comporte plus comme un étang qu’une rivière.
