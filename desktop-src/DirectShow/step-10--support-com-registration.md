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
# <a name="step-10-support-com-registration"></a><span data-ttu-id="c20c0-104">Étape 10.</span><span class="sxs-lookup"><span data-stu-id="c20c0-104">Step 10.</span></span> <span data-ttu-id="c20c0-105">Prise en charge de l’inscription COM</span><span class="sxs-lookup"><span data-stu-id="c20c0-105">Support COM Registration</span></span>

<span data-ttu-id="c20c0-106">La dernière tâche restante consiste à prendre en charge l’inscription COM, afin que le frame de propriété puisse créer des instances de votre page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c20c0-106">The last remaining task is to support COM registration, so that the property frame can create new instances of your property page.</span></span> <span data-ttu-id="c20c0-107">Ajoutez une autre entrée [**CFactoryTemplate**](cfactorytemplate.md) au tableau global *g \_ Templates* , qui est utilisé pour inscrire tous les objets COM dans votre dll.</span><span class="sxs-lookup"><span data-stu-id="c20c0-107">Add another [**CFactoryTemplate**](cfactorytemplate.md) entry to the global *g\_Templates* array, which is used to register all of the COM objects in your DLL.</span></span> <span data-ttu-id="c20c0-108">N’incluez pas d’informations de paramétrage de filtre pour la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c20c0-108">Do not include any filter set-up information for the property page.</span></span>


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



<span data-ttu-id="c20c0-109">Si vous déclarez *g \_ cTemplates* comme indiqué dans le code suivant, il a automatiquement la valeur correcte en fonction de la taille du tableau :</span><span class="sxs-lookup"><span data-stu-id="c20c0-109">If you declare *g\_cTemplates* as shown in the following code, then it automatically has the correct value based on the array size:</span></span>


```C++
int g_cTemplates = sizeof(g_Templates)/sizeof(g_Templates[0]);
```



<span data-ttu-id="c20c0-110">Ajoutez également une méthode statique `CreateInstance` à la classe de la page de propriétés.</span><span class="sxs-lookup"><span data-stu-id="c20c0-110">Also, add a static `CreateInstance` method to the property page class.</span></span> <span data-ttu-id="c20c0-111">Vous pouvez nommer la méthode comme vous le souhaitez, mais la signature doit correspondre à celle illustrée dans l’exemple suivant :</span><span class="sxs-lookup"><span data-stu-id="c20c0-111">You can name the method anything that you prefer, but the signature must match the one shown the following example:</span></span>


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



<span data-ttu-id="c20c0-112">Pour tester la page de propriétés, inscrivez la DLL, puis chargez le filtre dans GraphEdit.</span><span class="sxs-lookup"><span data-stu-id="c20c0-112">To test the property page, register the DLL and then load the filter in GraphEdit.</span></span> <span data-ttu-id="c20c0-113">Cliquez avec le bouton droit sur le filtre et sélectionnez **Propriétés du filtre**.</span><span class="sxs-lookup"><span data-stu-id="c20c0-113">Right-click the filter and select **Filter Properties**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c20c0-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c20c0-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c20c0-115">Création d’une page de propriétés de filtre</span><span class="sxs-lookup"><span data-stu-id="c20c0-115">Creating a Filter Property Page</span></span>](creating-a-filter-property-page.md)
</dt> <dt>

[<span data-ttu-id="c20c0-116">Comment créer une DLL de filtre DirectShow</span><span class="sxs-lookup"><span data-stu-id="c20c0-116">How to Create a DirectShow Filter DLL</span></span>](how-to-create-a-dll.md)
</dt> </dl>

 

 



