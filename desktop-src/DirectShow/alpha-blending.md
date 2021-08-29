---
description: Fusion alpha
ms.assetid: 56618e74-32cc-48f8-83b6-4fc31ab6fc36
title: Fusion alpha (DirectShow)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ffe2a81affdfb4fec8cd8363330cd0505851eedb96bbf635fe754c50610df82
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119537469"
---
# <a name="alpha-blending-directshow"></a>Fusion alpha (DirectShow)

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

cet article décrit la fusion alpha dans les [Services d’édition de DirectShow](directshow-editing-services.md) .

Alpha mesure la transparence d’un pixel ou d’une image. Dans la vidéo RVB non compressée 32 bits, quatre composants définissent chaque pixel : un canal alpha (A) et trois composants de couleur (RVB). Un pixel dont la valeur alpha est égale à zéro est totalement transparent. Un pixel avec une valeur alpha de 255 est opaque. Entre ces valeurs, le pixel a différents degrés de transparence.

DirectShow définit deux types de média pour la vidéo RGB 32 bits :

-   **MEDIASUBTYPE \_ ARGB32**: la vidéo est 32 bits RGB avec un canal alpha valide.
-   **MEDIASUBTYPE \_ RGB32**: les pixels sont 32 bits, mais le canal alpha n’est pas nécessairement valide.

Pour effectuer une fusion alpha dans DES, définissez le type de média non compressé du groupe vidéo sur MEDIASUBTYPE \_ ARGB32. En C++, appelez la méthode [**IAMTimelineGroup :: SetMediaType**](iamtimelinegroup-setmediatype.md) . Dans le format XTL, l’affectation de la valeur 32 à l’attribut [**bitdepth**](bitdepth-attribute.md) de l’élément [**Group**](group-element.md) est également possible.

Ensuite, vous avez besoin de données vidéo qui contiennent un canal alpha. Il existe plusieurs options :

-   Vous pouvez utiliser un fichier AVI qui possède déjà une vidéo RGB 32 bits avec des données alpha. actuellement, alpha n’est pas pris en charge pour les fichiers sources MPEG ou WMF (Microsoft Windows Media Format).
-   DES prend en charge les fichiers bitmap 32 bits (.bmp) et Targa (. TGA) avec des données alpha.
-   Vous pouvez écrire un filtre source personnalisé qui crée des données RGB 32 bits avec alpha. Le type de média de sortie doit être **MEDIASUBTYPE \_ ARGB32**. Utilisez le filtre en tant que sous-objet dans un objet source de chronologie.

Si votre source vidéo n’a pas d’alpha, vous pouvez utiliser un effet qui crée des données alpha. L' [effet d’accesseur Set alpha](alpha-setter-effect.md) définit le canal alpha pour l’intégralité de l’image sur une valeur constante. Pour faire varier l’alpha dans le temps, utilisez l’interface [**IPropertySetter**](ipropertysetter.md) avec l’effet d’accesseur Set alpha. La source d’origine ne doit pas nécessairement être de 32 bits, à condition que le type de support non compressé du groupe soit **MEDIASUBTYPE \_ ARGB32**.

Enfin, passez la vidéo à un effet ou à une transition qui effectue une fusion alpha. La [transition du compositeur](compositor-transition.md) effectue une fusion alpha et la [transition de clé](key-transition.md) peut être associée à la valeur alpha.

L’exemple de projet XTL suivant effectue une fusion alpha :


```C++
<timeline>
<group type="video" bitdepth="32" width="320" height="240">
<track>
  <clip start="0" stop="6" src="c:\Example.avi" />
</track>
<track>
  <clip start="0" stop="6" src="c:\Example2.avi">
    <!-- Alpha Setter effect. -->
    <effect clsid="{506D89AE-909A-44f7-9444-ABD575896E35}" start="0" stop="6">
      <param name="alpha" value="255">
        <linear time="6" value="0" />
      </param>
    </effect>
  </clip>
  <!-- Key transition, with alpha keying. -->
  <transition clsid="{C5B19592-145E-11d3-9F04-006008039E37}" start="0" stop="6">
    <param name="KeyType" value="3" />  
  </transition>
</track>
</group>
</timeline>
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[utilisation des Services de modification DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



