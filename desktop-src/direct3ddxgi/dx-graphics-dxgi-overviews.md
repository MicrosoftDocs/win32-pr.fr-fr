---
description: Microsoft DirectX Graphics infrastructure (DXGI) gère les tâches de bas niveau qui peuvent être indépendantes du runtime Graphics Direct3D. DXGI fournit une infrastructure commune pour plusieurs versions de Direct3D.
ms.assetid: bcbeb4bc-3bd1-40ed-b176-a8091cc6ee9f
title: Guide de programmation pour DXGI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7834b2fc68019dccfb8ab8b2e62698465ff1ea2d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200673"
---
# <a name="programming-guide-for-dxgi"></a>Guide de programmation pour DXGI

Microsoft DirectX Graphics infrastructure (DXGI) gère les tâches de bas niveau qui peuvent être indépendantes du runtime Graphics Direct3D. DXGI fournit une infrastructure commune pour plusieurs versions de Direct3D.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                                                              | Description                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Présentation de DXGI](d3d10-graphics-programming-guide-dxgi.md)<br/>                                                              | Cette rubrique contient les sections suivantes.<br/>                                                                                                                   |
| [Améliorations de DXGI 1,2](dxgi-1-2-improvements.md)<br/>                                                                      | Les fonctionnalités suivantes ont été ajoutées dans DXGI 1,2.<br/>                                                                                                       |
| [Améliorations de DXGI 1,3](dxgi-1-3-improvements.md)<br/>                                                                      | Les fonctionnalités suivantes ont été ajoutées dans DXGI 1,3, qui est inclus à partir de Windows 8.1.<br/>                                                            |
| [Améliorations de DXGI 1,4](dxgi-1-4-improvements.md)<br/>                                                                      | Les fonctionnalités suivantes ont été ajoutées ou modifiées dans DXGI 1,4, principalement pour prendre en charge Direct3D 12. <br/>                                                           |
| [Améliorations de DXGI 1,5](dxgi-1-5-improvements.md)<br/>                                                                      | Les fonctionnalités suivantes ont été ajoutées à DXGI 1,5, afin de prendre en charge une spécification et une duplication plus flexibles des formats de sortie.<br/>                                |
| [Améliorations de DXGI 1,6](dxgi-1-6-improvements.md)<br/>                                                                      | Les fonctionnalités suivantes ont été ajoutées à DXGI 1,6 afin de détecter les affichages HDR.<br/>                                                                       |
| [Utilisation de DirectX avec des écrans à haute gamme dynamique et une couleur avancée](../direct3darticles/high-dynamic-range.md)     | Cette rubrique fournit une vue d’ensemble technique du rendu de contenu Direct3D 11 et Direct3D 12 à plage dynamique élevée dans un affichage HDR10 à l’aide de la prise en charge avancée des couleurs Windows 10.<br/> |
| [Affichage du taux d’actualisation des variables](variable-refresh-rate-displays.md)<br/>                                                    | Le taux d’actualisation des variables indique que le *déchirement* doit être activé, ce qui est également appelé prise en charge de la « Vsync ».<br/>                                                    |
| [Utilisation de la correction gamma](using-gamma-correction.md)<br/>                                                                    | La correction gamma, ou gamma pour Short, est le nom d’une opération non linéaire que les systèmes utilisent pour coder et décoder les valeurs de pixel dans les images.<br/>                        |
| [Prise en charge du format pour Direct3D Feature 10Level9 9,1 Hardware](format-support-for-direct3d-feature-level-9-1-hardware.md)<br/> | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,1 Hardware.<br/>        |
| [Prise en charge du format pour Direct3D Feature 10Level9 9,3 Hardware](format-support-for-direct3d-feature-level-9-3-hardware.md)<br/> | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans la fonctionnalité Direct3D 10Level9 9,3 Hardware.<br/>        |
| [Prise en charge du format du matériel 10,0 de niveau de fonctionnalité Direct3D](format-support-for-direct3d-feature-level-10-0-hardware.md)<br/>  | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel Direct3D 10,0.<br/>                        |
| [Prise en charge du format du matériel 10,1 de niveau de fonctionnalité Direct3D](format-support-for-direct3d-feature-level-10-1-hardware.md)<br/>  | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel Direct3D 10,1.<br/>                        |
| [Prise en charge du format du matériel 11,0 de niveau de fonctionnalité Direct3D](format-support-for-direct3d-11-0-feature-level-hardware.md)<br/>  | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel 11,0 de niveau de fonctionnalité Direct3D.<br/>          |
| [Prise en charge du format du matériel 11,1 de niveau de fonctionnalité Direct3D](format-support-for-direct3d-11-1-feature-level-hardware.md)<br/>  | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel 11,1 de niveau de fonctionnalité Direct3D.<br/>          |
| [Prise en charge du format du matériel 12,0 de niveau de fonctionnalité Direct3D](hardware-support-for-direct3d-12-0-formats.md)<br/>               | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel 12,0 de niveau de fonctionnalité Direct3D.<br/>          |
| [Prise en charge du format du matériel 12,1 de niveau de fonctionnalité Direct3D](hardware-support-for-direct3d-12-1-formats.md)<br/>               | Cette section spécifie les formats (valeurs de [**\_ format dxgi**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) ) qui sont pris en charge dans le matériel Direct3D 12,1.<br/>                        |
| [Vérification de la prise en charge des fonctionnalités matérielles](checking-hardware-feature-support.md)<br/>                                              | Cette section explique comment vérifier la prise en charge du format pour le matériel de niveau de fonctionnalité Direct3D à l’aide d’appels d’API.<br/>                                                       |
| [Pour des performances optimales, utilisez DXGI Flip Model](for-best-performance--use-dxgi-flip-model.md)<br/>                              | Cette rubrique fournit des conseils pour les développeurs sur la façon d’optimiser les performances et l’efficacité dans la pile de présentation sur les versions modernes de Windows.<br/>                 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DXGI](dx-graphics-dxgi.md)
</dt> <dt>

[Référence DXGI](d3d10-graphics-reference-dxgi.md)
</dt> <dt>

[DirectX Graphics infrastructure (DXGI) : meilleures pratiques](../direct3darticles/dxgi-best-practices.md)
</dt> </dl>

 

 
