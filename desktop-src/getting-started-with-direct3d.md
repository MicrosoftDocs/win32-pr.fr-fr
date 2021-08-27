---
description: Direct3D est une API de bas niveau pour le dessin de primitives avec le pipeline de rendu ou l’exécution d’opérations parallèles avec le nuanceur de calcul.
ms.assetid: 55063BF2-34A3-4E56-882C-86F0949DE557
title: Bien démarrer avec Direct3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea01f24659bfbb5eb0667a0ae1cbfa3529a206b7b7ce7e3d3a4388e71fabd571
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092549"
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

-   Si vous souhaitez écrire une application UWP, utilisez un sous-ensemble de l’API Direct3D 11, DXGI et HLSL. Pour obtenir la liste de ces API, consultez [API Win32 et com pour les applications UWP](/uwp/win32-and-com/win32-and-com-for-uwp-apps). pour savoir comment écrire une application Direct3D 11 Windows Store, consultez [créer des graphiques 3d avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)).
-   Si vous écrivez une application de bureau, vous pouvez utiliser l’ensemble complet des API Direct3D 11, DXGI et HLSL.
-   à compter de Windows 8, nous ne prenons plus en charge activement l’infrastructure XNA pour les applications de bureau. Windows toutefois, les applications du windows Store, les applications UWP et les applications de bureau peuvent utiliser l’ensemble complet des api [XAudio2](/windows/desktop/xaudio2/xaudio2-apis-portal) et [DirectXMath](/windows/desktop/dxmath/directxmath-portal) . les applications de bureau peuvent utiliser l’ensemble complet des api [XInput](/windows/desktop/xinput/xinput-game-controller-apis-portal) , tandis que les applications Windows store et les applications UWP peuvent utiliser la plupart des api XInput. Pour plus d’informations, consultez [versions de XInput](/windows/desktop/xinput/xinput-versions).

## <a name="which-direct3d-version"></a>Quelle version de Direct3D ?

La version de l’API Direct3D que vous choisissez dépend du système d’exploitation et du matériel que vous souhaitez cibler.

-   si vous souhaitez cibler Windows 8 et versions ultérieures, utilisez les api Direct3D 11.
-   utilisez les api Direct3D 9 avec Windows XP et versions ultérieures. Tout le matériel prend en charge les API Direct3D 9, même tout nouveau matériel Direct3D de niveau 11.
-   utilisez les api Direct3D 10 avec Windows Vista et versions ultérieures. Seuls les matériels Direct3D 10 et versions ultérieures prennent en charge les API Direct3D 10.
-   utilisez les api direct3d 10,1 et direct3d 11 avec Windows 7 et versions ultérieures. vous pouvez également utiliser les api direct3d 10,1 et direct3d 11 avec Windows Vista avec Service Pack 2 (SP2) en téléchargeant [KB 971644](https://support.microsoft.com/kb/971644).

## <a name="direct3d-rendering-pipeline"></a>Pipeline de rendu Direct3D

Dans le [pipeline de rendu](./direct3d11/overviews-direct3d-11-graphics-pipeline.md)Direct3D, les données circulent à partir de plusieurs sources, telles que les « les ».

-   Certaines parties du fluide sont programmables.
-   Certaines parties ont des boutons et des cadrans.
-   Les sources de données sont soit des flux série de paquets (sommets), soit des tableaux indexables (ressources de nuanceur).
-   Les vertex et les ressources de nuanceur sont transmis dans des primitives, que vous pouvez amplifier.
-   Les primitives et les ressources de nuanceur sont transmises en opérations de pixels.

## <a name="direct3d-compute-shader"></a>Nuanceur de calcul Direct3D

Avec le [nuanceur de calcul](./direct3d11/direct3d-11-advanced-stages-compute-shader.md)Direct3D, tous les processeurs du GPU s’exécutent en parallèle. Par conséquent, le nuanceur de calcul se comporte plus comme un étang qu’une rivière.
