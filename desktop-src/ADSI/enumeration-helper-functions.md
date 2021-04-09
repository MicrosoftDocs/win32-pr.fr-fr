---
title: Fonctions d’assistance d’énumération
description: Il existe trois fonctions d’assistance d’énumérateur qui peuvent être utilisées à partir de C/C++ pour faciliter la navigation dans les objets Active Directory. Il s’agit de ADsBuildEnumerator, ADsEnumerateNext et ADsFreeEnumerator.
ms.assetid: 019958c8-5bf5-45eb-871c-796ff3750cdc
ms.tgt_platform: multiple
keywords:
- ADsBuildEnumerator ADSI, utilisation
- ADsEnumerateNext ADSI, utilisation
- ADsFreeEnumerator ADSI, utilisation
- ADSI ADSI, exemple de code C/C++, utilisant ADsBuildEnumerator ADsEnumerateNext et ADsFreeEnumerator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af9597787202adf183435262eab9341957e19457
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "104102337"
---
# <a name="enumeration-helper-functions"></a><span data-ttu-id="2cf16-108">Fonctions d’assistance d’énumération</span><span class="sxs-lookup"><span data-stu-id="2cf16-108">Enumeration Helper Functions</span></span>

<span data-ttu-id="2cf16-109">Il existe trois fonctions d’assistance d’énumérateur qui peuvent être utilisées à partir de C/C++ pour faciliter la navigation dans les objets Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2cf16-109">There are three enumerator helper functions that can be used from C/C++ to aid in the navigation of Active Directory objects.</span></span> <span data-ttu-id="2cf16-110">Il s’agit de [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext)et [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span><span class="sxs-lookup"><span data-stu-id="2cf16-110">They are [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator), [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext), and [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator).</span></span>

## <a name="adsbuildenumerator"></a><span data-ttu-id="2cf16-111">ADsBuildEnumerator</span><span class="sxs-lookup"><span data-stu-id="2cf16-111">ADsBuildEnumerator</span></span>

<span data-ttu-id="2cf16-112">La fonction d’assistance [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) encapsule le code requis pour créer un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="2cf16-112">The [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) helper function encapsulates the code required to create an enumerator object.</span></span> <span data-ttu-id="2cf16-113">Elle appelle la méthode [**IADsContainer :: obtenir \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) pour créer un objet énumérateur, puis appelle la méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pour obtenir un pointeur vers l’interface [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) pour cet objet.</span><span class="sxs-lookup"><span data-stu-id="2cf16-113">It calls the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscontainer-get__newenum) method to create an enumerator object and then calls the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) to get a pointer to the [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) interface for that object.</span></span> <span data-ttu-id="2cf16-114">L’objet d’énumération est le mécanisme d’automatisation pour énumérer des conteneurs.</span><span class="sxs-lookup"><span data-stu-id="2cf16-114">The enumeration object is the Automation mechanism to enumerate over containers.</span></span> <span data-ttu-id="2cf16-115">Utilisez la fonction [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) pour libérer cet objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="2cf16-115">Use the [**ADsFreeEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsfreeenumerator) function to release this enumerator object.</span></span>

## <a name="adsenumeratenext"></a><span data-ttu-id="2cf16-116">ADsEnumerateNext</span><span class="sxs-lookup"><span data-stu-id="2cf16-116">ADsEnumerateNext</span></span>

<span data-ttu-id="2cf16-117">La fonction d’assistance [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) remplit un tableau de variants avec les éléments extraits d’un objet énumérateur.</span><span class="sxs-lookup"><span data-stu-id="2cf16-117">The [**ADsEnumerateNext**](/windows/desktop/api/Adshlp/nf-adshlp-adsenumeratenext) helper function populates a VARIANT array with elements fetched from an enumerator object.</span></span> <span data-ttu-id="2cf16-118">Le nombre d’éléments récupérés peut être inférieur au nombre demandé.</span><span class="sxs-lookup"><span data-stu-id="2cf16-118">The number of elements retrieved can be smaller than the number requested.</span></span>

## <a name="adsfreeenumerator"></a><span data-ttu-id="2cf16-119">ADsFreeEnumerator</span><span class="sxs-lookup"><span data-stu-id="2cf16-119">ADsFreeEnumerator</span></span>

<span data-ttu-id="2cf16-120">Libère un objet énumérateur créé précédemment à l’aide de la fonction [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) .</span><span class="sxs-lookup"><span data-stu-id="2cf16-120">Frees an enumerator object previously created through the [**ADsBuildEnumerator**](/windows/desktop/api/Adshlp/nf-adshlp-adsbuildenumerator) function.</span></span>

<span data-ttu-id="2cf16-121">L’exemple de code suivant montre une fonction qui utilise des fonctions d’assistance d’énumérateur en C++.</span><span class="sxs-lookup"><span data-stu-id="2cf16-121">The following code example shows a function that uses enumerator helper functions in C++.</span></span>


```C++
/*****************************************************************************
  Function:    TestEnumObject
  Arguments:   pszADsPath - ADsPath of the container to be enumerated (WCHAR*).
  Return:      S_OK if successful, an error code otherwise.
  Purpose:     Example using ADsBuildEnumerator, ADsEnumerateNext and
               ADsFreeEnumerator.
******************************************************************************/
#define MAX_ENUM      100  
 
HRESULT
TestEnumObject( LPWSTR pszADsPath )
{
    ULONG cElementFetched = 0L;
    IEnumVARIANT * pEnumVariant = NULL;
    VARIANT VariantArray[MAX_ENUM];
    HRESULT hr = S_OK;
    IADsContainer * pADsContainer =  NULL;
    DWORD dwObjects = 0, dwEnumCount = 0, i = 0;
    BOOL  fContinue = TRUE;
 
 
    hr = ADsGetObject(
                pszADsPath,
                IID_IADsContainer,
                (void **)&pADsContainer
                );
 
 
    if (FAILED(hr)) {
 
        printf("\"%S\" is not a valid container object.\n", pszADsPath) ;
        goto exitpoint ;
    }
 
    hr = ADsBuildEnumerator(
            pADsContainer,
            &pEnumVariant
            );
 
    if( FAILED( hr ) )
    {
      printf("ADsBuildEnumerator failed with %lx\n", hr ) ;
      goto exitpoint ;
    }
 
    fContinue  = TRUE;
    while (fContinue) {
 
        IADs *pObject ;
 
        hr = ADsEnumerateNext(
                    pEnumVariant,
                    MAX_ENUM,
                    VariantArray,
                    &cElementFetched
                    );

        if ( FAILED( hr ) )
        {
            printf("ADsEnumerateNext failed with %lx\n",hr);
            goto exitpoint;
        }
 
        if (hr == S_FALSE) {
            fContinue = FALSE;
        }
 
        dwEnumCount++;
 
        for (i = 0; i < cElementFetched; i++ ) {
 
            IDispatch *pDispatch    = NULL;
            BSTR        bstrADsPath = NULL;
 
            pDispatch = VariantArray[i].pdispVal;
 
            hr = V_DISPATCH( VariantArray + i )->QueryInterface(IID_IADs, (void **) &pObject) ;
 
            if( SUCCEEDED( hr ) )
            {
               pObject->get_ADsPath( &bstrADsPath );
               printf( "%S\n", bstrADsPath );
            }
            pObject->Release();
            VariantClear( VariantArray + i );
            SysFreeString( bstrADsPath );
        }
 
        dwObjects += cElementFetched;
    }
 
    printf("Total Number of Objects enumerated is %d\n", dwObjects);
 
exitpoint:
    if (pEnumVariant) {
        ADsFreeEnumerator( pEnumVariant );
    }
 
    if (pADsContainer) {
        pADsContainer->Release();
    }
 
    return(hr);
}
```



 

 