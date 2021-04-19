---
description: Étape 10.
ms.assetid: 2959f574-1a39-4db1-9e4a-a303d0c7f8f3
title: Étape 10. Prise en charge de l’inscription COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fead7e3448d8f02fd477141699e1107ca288afd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541848"
---
# <a name="step-10-support-com-registration"></a>Étape 10. Prise en charge de l’inscription COM

La dernière tâche restante consiste à prendre en charge l’inscription COM, afin que le frame de propriété puisse créer des instances de votre page de propriétés. Ajoutez une autre entrée [**CFactoryTemplate**](cfactorytemplate.md) au tableau global *g \_ Templates* , qui est utilisé pour inscrire tous les objets COM dans votre dll. N’incluez pas d’informations de paramétrage de filtre pour la page de propriétés.


```C++
const AMOVIESETUP_FILTER FilterSetupData = 
{ 
    /* Not shown ... */
};

CFactoryTemplate g_Templates[] =
{   
    // This entry is for the filter.
    {
        wszName,
        &CLSID_GrayFilter,
        CGrayFilter::CreateInstance,
        NULL,
        &FilterSetupData 
    },
    // This entry is for the property page.
    { 
        L"Saturation Props",
        &CLSID_SaturationProp,
        CGrayProp::CreateInstance, 
        NULL, NULL
    }
};
```



Si vous déclarez *g \_ cTemplates* comme indiqué dans le code suivant, il a automatiquement la valeur correcte en fonction de la taille du tableau :


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



Ajoutez également une méthode statique `CreateInstance` à la classe de la page de propriétés. Vous pouvez nommer la méthode comme vous le souhaitez, mais la signature doit correspondre à celle illustrée dans l’exemple suivant :


```C++
static CUnknown * WINAPI CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CGrayProp *pNewObject = new CGrayProp(pUnk);
    if (pNewObject == NULL) 
    {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 
```



Pour tester la page de propriétés, inscrivez la DLL, puis chargez le filtre dans GraphEdit. Cliquez avec le bouton droit sur le filtre et sélectionnez **Propriétés du filtre**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création d’une page de propriétés de filtre](creating-a-filter-property-page.md)
</dt> <dt>

[Comment créer une DLL de filtre DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 



