---
title: Articles sur le graphisme DirectX
description: .
ms.assetid: 22178507-9a3b-49b1-a3db-851001a32e8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16ac2a3a6b9beff7dfc8bfe4f6c0de92885f39ca
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316019"
---
# <a name="directx-graphics-articles"></a>Articles sur le graphisme DirectX

## <a name="purpose"></a>Objectif

Cette section contient des articles techniques qui décrivent la déformation et la prise en charge nouvellement ajoutée de Windows 7 pour le mode de basculement présent et les statistiques actuelles associées dans Direct3D 9Ex et Gestionnaire de fenêtrage. Cette section contient également des articles techniques sur les API graphiques Windows, le portage des API Direct3D 9 vers les API Microsoft DirectX Graphics infrastructure (DXGI) et la procédure de déploiement de Direct3D 11.

Pour plus d’informations sur Direct3D, consultez [Direct3D](/windows/desktop/direct3d).

## <a name="developer-audience"></a>Développeurs concernés

Ces articles techniques sont destinés aux développeurs d’applications graphiques DirectX.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Mise à jour de plateforme pour Windows 7](platform-update-for-windows-7.md) | Décrit les composants de la pile graphique Windows 8 qui deviennent disponibles et dans quelle mesure, via la [mise à jour de plateforme pour Windows 7](https://support.microsoft.com/kb/2670838). |
| [Améliorations de Direct3D 9Ex](direct3d-9ex-improvements.md) | Décrit la prise en charge récemment ajoutée de Windows 7 pour le mode de basculement et les statistiques actuelles associées dans Direct3D 9Ex et Gestionnaire de fenêtrage. Les applications cibles incluent des applications de présentation vidéo ou à fréquence d’images. Les applications qui utilisent le mode de basculement Direct3D 9Ex présentent réduisent la charge des ressources système lorsque DWM est activé. La présentation des améliorations des statistiques associées au mode de basculement présente permet aux applications Direct3D 9Ex de mieux contrôler le taux de présentation en fournissant des mécanismes de commentaires et de correction en temps réel. Des explications détaillées et des pointeurs vers des exemples de ressources sont inclus. |
| [Partage de surface entre les API graphiques Windows](surface-sharing-between-windows-graphics-apis.md) | Fournit une vue d’ensemble technique de l’interopérabilité à l’aide du partage de surface entre les API graphiques Windows, notamment Direct3D 11, Direct2D, Direct3D 10 et Direct3D 9Ex. Si vous avez déjà une connaissance de ces API, ce document peut vous aider à utiliser plusieurs API pour effectuer un rendu sur la même surface dans une application conçue pour les systèmes d’exploitation Windows 7 ou Windows Vista. Cette rubrique présente également les meilleures pratiques et les pointeurs vers des ressources supplémentaires. |
| [Guide de distorsion](directx-warp.md) | Fournit un guide de la plateforme de rastérisation avancée Windows (WARP), un rastériseur logiciel à grande vitesse. |
| [API graphiques dans Windows](graphics-apis-in-windows-vista.md) | Présente les API et les fonctionnalités graphiques de Windows. |
| [Déploiement de Direct3D 11 pour les développeurs de jeux](direct3d11-deployment.md) | Décrit comment déployer les composants Direct3D 11 sur un système. |
| [DirectX Graphics infrastructure (DXGI) : meilleures pratiques](dxgi-best-practices.md) | Décrit les problèmes liés au portage des API Direct3D 9 vers les API DXGI et les fonctionnalités des différentes versions de DXGI. |
| [Utilisation de DirectX avec des écrans à haute gamme dynamique et une couleur avancée](high-dynamic-range.md) | Cette rubrique fournit une vue d’ensemble technique du rendu de contenu Direct3D 11 et Direct3D 12 à plage dynamique élevée dans un affichage HDR10 à l’aide de la prise en charge avancée des couleurs Windows 10. |