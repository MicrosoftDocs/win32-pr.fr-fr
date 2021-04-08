---
title: Meilleures pratiques pour DirectComposition
description: Cette rubrique décrit les meilleures pratiques pour l’utilisation de Microsoft DirectComposition.
ms.assetid: D3A1ECD4-9358-44B9-8A84-7D901219D5CD
keywords:
- meilleures pratiques pour DirectComposition
- pratiques recommandées pour DirectComposition
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0d19b82b188105c7914e89282c08b12dd4bdc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729900"
---
# <a name="best-practices-for-directcomposition"></a>Meilleures pratiques pour DirectComposition

> [!NOTE]
> Pour les applications sur Windows 10, nous vous recommandons d’utiliser des API Windows. UI. composition au lieu de DirectComposition. Pour plus d’informations, consultez [moderniser votre application de bureau à l’aide de la couche visuelle](/windows/uwp/composition/visual-layer-in-desktop-apps).

Cette rubrique décrit les meilleures pratiques pour l’utilisation de Microsoft DirectComposition.

-   [Bonnes pratiques](#best-practices-for-directcomposition)
-   [Considérations relatives à la sécurité](#security-considerations)
-   [Rubriques connexes](#related-topics)

## <a name="best-practices"></a>Bonnes pratiques

Le tableau suivant présente les pratiques recommandées pour l’utilisation des éléments visuels Microsoft DirectComposition.



| Pratiquer                                                                                                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Après avoir créé un appareil DirectComposition, appelez la méthode [**IDCompositionDevice :: CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) en réponse à chaque message [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) pour vous assurer que l’appareil est toujours valide.<br/> | Si l’appareil Microsoft DirectX Graphics (DXGI) est perdu, l’appareil DirectComposition associé à l’appareil DXGI est également perdu. Lorsqu’il détecte un appareil perdu, DirectComposition envoie le message [**de \_ peinture WM**](/windows/desktop/gdi/wm-paint) à toutes les fenêtres. L’appel de [**CheckDeviceState**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-checkdevicestate) en réponse à chaque message **WM \_ Paint** vous permet de déterminer si l’objet appareil DirectComposition est toujours valide et, dans le cas contraire, de prendre des mesures pour récupérer du contenu. <br/> Pour plus d’informations, consultez [objet Device](basic-concepts.md).<br/> |
| Créez uniquement le nombre d’éléments visuels nécessaires pour une composition ou une animation, puis détruisez les visuels immédiatement après que DirectComposition a terminé de les utiliser.<br/>                                                                                            | DirectComposition utilise l’unité de traitement graphique (GPU), une ressource que votre application partage avec d’autres applications et le système d’exploitation. Cette pratique garantit que toutes les applications et le système d’exploitation reçoivent des ressources GPU appropriées.<br/> Pour plus d’informations, consultez [visuels](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                     |
| Ne pas masquer les visuels en affectant à l’opacité la valeur 0%; à la place, supprimez les éléments visuels de l’arborescence d’éléments visuels.<br/>                                                                                                                                                          | La définition de l’opacité à 0% nécessite davantage de ressources système que la suppression de l’arborescence d’éléments visuels.<br/> Pour plus d’informations, consultez [opacité](effects.md) et arborescence d’éléments [visuels](basic-concepts.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| Ne masquez pas un visuel en appliquant un rectangle de découpage vide (de taille zéro) à un visuel. Au lieu de cela, supprimez le visuel de l’arborescence d’éléments visuels. <br/>                                                                                                                 | La suppression d’un visuel de l’arborescence d’éléments visuels donne de meilleures performances que l’application d’un rectangle de découpage vide.<br/> Pour plus d’informations, consultez [découpage](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                |
| N’appliquez pas de rectangle de découpage à un visuel si le rectangle de découpage n’est pas nécessaire, tel qu’un rectangle de découpage qui comprend l’intégralité du contenu de la bitmap de l’élément visuel.<br/>                                                                                       | Les rectangles de découpage inutiles nuisent aux performances du système.<br/> Pour plus d’informations, consultez [découpage](clipping.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Si vous avez besoin d’une grande image bitmap de couleur unique, créez une surface bitmap plus petite, puis appliquez une transformation d’échelle au lieu de créer une surface pleine. <br/>                                                                                                | L’application d’une transformation d’échelle à une surface plus petite utilise moins de ressources système qu’une surface pleine taille.<br/> Pour plus d’informations, consultez [objets bitmap](bitmap-surfaces.md) et [transformations](transforms.md).<br/>                                                                                                                                                                                                                                                                                                                                                                                     |
| Évitez d’appliquer des transformations 3D à plusieurs niveaux d’une arborescence d’éléments visuels, par exemple à un parent et à ses descendants. <br/>                                                                                                                                        | L’application de transformations 3D à plusieurs niveaux d’une arborescence d’éléments visuels peut produire des résultats inattendus, car les transformations 3D ne sont pas multipliées dans l’arborescence. Par exemple, une rotation de 90 degrés autour de l’axe y sur un enfant, et une rotation de 90 degrés autour de l’axe y sur un parent, entraîne la rotation des deux éléments visuels vers l’extérieur.<br/> Pour plus d’informations, consultez [Effets](effects.md).<br/>                                                                                                                                                                                                     |



 

## <a name="security-considerations"></a>Considérations relatives à la sécurité

Les articles suivants fournissent des conseils pour l’écriture de code C++ sécurisé.

-   [Meilleures pratiques de sécurité pour C++](/cpp/security/security-best-practices-for-cpp?view=vs-2019)
-   [Modèles & pratiques conseils de sécurité pour les applications](/previous-versions/msp-n-p/ff650760(v=pandp.10))

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de DirectComposition](how-to-use-directcomposition.md)
</dt> </dl>

 

