---
description: Exposer les nouvelles interfaces d’un filtre aux clients dans le cadre de la création d’une page de propriétés de filtre pour un filtre DirectShow personnalisé.
ms.assetid: a0e52ba9-9f7c-4cf3-ba5f-b0035ed1794c
title: Étape 3. Prendre en charge QueryInterface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b62132a6f24c68453ad4e51f72cdd9a2a78c65
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112410022"
---
# <a name="step-3-support-queryinterface"></a>Étape 3. Prendre en charge QueryInterface

Pour exposer les nouvelles interfaces du filtre aux clients, procédez comme suit :

-   Incluez la macro [**Declare \_ IUnknown**](declare-iunknown.md) dans la section Déclaration publique de votre filtre :
    ```C++
    public:
        DECLARE_IUNKNOWN;
    ```

    

-   Remplacez [**CUnknown :: NonDelegatingQueryInterface**](cunknown-nondelegatingqueryinterface.md) pour vérifier les IID des deux interfaces :
    ```C++
    STDMETHODIMP CGrayFilter::NonDelegatingQueryInterface(REFIID riid, void **ppv)
    {
        if (riid == IID_ISpecifyPropertyPages)
        {
            return GetInterface(
               static_cast<ISpecifyPropertyPages*>(this),
               ppv);
        }
        else if (riid == IID_ISaturation)
        {
            return GetInterface(static_cast<ISaturation*>(this), ppv);
        }
        else
        {
            // Call the parent class.
            return CBaseFilter::NonDelegatingQueryInterface(riid, ppv);

            // NOTE: This example assumes that the filter inherits directly
            // from CBaseFilter. If your filter inherits from another class,
            // call the NonDelegatingQueryInterface method of that class.
        }
    }
    ```

    

Suivant : [étape 4. Créez la page de propriétés](step-4--create-the-property-page.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> <dt>

[Comment implémenter IUnknown](how-to-implement-iunknown.md)
</dt> </dl>

 

 



