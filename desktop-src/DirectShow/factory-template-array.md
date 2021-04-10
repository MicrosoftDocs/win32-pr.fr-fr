---
description: Tableau de modèles de fabrique
ms.assetid: 310afccd-42a6-426e-b455-7bf98062bf36
title: Tableau de modèles de fabrique
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f2c8d05f37ab64142747755d6a0e7727f4b11
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109899"
---
# <a name="factory-template-array"></a>Tableau de modèles de fabrique

Le modèle Factory contient les variables membres publiques suivantes :

``` syntax
const WCHAR *              m_Name;                // Name
const CLSID *              m_ClsID;               // CLSID
LPFNNewCOMObject           m_lpfnNew;             // Function to create an instance
                                                  //   of the component
LPFNInitRoutine            m_lpfnInit;            // Initialization function (optional)
const AMOVIESETUP_FILTER * m_pAMovieSetup_Filter; // Set-up information (for filters)
```

Les deux pointeurs de fonction, [**m \_ lpfnNew**](cfactorytemplate-m-lpfnnew.md) et [**m \_ lpfnInit**](cfactorytemplate-m-lpfninit.md), utilisent les définitions de type suivantes :

``` syntax
typedef CUnknown *(CALLBACK *LPFNNewCOMObject)(LPUNKNOWN pUnkOuter, HRESULT *phr);
typedef void (CALLBACK *LPFNInitRoutine)(BOOL bLoading, const CLSID *rclsid);
```

La première est la fonction d’instanciation du composant. La seconde est une fonction d’initialisation facultative. Si vous fournissez une fonction d’initialisation, elle est appelée depuis l’intérieur de la fonction de point d’entrée DLL. (La fonction de point d’entrée DLL est présentée plus loin dans cet article.)

Supposons que vous créez une DLL qui contient un composant nommé CMyComponent, qui hérite de [**CUnknown**](cunknown.md). Vous devez fournir les éléments suivants dans votre DLL :

-   La fonction d’initialisation, une méthode publique qui retourne une nouvelle instance de CMyComponent.
-   Tableau global de modèles de fabrique, appelés *\_ modèles g.* Ce tableau contient le modèle de fabrique pour CMyComponent.
-   Une variable globale nommée *g \_ cTemplates* qui spécifie la taille du tableau.

L’exemple suivant montre comment déclarer ces éléments :


```C++
// Public method that returns a new instance. 
CUnknown * WINAPI CMyComponent::CreateInstance(LPUNKNOWN pUnk, HRESULT *pHr) 
{
    CMyComponent *pNewObject = new CMyComponent(NAME("My Component"), pUnk, pHr );
    if (pNewObject == NULL) {
        *pHr = E_OUTOFMEMORY;
    }
    return pNewObject;
} 

CFactoryTemplate g_Templates[1] = 
{
    { 
      L"My Component",                // Name
      &CLSID_MyComponent,             // CLSID
      CMyComponent::CreateInstance,   // Method to create an instance of MyComponent
      NULL,                           // Initialization function
      NULL                            // Set-up information (for filters)
    }
};
int g_cTemplates = sizeof(g_Templates) / sizeof(g_Templates[0]);    
```



La `CreateInstance` méthode appelle le constructeur de classe et retourne un pointeur vers la nouvelle instance de classe. Le paramètre *punk* est un pointeur vers l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)d’agrégation. Vous pouvez simplement passer ce paramètre au constructeur de classe. Le paramètre *pHr* est un pointeur vers une valeur HRESULT. Le constructeur de classe affecte à ce paramètre une valeur appropriée, mais si le constructeur échoue, définissez la valeur sur E \_ OUTOFMEMORY.

La macro [**Name**](name.md) génère une chaîne dans les versions Debug, mais résout la **valeur null** dans les builds de vente au détail. Il est utilisé dans cet exemple pour attribuer au composant un nom qui apparaît dans les journaux de débogage, mais n’occupe pas la mémoire dans la version finale.

La `CreateInstance` méthode peut avoir n’importe quel nom, car la fabrique de classe fait référence au pointeur de fonction dans le modèle de fabrique. Toutefois, *les \_ modèles g* et *g \_ cTemplates* sont des variables globales que la fabrique de classes s’attend à trouver. elles doivent donc avoir exactement ces noms.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment créer une DLL de filtre DirectShow](how-to-create-a-dll.md)
</dt> </dl>

 

 
