---
title: DirectComposition
description: Cette rubrique décrit l’objectif de Microsoft DirectComposition, identifie ses exigences d’exécution et décrit l’arrière-plan de programmation dont vous avez besoin pour utiliser Microsoft DirectComposition efficacement.
ms.assetid: 40e2d02b-77e8-425f-ac5e-3dcddef08173
keywords:
- DirectComposition
- API DirectComposition
- Microsoft DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb34a4bb3bb7c0ffe370777888e20704fd0165d0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524445"
---
# <a name="directcomposition"></a>DirectComposition

> [!NOTE]
> pour les applications sur Windows 10, nous vous recommandons d’utiliser des api Windows. UI. Composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

## <a name="purpose"></a>Objectif

Microsoft DirectComposition est un composant Windows qui permet la composition de bitmaps hautes performances avec des transformations, des effets et des animations. Les développeurs d’applications peuvent utiliser l’API DirectComposition pour créer des interfaces utilisateur visuellement attrayantes avec des transitions riches et fluides d’un élément visuel à l’autre.

DirectComposition permet d’effectuer des transitions riches et fluides en obtenant une fréquence élevée, en utilisant le matériel graphique et en opérant indépendamment du thread d’interface utilisateur. DirectComposition peut accepter le contenu bitmap dessiné par différentes bibliothèques de rendu, y compris les bitmaps Microsoft DirectX, et les bitmaps restitués dans une fenêtre (images bitmap HWND). En outre, DirectComposition prend en charge diverses transformations, telles que des transformations affines 2D et des transformations de perspective 3D, ainsi que des effets de base tels que le découpage et l’opacité.

DirectComposition est conçu pour simplifier le processus de composition des éléments [*visuels*](directcomposition-glossary.md) et la création de transitions animées. Si votre application contient déjà du code de rendu ou utilise déjà l’API DirectX recommandée, il vous suffit d’effectuer une quantité minimale de travail pour utiliser DirectComposition efficacement.

## <a name="developer-audience"></a>Développeurs concernés

l’API DirectComposition est conçue pour les développeurs de graphiques expérimentés et très efficaces qui connaissent C/C++, ont une bonne compréhension du modèle COM (component Object Model) et connaissent Windows concepts de programmation.

## <a name="run-time-requirements"></a>Conditions d’exécution

DirectComposition a été introduite dans Windows 8. Il est inclus dans les plateformes 32 bits, 64 bits et ARM.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                       | Description                                                                                                                                                    |
|-----------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pourquoi utiliser DirectComposition ?](why-use-directcomposition-.md)<br/>     | Cette rubrique décrit les fonctionnalités et les avantages de DirectComposition. <br/>                                                                           |
| [Utilisation de DirectComposition](how-to-use-directcomposition.md)<br/> | Cette section décrit les meilleures pratiques pour l’utilisation de l’API DirectComposition et montre comment utiliser l’API pour accomplir plusieurs tâches courantes. <br/> |
| [Concepts DirectComposition](directcomposition-concepts.md)<br/>     | Cette section fournit une vue d’ensemble conceptuelle de DirectComposition.<br/>                                                                                   |
| [Référence DirectComposition](reference.md)<br/>                     | Cette section fournit des informations de référence détaillées sur les éléments qui composent l’API DirectComposition.<br/>                                       |
| [Exemples DirectComposition](directcomposition-code-samples.md)<br/>  | Les exemples d’applications suivants montrent comment utiliser l’API DirectComposition et illustrer ses fonctionnalités. <br/>                                      |
| [Glossaire DirectComposition](directcomposition-glossary.md)<br/>     | Cette rubrique définit les conditions de DirectComposition. <br/>                                                                                                        |



 

 

 





