---
description: Déclarez une classe C++ qui hérite de la classe de base que votre a choisie dans le cadre de l’écriture d’un filtre de transformation.
ms.assetid: 74fbfc16-541f-4f80-a72f-26b67dc09a93
title: Étape 2. Déclarer la classe de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3e814802a67185f320345dea2f397188999ecafb9596b9b368a4b6eff8e240
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118652195"
---
# <a name="step-2-declare-the-filter-class"></a>Étape 2. Déclarer la classe de filtre

Il s’agit de l’étape 2 du didacticiel [écriture de filtres de transformation](writing-transform-filters.md).

Commencez par déclarer une classe C++ qui hérite de la classe de base :


```C++
class CRleFilter : public CTransformFilter
{
    /* Declarations will go here. */
};
```



Chacune des classes de filtre a des classes pin associées. En fonction des besoins spécifiques de votre filtre, vous devrez peut-être remplacer les classes pin. Dans le cas de **CTransformFilter**, les pin délèguent la plus grande partie de leur travail au filtre, ce qui signifie que vous n’avez probablement pas besoin de remplacer les codes confidentiels.

Vous devez générer un CLSID unique pour le filtre. Vous pouvez utiliser l’utilitaire Guidgen ou uuidgen. ne jamais copier un GUID existant. Il existe plusieurs façons de déclarer un CLSID. L’exemple suivant utilise la macro **définir le \_ GUID** :


```C++
[RleFilt.h]
// {1915C5C7-02AA-415f-890F-76D94C85AAF1}
DEFINE_GUID(CLSID_RLEFilter, 
0x1915c5c7, 0x2aa, 0x415f, 0x89, 0xf, 0x76, 0xd9, 0x4c, 0x85, 0xaa, 0xf1);

[RleFilt.cpp]
#include <initguid.h>
#include "RleFilt.h"
```



Ensuite, écrivez une méthode de constructeur pour le filtre :


```C++
CRleFilter::CRleFilter()
  : CTransformFilter(NAME("My RLE Encoder"), 0, CLSID_RLEFilter)
{ 
   /* Initialize any private variables here. */
}
```



Notez que l’un des paramètres du constructeur [**CTransformFilter**](ctransformfilter-ctransformfilter.md) est le CLSID défini précédemment.

Suivant : [étape 3. Prendre en charge la négociation de type de média](step-3--support-media-type-negotiation.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



