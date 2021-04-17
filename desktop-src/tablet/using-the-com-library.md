---
description: Vue d’ensemble de la bibliothèque COM et notes sur l’utilisation des sections de la technologie Tablet PC du kit de développement logiciel (SDK) Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Utilisation de la bibliothèque COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d82671b198114cf45b334e8c4e07146a91964e4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318289"
---
# <a name="using-the-com-library"></a><span data-ttu-id="75824-103">Utilisation de la bibliothèque COM</span><span class="sxs-lookup"><span data-stu-id="75824-103">Using the COM Library</span></span>

<span data-ttu-id="75824-104">La référence de la bibliothèque managée Tablet PC est désormais disponible dans la section Référence de la bibliothèque de classes du kit de développement logiciel (SDK) Windows Vista standard.</span><span class="sxs-lookup"><span data-stu-id="75824-104">The Tablet PC managed library reference can now be found in the regular Windows Vista SDK Class Library reference section.</span></span> <span data-ttu-id="75824-105">Il fournit un modèle objet pour Microsoft Visual C++.</span><span class="sxs-lookup"><span data-stu-id="75824-105">It provides an object model for Microsoft Visual C++.</span></span> <span data-ttu-id="75824-106">La majorité des objets de la bibliothèque COM sont identiques à ceux qui se trouvent dans l’API gérée Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="75824-106">The majority of the objects in the COM Library are identical to those found in the Tablet PC Managed API.</span></span>

<span data-ttu-id="75824-107">Toutefois, l’API COM contient certains membres en plus de ceux de l’API managée en raison de différences entre l’environnement Microsoft Win32 standard et l’environnement du kit de développement (SDK) Microsoft .NET Frameworksoftware.</span><span class="sxs-lookup"><span data-stu-id="75824-107">However, the COM API contains some members in addition to those found in the Managed API because of differences between the standard Microsoft Win32 environment and the Microsoft .NET Frameworksoftware development kit (SDK) environment.</span></span> <span data-ttu-id="75824-108">Par exemple, les objets InkRectangle et InkTransform sont utilisés dans COM, mais le FrameworkSDK fournit une implémentation native pour la [**classe InkRectangle**](inkrectangle-class.md) et la [**classe InkTransform**](inktransform-class.md) qui élimine le besoin de ces objets dans l’API managée de la plateforme Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="75824-108">For example, the InkRectangle and InkTransform objects are used in COM, but the FrameworkSDK provides native implementation for [**InkRectangle Class**](inkrectangle-class.md) and [**InkTransform Class**](inktransform-class.md) that eliminates the need for these objects in the Tablet PC platform Managed API.</span></span>

> [!Note]  
> <span data-ttu-id="75824-109">Les objets de l’API COM et les contrôles Ink ne sont pas conçus pour être utilisés dans les pages d’Active Server (ASP).</span><span class="sxs-lookup"><span data-stu-id="75824-109">The objects in the COM API and the ink controls are not designed for use in Active Server Pages (ASP).</span></span>

 

## <a name="working-with-collections"></a><span data-ttu-id="75824-110">Utilisation des regroupements</span><span class="sxs-lookup"><span data-stu-id="75824-110">Working with Collections</span></span>

<span data-ttu-id="75824-111">Si vous transmettez une valeur **null** en tant qu’index à l’un des objets de collection de la bibliothèque com, vous recevez le premier élément de la collection, car ces valeurs d’argument sont forcées à 0 lorsque l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="75824-111">If you pass in a **NULL** value as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

<span data-ttu-id="75824-112">La propriété **\_ NewEnum** est marquée comme restreinte dans la définition IDL (Interface Definition Language) pour les interfaces de collection.</span><span class="sxs-lookup"><span data-stu-id="75824-112">The **\_NewEnum** property is marked restricted in the Interface Definition Language (IDL) definition for the collection interfaces.</span></span>

<span data-ttu-id="75824-113">En C++, utilisez une `For...` boucle pour itérer au sein d’une collection en obtenant d’abord la longueur de la collection.</span><span class="sxs-lookup"><span data-stu-id="75824-113">In C++, use a `For...` loop to iterate through a collection by first obtaining the collection's length.</span></span> <span data-ttu-id="75824-114">L’exemple ci-dessous montre comment itérer au sein des traits d’un objet [**InkDisp**](inkdisp-class.md) , `pInk` .</span><span class="sxs-lookup"><span data-stu-id="75824-114">The example below shows how to iterate through the strokes of an [**InkDisp**](inkdisp-class.md) object, `pInk`.</span></span>


```C++
IInkStrokes* pStrokes;
HRESULT result = pInk->get_Strokes(&pStrokes);
if (SUCCEEDED(result))
{
    // Loop over strokes
    long nStrokes;
    result = pStrokes->get_Count(&nStrokes);
    if (SUCCEEDED(result))
    {
        for (int i =0; i < nStrokes; i++)
        {
            IInkStrokeDisp* pStroke;
            result = pStrokes->Item(i, &pStroke);
            if (SUCCEEDED(result))
            {
              // Code that uses pStroke
              // ...
            }
        }
    }
}
```



## <a name="parameters"></a><span data-ttu-id="75824-115">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75824-115">Parameters</span></span>

<span data-ttu-id="75824-116">Si vous transmettez VT \_ vide ou VT \_ null comme index de l’un des objets de collection de la bibliothèque com, vous recevez le premier élément de la collection, car ces valeurs d’argument sont forcées à 0 lorsque l’appel est effectué.</span><span class="sxs-lookup"><span data-stu-id="75824-116">If you pass in VT\_EMPTY or VT\_NULL as the index to any of the collection objects in the COM Library, you receive the first item in the collection because these argument values are coerced to 0 when the call is made.</span></span>

## <a name="using-idispatch"></a><span data-ttu-id="75824-117">Utilisation de IDispatch</span><span class="sxs-lookup"><span data-stu-id="75824-117">Using IDispatch</span></span>

<span data-ttu-id="75824-118">Pour améliorer les performances, l’interface de programmation d’applications (API) COM de la plateforme Tablet PC ne prend pas en charge l’appel `IDispatchImpl::Invoke` avec une structure DISPPARAMS avec des arguments nommés.</span><span class="sxs-lookup"><span data-stu-id="75824-118">To increase performance, the Tablet PC Platform COM application programming interface (API) does not support calling `IDispatchImpl::Invoke` with a DISPPARAMS structure with named arguments.</span></span> <span data-ttu-id="75824-119">Le `IDispatchImpl::GetIDsOfNames` n’est pas non plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="75824-119">The `IDispatchImpl::GetIDsOfNames` is also not supported.</span></span> <span data-ttu-id="75824-120">Au lieu de cela, appelez `Invoke` avec les DISPID fournis dans les en-têtes du kit de développement logiciel (SDK).</span><span class="sxs-lookup"><span data-stu-id="75824-120">Instead, call `Invoke` with the DISPIDs supplied in the SDK headers.</span></span>

## <a name="waiting-for-events"></a><span data-ttu-id="75824-121">En attente d’événements</span><span class="sxs-lookup"><span data-stu-id="75824-121">Waiting for Events</span></span>

<span data-ttu-id="75824-122">L’environnement Tablet PC est multithread.</span><span class="sxs-lookup"><span data-stu-id="75824-122">The Tablet PC environment is multithreaded.</span></span> <span data-ttu-id="75824-123">Reportez-vous à la documentation COM pour le Multi-Threading.</span><span class="sxs-lookup"><span data-stu-id="75824-123">Refer to COM documentation for multi-threading.</span></span>

## <a name="support-for-aggregation"></a><span data-ttu-id="75824-124">Prise en charge de l’agrégation</span><span class="sxs-lookup"><span data-stu-id="75824-124">Support for Aggregation</span></span>

<span data-ttu-id="75824-125">L’agrégation a été testée uniquement pour le contrôle [InkEdit](inkedit-control-reference.md) , le contrôle [InkPicture](inkpicture-control-reference.md) , l’objet [**InkDisp**](inkdisp-class.md) et l’objet [**InkOverlay**](inkoverlay-class.md) .</span><span class="sxs-lookup"><span data-stu-id="75824-125">Aggregation has been tested for only the [InkEdit](inkedit-control-reference.md) control, the [InkPicture](inkpicture-control-reference.md) control, the [**InkDisp**](inkdisp-class.md) object, and the [**InkOverlay**](inkoverlay-class.md) object.</span></span> <span data-ttu-id="75824-126">L’agrégation n’a pas été testée pour d’autres contrôles et objets de la bibliothèque.</span><span class="sxs-lookup"><span data-stu-id="75824-126">Aggregation has not been tested for other controls and objects in the library.</span></span>

## <a name="c"></a><span data-ttu-id="75824-127">C++</span><span class="sxs-lookup"><span data-stu-id="75824-127">C++</span></span>

<span data-ttu-id="75824-128">L’utilisation du kit de développement logiciel (SDK) Tablet PC en C++ requiert l’utilisation de certains concepts COM, tels que VARIANT, SAFEARRAY et BSTR.</span><span class="sxs-lookup"><span data-stu-id="75824-128">Using the Tablet PC SDK in C++ requires the use of some COM concepts, such as VARIANT, SAFEARRAY, and BSTR.</span></span> <span data-ttu-id="75824-129">Cette section explique comment les utiliser.</span><span class="sxs-lookup"><span data-stu-id="75824-129">This section describes how to use them.</span></span>

### <a name="variant-and-safearray"></a><span data-ttu-id="75824-130">VARIANT et SAFEARRAY</span><span class="sxs-lookup"><span data-stu-id="75824-130">VARIANT and SAFEARRAY</span></span>

<span data-ttu-id="75824-131">La structure VARIANT est utilisée pour la communication entre les objets COM.</span><span class="sxs-lookup"><span data-stu-id="75824-131">The VARIANT structure is used for communication between COM objects.</span></span> <span data-ttu-id="75824-132">Fondamentalement, la structure VARIANT est un conteneur pour une grande Union qui transporte de nombreux types de données.</span><span class="sxs-lookup"><span data-stu-id="75824-132">Essentially, the VARIANT structure is a container for a large union that carries many types of data.</span></span>

<span data-ttu-id="75824-133">La valeur du premier membre de la structure, VT, décrit les membres de l’Union qui sont valides.</span><span class="sxs-lookup"><span data-stu-id="75824-133">The value in the first member of the structure, vt, describes which of the union members is valid.</span></span> <span data-ttu-id="75824-134">Lorsque vous recevez des informations dans une structure de variante, vérifiez le membre VT pour savoir quel membre contient des données valides.</span><span class="sxs-lookup"><span data-stu-id="75824-134">When you receive information in a VARIANT structure, check the vt member to find out which member contains valid data.</span></span> <span data-ttu-id="75824-135">De même, lorsque vous envoyez des informations à l’aide d’une structure VARIANT, définissez toujours VT pour refléter le membre d’Union qui contient les informations.</span><span class="sxs-lookup"><span data-stu-id="75824-135">Similarly, when you send information using a VARIANT structure, always set vt to reflect the union member that contains the information.</span></span>

<span data-ttu-id="75824-136">Avant d’utiliser la structure, initialisez-la en appelant la fonction COM VariantInit.</span><span class="sxs-lookup"><span data-stu-id="75824-136">Before using the structure, initialize it by calling the VariantInit COM function.</span></span> <span data-ttu-id="75824-137">Lorsque vous avez terminé avec la structure, effacez-la avant de libérer la mémoire qui contient la variante en appelant VariantClear.</span><span class="sxs-lookup"><span data-stu-id="75824-137">When finished with the structure, clear it before the memory that contains the VARIANT is freed by calling VariantClear.</span></span>

<span data-ttu-id="75824-138">Pour plus d’informations sur la structure de la variante, consultez [types de données Variant et VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span><span class="sxs-lookup"><span data-stu-id="75824-138">For more information on the VARIANT structure, see [VARIANT and VARIANTARG Data Types](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="75824-139">La structure SAFEARRAY est fournie comme un moyen de travailler en toute sécurité sur des tableaux dans COM.</span><span class="sxs-lookup"><span data-stu-id="75824-139">The SAFEARRAY structure is provided as a way to safely work with arrays in COM.</span></span> <span data-ttu-id="75824-140">Le champ pArray de la variante est un pointeur vers un SAFEARRAY.</span><span class="sxs-lookup"><span data-stu-id="75824-140">The VARIANT's parray field is a pointer to a SAFEARRAY.</span></span> <span data-ttu-id="75824-141">Utilisez des fonctions telles que SafeArrayCreateVector, SafeArrayAccessData et SafeArrayUnaccessData pour créer et remplir un SAFEARRAY dans un VARIANT.</span><span class="sxs-lookup"><span data-stu-id="75824-141">Use functions such as SafeArrayCreateVector, SafeArrayAccessData, and SafeArrayUnaccessData to create and fill a SAFEARRAY in a VARIANT.</span></span>

<span data-ttu-id="75824-142">Pour plus d’informations sur le type de données SAFEARRAY, consultez [SAFEARRAY Data type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span><span class="sxs-lookup"><span data-stu-id="75824-142">For more information on the SAFEARRAY data type, see [SafeArray Data Type](/windows/win32/api/oaidl/ns-oaidl-safearray).</span></span>

<span data-ttu-id="75824-143">Cet exemple C++ crée un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , dans un objet [**InkDisp**](inkdisp-class.md) , `pInk` , à partir d’un tableau de données point.</span><span class="sxs-lookup"><span data-stu-id="75824-143">This C++ example creates an [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp`, in an [**InkDisp**](inkdisp-class.md) object, `pInk`, from an array of point data.</span></span>


```C++
VARIANT   var, varPK;
LONG*   plongArray=NULL;
POINT   ptArray[2]={0};
long   lSize=0;
IInkStrokeDisp* pInkStrokeDisp;

IInkDisp*   pInk;   // the object should be created correctly 
                    // elsewhere and assigned here.
HRESULT   hr=E_FAIL;

ptArray[0].x = 20;
ptArray[0].y = 100;
ptArray[1].x = 30;
ptArray[1].y = 110;
lSize = 2;   // two points

VariantInit( &var );
VariantInit( &varPK );
SAFEARRAY* psa = SafeArrayCreateVector( VT_I4, 0, lSize*2 );
if( psa )
{
  if( SUCCEEDED( hr = SafeArrayAccessData( psa, (void**)&plongArray) ))
   {
      for( long i = 0; i < lSize; i++ ) 
      {
         plongArray[2*i] = ptArray[i].x;
         plongArray[2*i+1] = ptArray[i].y;
      }
      hr = SafeArrayUnaccessData( psa );

      if ( SUCCEEDED( hr ) ) 
      {
         var.vt     = VT_ARRAY | VT_I4;
         var.parray = psa;

        // varPK (packet description) is currently reserved, so it is
        // just empty variant for now.
         pInk->CreateStroke( var, varPK, &pInkStrokeDisp );   
      }
   }
}
VariantClear( &var );
VariantClear( &varPK );
```



### <a name="bstr"></a><span data-ttu-id="75824-144">BSTR</span><span class="sxs-lookup"><span data-stu-id="75824-144">BSTR</span></span>

<span data-ttu-id="75824-145">Le format de chaîne pris en charge pour COM est BSTR.</span><span class="sxs-lookup"><span data-stu-id="75824-145">The supported string format for COM is BSTR.</span></span> <span data-ttu-id="75824-146">Un BSTR a un pointeur vers une chaîne se terminant par zéro, mais il contient également la longueur de la chaîne (en octets, sans compter le terminateur), qui est stockée dans les 4 octets qui précèdent immédiatement le premier caractère de la chaîne.</span><span class="sxs-lookup"><span data-stu-id="75824-146">A BSTR has a pointer to a zero-terminated string, but it also contains the length of the string (in bytes, not counting the terminator), which is stored in the 4 bytes immediately preceding the first character of the string.</span></span>

<span data-ttu-id="75824-147">Pour plus d’informations sur BSTR, consultez [type de données BSTR](/previous-versions/windows/desktop/automat/bstr).</span><span class="sxs-lookup"><span data-stu-id="75824-147">For more information on BSTR, see [BSTR Data Type](/previous-versions/windows/desktop/automat/bstr).</span></span>

<span data-ttu-id="75824-148">Cet exemple C++ montre comment définir le Factoid sur un [**InkRecognizerContext**](inkrecognizercontext-class.md) à l’aide d’un BSTR.</span><span class="sxs-lookup"><span data-stu-id="75824-148">This C++ sample shows how to set the factoid on an [**InkRecognizerContext**](inkrecognizercontext-class.md) using a BSTR.</span></span>


```C++
IInkRecognizerContext* pRecognizerContext = NULL;
result = CoCreateInstance(CLSID_InkRecognizerContext, 
    NULL, CLSCTX_INPROC_SERVER,
    IID_IInkRecognizerContext, 
    (void **) &pRecognizerContext);
if SUCCEEDED(result)
{
    BSTR bstrFactoid = SysAllocString(FACTOID_DATE);
    result = pRecognizerContext->put_Factoid(bstrFactoid);
    if SUCCEEDED(result)
    {
      // Use recognizer context...
      // ...
    }
    SysFreeString(bstrFactoid);
}
```



 

 
