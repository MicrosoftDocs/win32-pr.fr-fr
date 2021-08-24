---
description: vue d’ensemble de la bibliothèque COM et notes sur l’utilisation des sections de la technologie Tablet PC du kit de développement logiciel (SDK) Windows Vista.
ms.assetid: fa43fad9-804c-42d9-9717-6686d5f98ed8
title: Utilisation de la bibliothèque COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf986d79011301abe6a9f279a83278fda5dd9e33e3a79335d7d94e6081fb11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819139"
---
# <a name="using-the-com-library"></a>Utilisation de la bibliothèque COM

la référence de la bibliothèque managée Tablet PC est désormais disponible dans la section référence de la bibliothèque de classes du kit de développement logiciel (SDK) standard Windows Vista. Il fournit un modèle objet pour Microsoft Visual C++. La majorité des objets de la bibliothèque COM sont identiques à ceux qui se trouvent dans l’API gérée Tablet PC.

Toutefois, l’API COM contient certains membres en plus de ceux de l’API managée en raison de différences entre l’environnement Microsoft Win32 standard et l’environnement du kit de développement (SDK) Microsoft .NET Frameworksoftware. Par exemple, les objets InkRectangle et InkTransform sont utilisés dans COM, mais le FrameworkSDK fournit une implémentation native pour la [**classe InkRectangle**](inkrectangle-class.md) et la [**classe InkTransform**](inktransform-class.md) qui élimine le besoin de ces objets dans l’API managée de la plateforme Tablet PC.

> [!Note]  
> Les objets de l’API COM et les contrôles Ink ne sont pas conçus pour être utilisés dans les pages d’Active Server (ASP).

 

## <a name="working-with-collections"></a>Utilisation des regroupements

Si vous transmettez une valeur **null** en tant qu’index à l’un des objets de collection de la bibliothèque com, vous recevez le premier élément de la collection, car ces valeurs d’argument sont forcées à 0 lorsque l’appel est effectué.

La propriété **\_ NewEnum** est marquée comme restreinte dans la définition IDL (Interface Definition Language) pour les interfaces de collection.

En C++, utilisez une `For...` boucle pour itérer au sein d’une collection en obtenant d’abord la longueur de la collection. L’exemple ci-dessous montre comment itérer au sein des traits d’un objet [**InkDisp**](inkdisp-class.md) , `pInk` .


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



## <a name="parameters"></a>Paramètres

Si vous transmettez VT \_ vide ou VT \_ null comme index de l’un des objets de collection de la bibliothèque com, vous recevez le premier élément de la collection, car ces valeurs d’argument sont forcées à 0 lorsque l’appel est effectué.

## <a name="using-idispatch"></a>Utilisation de IDispatch

Pour améliorer les performances, l’interface de programmation d’applications (API) COM de la plateforme Tablet PC ne prend pas en charge l’appel `IDispatchImpl::Invoke` avec une structure DISPPARAMS avec des arguments nommés. Le `IDispatchImpl::GetIDsOfNames` n’est pas non plus pris en charge. Au lieu de cela, appelez `Invoke` avec les DISPID fournis dans les en-têtes du kit de développement logiciel (SDK).

## <a name="waiting-for-events"></a>En attente d’événements

L’environnement Tablet PC est multithread. Reportez-vous à la documentation COM pour le Multi-Threading.

## <a name="support-for-aggregation"></a>Prise en charge de l’agrégation

L’agrégation a été testée uniquement pour le contrôle [InkEdit](inkedit-control-reference.md) , le contrôle [InkPicture](inkpicture-control-reference.md) , l’objet [**InkDisp**](inkdisp-class.md) et l’objet [**InkOverlay**](inkoverlay-class.md) . L’agrégation n’a pas été testée pour d’autres contrôles et objets de la bibliothèque.

## <a name="c"></a>C++

L’utilisation du kit de développement logiciel (SDK) Tablet PC en C++ requiert l’utilisation de certains concepts COM, tels que VARIANT, SAFEARRAY et BSTR. Cette section explique comment les utiliser.

### <a name="variant-and-safearray"></a>VARIANT et SAFEARRAY

La structure VARIANT est utilisée pour la communication entre les objets COM. Fondamentalement, la structure VARIANT est un conteneur pour une grande Union qui transporte de nombreux types de données.

La valeur du premier membre de la structure, VT, décrit les membres de l’Union qui sont valides. Lorsque vous recevez des informations dans une structure de variante, vérifiez le membre VT pour savoir quel membre contient des données valides. De même, lorsque vous envoyez des informations à l’aide d’une structure VARIANT, définissez toujours VT pour refléter le membre d’Union qui contient les informations.

Avant d’utiliser la structure, initialisez-la en appelant la fonction COM VariantInit. Lorsque vous avez terminé avec la structure, effacez-la avant de libérer la mémoire qui contient la variante en appelant VariantClear.

Pour plus d’informations sur la structure de la variante, consultez [types de données Variant et VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).

La structure SAFEARRAY est fournie comme un moyen de travailler en toute sécurité sur des tableaux dans COM. Le champ pArray de la variante est un pointeur vers un SAFEARRAY. Utilisez des fonctions telles que SafeArrayCreateVector, SafeArrayAccessData et SafeArrayUnaccessData pour créer et remplir un SAFEARRAY dans un VARIANT.

Pour plus d’informations sur le type de données SAFEARRAY, consultez [SAFEARRAY Data type](/windows/win32/api/oaidl/ns-oaidl-safearray).

Cet exemple C++ crée un [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) , `pInkStrokeDisp` , dans un objet [**InkDisp**](inkdisp-class.md) , `pInk` , à partir d’un tableau de données point.


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



### <a name="bstr"></a>BSTR

Le format de chaîne pris en charge pour COM est BSTR. Un BSTR a un pointeur vers une chaîne se terminant par zéro, mais il contient également la longueur de la chaîne (en octets, sans compter le terminateur), qui est stockée dans les 4 octets qui précèdent immédiatement le premier caractère de la chaîne.

Pour plus d’informations sur BSTR, consultez [type de données BSTR](/previous-versions/windows/desktop/automat/bstr).

Cet exemple C++ montre comment définir le Factoid sur un [**InkRecognizerContext**](inkrecognizercontext-class.md) à l’aide d’un BSTR.


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



 

 
