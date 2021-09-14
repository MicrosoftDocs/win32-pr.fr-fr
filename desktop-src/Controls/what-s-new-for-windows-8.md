---
title: nouveautés (contrôles Windows)
description: cette rubrique décrit les différences de prise en charge des thèmes et des styles visuels entre Windows 8 et les versions précédentes de Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115206"
---
# <a name="whats-new-windows-controls"></a>nouveautés (contrôles Windows)

cette rubrique décrit les différences de prise en charge des thèmes et des styles visuels entre Windows 8 et les versions précédentes de Windows.

## <a name="through-windows-7"></a>jusqu’à Windows 7

par le biais de Windows 7, les styles visuels sont activés par défaut, mais l’utilisateur peut les désactiver en sélectionnant Windows thème classique ou en désactivant le service thèmes. Lorsque les styles visuels sont désactivés, toute l’interface utilisateur obtient l’apparence classique, et la plupart des API de styles visuels ne sont pas disponibles. le mode de désactivation des styles visuels a été conservé via Windows 7 pour prendre en charge les différents thèmes à contraste élevé, ainsi que Windows thème classique. Si vous souhaitez prendre en charge à la fois les styles visuels et les thèmes à contraste élevé dans la même application, vous devez généralement gérer deux chemins de code distincts pour le rendu des contrôles.

## <a name="windows-8-and-later"></a>Windows 8 et versions ultérieures

dans Windows 8, les styles visuels ne peuvent pas être désactivés via la page de **personnalisation** du **Paramètres de PC** ou en désactivant le service thèmes. Windows Le mode classique n’existe plus et le mode contraste élevé a été modifié pour fonctionner avec les styles visuels. en raison de ces modifications, les applications qui ciblent uniquement Windows 8 n’ont plus besoin de deux chemins de code distincts pour prendre en charge les styles visuels et les thèmes à contraste élevé.

les styles visuels dans Windows 8 incluent la prise en charge de la compatibilité descendante pour Windows mode de thèmes classiques. tout code de rendu d’interface utilisateur qui fonctionne sur les versions précédentes continuera à fonctionner sur Windows 8 sans aucune modification.

dans Windows 8, si vous souhaitez que votre application prenne en charge les thèmes à contraste élevé basés sur des styles visuels, vous devez inclure le GUID Windows 8 dans la section compatibilité de votre manifeste d’application. dans le cas contraire, le système suppose que l’application est conçue pour une version antérieure et restitue la zone cliente en simulant Windows des thèmes à contraste élevé classiques. Pour plus d’informations, consultez [prise en charge des thèmes de contraste élevé](supporting-high-contrast-themes.md).

comme dans les versions précédentes, Windows 8 prend en charge la version 5 et la version 6 des contrôles communs, la version 5 étant la valeur par défaut. Étant donné que seule la version 6 prend en charge les styles visuels, vous devez spécifier la version 6 dans votre manifeste d’application si vous souhaitez que les styles visuels soient appliqués aux contrôles communs dans la zone cliente de votre application. Pour plus d’informations, consultez [activation des styles visuels](cookbook-overview.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Activation des styles visuels](cookbook-overview.md)
</dt> <dt>

[Prise en charge des thèmes de contraste élevé](supporting-high-contrast-themes.md)
</dt> <dt>

[Styles visuels](themes-overview.md)
</dt> <dt>

[Vue d’ensemble des styles visuels](visual-styles-overview.md)
</dt> </dl>

 

 




