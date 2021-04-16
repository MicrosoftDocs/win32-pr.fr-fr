---
description: Épingler le jeu de propriétés
ms.assetid: 0c01bd51-353d-4f48-b33c-796f740915e2
title: Épingler le jeu de propriétés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc2d3ed55d7fed70d37a92427d1288ed58aef65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392504"
---
# <a name="pin-property-set"></a>Épingler le jeu de propriétés

La propriété pin définie renvoie la catégorie pin d’un code confidentiel sur un filtre. La catégorie est définie par le filtre lorsqu’elle crée le code confidentiel. la catégorie indique le type de données que le code confidentiel est remis ou reçoit par ce code PIN.



|                   |                      |
|-------------------|----------------------|
| GUID de jeu de propriétés | **\_Code PIN AMPROPSETID** |



 



| ID de propriété                   | Description                      |
|-------------------------------|----------------------------------|
| **\_catégorie de code confidentiel AMPROPERTY \_** | Spécifie la catégorie d’un code confidentiel. |



 

DirectShow définit les catégories de code confidentiel suivantes dans le fichier d’en-tête UUID. h.



| GUID de la catégorie                     | Description                                                                                                                                                                                                                                                                                                             |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **PIN \_ catégorie \_ ANALOGVIDEOIN**  | Broche d’entrée du filtre de capture qui prend le analogique et le numérise.                                                                                                                                                                                                                                                     |
| **ÉPINGLer la \_ capture de catégorie \_**        | Code PIN de capture.                                                                                                                                                                                                                                                                                                            |
| **ÉPINGLer la \_ catégorie \_ CC**             | Code PIN fournissant les données de sous-titrage de la ligne 21.                                                                                                                                                                                                                                                                      |
| **ÉPINGLer la \_ catégorie \_ EDS**            | Code confidentiel fournissant des Data Services étendues (lignes 21, même champs).                                                                                                                                                                                                                                                            |
| **PIN \_ catégorie \_ NABTS**          | Code PIN fournissant des données standard Videotext de l’Amérique du Nord.                                                                                                                                                                                                                                                                   |
| **Aperçu de la \_ catégorie pin \_**        | Code pin d’aperçu.                                                                                                                                                                                                                                                                                                            |
| **catégorie de PIN \_ \_ toujours**          | Code confidentiel qui fournit une image continue. Le code PIN de capture du filtre doit être connecté avant que le code confidentiel d’image continue soit connecté.                                                                                                                                                                                                    |
| **ÉPINGLer la \_ catégorie \_ télétexte**       | Code confidentiel fournissant du télétexte (variante de sous-titrage).                                                                                                                                                                                                                                                                   |
| **code \_ temporel de la catégorie pin \_**       | Code PIN fournissant les données de code temporel.                                                                                                                                                                                                                                                                                            |
| **BROCHE \_ catégorie \_ VBI**            | Code PIN fournissant les données de l’intervalle de l’occultation vertical.                                                                                                                                                                                                                                                                          |
| **PIN \_ catégorie \_ VIDEOPORT**      | Broche de sortie vidéo à connecter à la broche d’entrée zéro dans le [mélangeur de superposition](overlay-mixer-filter.md).                                                                                                                                                                                                                    |
| **BROCHE \_ catégorie \_ VIDEOPORT \_ VBI** | Code confidentiel à connecter à l' [allocateur de surface VBI](vbi-surface-allocator.md), filtre d’allocateur de surface VBI requis pour allouer la mémoire vidéo correcte pour des éléments tels que les superpositions de sous-titrage dans les scénarios où un port vidéo est utilisé. Les scénarios PCI, IEEE 1394 et USB n’utilisent pas ce filtre. |
| **\_ \_ capture CC de la vidéo PINNAME \_**   | Découpage matériel fermé-code confidentiel                                                                                                                                                                                                                                                                                  |



 

Cette propriété est en lecture seule.

### <a name="example-code"></a>Exemple de code

Le code suivant montre comment vérifier si un code PIN prend en charge ce jeu de propriétés et, le cas échéant, comment obtenir la catégorie de code confidentiel :


```C++
HRESULT GetPinCategory(IPin *pPin, GUID *pPinCategory)
{
    IKsPropertySet *pKs = NULL;

    HRESULT hr = pPin->QueryInterface(IID_PPV_ARGS(&pKs));
    if (FAILED(hr))
    {
        return hr;
    }

    // Try to retrieve the pin category.
    DWORD cbReturned = 0;
    hr = pKs->Get(AMPROPSETID_Pin, AMPROPERTY_PIN_CATEGORY, NULL, 0, 
        pPinCategory, sizeof(GUID), &cbReturned);
    
    // If this succeeded, pPinCategory now contains the category GUID.

    SafeRelease(&pKs);
    return hr;
}
```



> [!Note]  
> Cet exemple utilise la fonction [SafeRelease](../medfound/saferelease.md) pour libérer des pointeurs d’interface.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exigences de code confidentiel pour les filtres de capture](pin-requirements-for-capture-filters.md)
</dt> <dt>

[Jeux de propriétés](property-sets.md)
</dt> <dt>

[Utilisation des catégories de code confidentiel](working-with-pin-categories.md)
</dt> </dl>

 

 
