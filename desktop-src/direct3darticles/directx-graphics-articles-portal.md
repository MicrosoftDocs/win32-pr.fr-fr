---
title: Articles sur le graphisme DirectX
description: Articles sur le graphisme DirectX
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b5562b4b7dafc899d1c6a827cfd2e240a20013be7a31f225cdd41893d967748
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120095499"
---
# <a name="directx-graphics-articles"></a>Articles sur le graphisme DirectX

## <a name="purpose"></a>Objectif

cette section contient des articles techniques qui décrivent la déformation Windows et la prise en charge récemment ajoutée du Mode Flip et des statistiques actuelles associées dans Direct3D 9ex et Gestionnaire de fenêtrage. cette section contient également des articles techniques sur Windows api graphics, le portage des api direct3d 9 vers les api Microsoft DirectX graphics (DXGI) et la procédure de déploiement de direct3d 11.

Pour plus d’informations sur Direct3D, consultez [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Développeurs concernés

Ces articles techniques sont destinés aux développeurs d’applications graphiques DirectX.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [mise à jour de plateforme pour Windows 7](platform-update-for-windows-7.md) | décrit les composants de la pile de Windows 8 graphics qui deviennent disponibles et dans quelle mesure, par le biais de la [mise à jour de la plateforme pour Windows 7](https://support.microsoft.com/kb/2670838). |
| [Améliorations de Direct3D 9Ex](direct3d-9ex-improvements.md) | décrit la prise en charge nouvellement ajoutée de Windows 7 pour le Mode de basculement présent et les statistiques actuelles associées dans Direct3D 9ex et Gestionnaire de fenêtrage. Les applications cibles incluent des applications de présentation vidéo ou à fréquence d’images. Les applications qui utilisent le mode de basculement Direct3D 9Ex présentent réduisent la charge des ressources système lorsque DWM est activé. La présentation des améliorations des statistiques associées au mode de basculement présente permet aux applications Direct3D 9Ex de mieux contrôler le taux de présentation en fournissant des mécanismes de commentaires et de correction en temps réel. Des explications détaillées et des pointeurs vers des exemples de ressources sont inclus. |
| [Partage de surface entre les API graphiques Windows](surface-sharing-between-windows-graphics-apis.md) | fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre Windows api graphics, notamment direct3d 11, Direct2D, direct3d 10 et direct3d 9ex. si vous avez déjà une connaissance de ces api, ce document peut vous aider à utiliser plusieurs api pour effectuer un rendu sur la même surface dans une application conçue pour les systèmes d’exploitation Windows 7 ou Windows Vista. Cette rubrique présente également les meilleures pratiques et les pointeurs vers des ressources supplémentaires. |
| [Guide de distorsion](directx-warp.md) | fournit un guide de Windows plateforme de rastérisation avancée (WARP), un rastériseur logiciel à grande vitesse. |
| [API graphiques dans Windows](graphics-apis-in-windows-vista.md) | décrit Windows fonctionnalités graphiques et les api. |
| [Déploiement de Direct3D 11 pour les développeurs de jeux](direct3d11-deployment.md) | Décrit comment déployer les composants Direct3D 11 sur un système. |
| [DirectX Graphics infrastructure (DXGI) : meilleures pratiques](dxgi-best-practices.md) | Décrit les problèmes liés au portage des API Direct3D 9 vers les API DXGI et les fonctionnalités des différentes versions de DXGI. |
| [Utilisation de DirectX avec des écrans à haute gamme dynamique et une couleur avancée](high-dynamic-range.md) | cette rubrique fournit une vue d’ensemble technique du rendu d’un contenu direct3d 11 et direct3d 12 à plage dynamique élevée dans un affichage HDR10 Windows 10 à l’aide de la prise en charge des couleurs avancées. |
