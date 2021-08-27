---
title: Assistant impression en ligne
description: l’assistant impression en ligne Windows Vista aide les utilisateurs à commander des photos des détaillants en ligne.
ms.assetid: 1e73a5d0-2ca8-4eca-846a-bd69eee257cb
keywords:
- Assistant impression en ligne
- icônes, Assistant impression en ligne
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc402f1fe5853c7a255ea45940d62efcd092c424be6905287315c5cfe5fc7504
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975915"
---
# <a name="online-printing-wizard"></a>Assistant impression en ligne

l’assistant impression en ligne Windows Vista aide les utilisateurs à commander des photos des détaillants en ligne. Cet Assistant est conçu afin de pouvoir être appelé par programme par toute application qui souhaite offrir aux utilisateurs la possibilité de commander des impressions de photos. l’assistant impression de photos est disponible sur Windows Vista. PIX pour Windows

-   [Fonctionnalités fournies par l’Assistant impression en ligne](#features-provided-by-the-online-print-wizard)
-   [Formats de fichier photo pris en charge](#supported-photo-file-formats)
-   [Lancement de l’Assistant impression en ligne par programmation](#programmatically-launching-the-online-print-wizard)
-   [Accès à l’icône de l’Assistant impression en ligne](#accessing-the-online-print-wizard-icon)
-   [Propriétés MRU de l’Assistant impression en ligne](#online-print-wizard-mru-properties)

## <a name="features-provided-by-the-online-print-wizard"></a>Fonctionnalités fournies par l’Assistant impression en ligne

l’assistant impression en ligne Windows Vista permet aux utilisateurs de commander des tirages à partir d’une sélection de détaillants en ligne participant à l’impression. Lorsqu’il est appelé, l’Assistant :

1.  Accepte un fichier ou une liste de fichiers pour lesquels des impressions doivent être classées.
2.  Récupère automatiquement la liste actuelle des revendeurs d’impression en ligne participante et permet à l’utilisateur de sélectionner le détaillant à partir duquel acheter les photos.
3.  Guide l’utilisateur tout au long du processus ou de l’ordre des impressions.

toute application peut tirer parti des fonctionnalités offertes par l’assistant impression en ligne Windows Vista. Une application n’a besoin que de transmettre le ou les fichiers pour lesquels les tirage sont triés, et l’Assistant guide l’utilisateur tout au long du processus de commande.

l’illustration suivante montre l’assistant impression en ligne Windows Vista affichant un exemple de liste des détaillants en ligne participant à l’impression.

![Assistant impression en ligne Windows Vista](images/opw.png)

## <a name="supported-photo-file-formats"></a>Formats de fichier photo pris en charge

l’assistant impression en ligne Windows Vista prend en charge tout format de fichier image pour lequel un codec WIC (Windows Imaging Component) est installé. WIC fournit plusieurs codecs standard, notamment :

-   Bitmap (BMP)
-   format GIF (Graphics Interchange Format)
-   Format d’icône (ICO)
-   Joint Photographic Experts Group (JPEG)
-   format PNG (Portable Network Graphics)
-   format TIFF (Tagged Image File Format)
-   Windows Format de photo multimédia

pour plus d’informations sur les codecs wic et wic, consultez [Windows composant de création d’images](https://msdn.microsoft.com/library/ms737408(VS.85).aspx).

Les formats de fichier pris en charge par les revendeurs d’impression en ligne varient d’un détaillant à l’autres. il est possible qu’un détaillant particulier ne prenne pas en charge tous les formats de fichier pris en charge par l’assistant impression Windows Vista Online. si l’utilisateur tente de commander des tirages dans un format qui n’est pas pris en charge par le détaillant sélectionné, l’assistant impression Windows Vista Online avertit l’utilisateur que le détaillant sélectionné ne prend pas en charge le format de fichier envoyé.

## <a name="programmatically-launching-the-online-print-wizard"></a>Lancement de l’Assistant impression en ligne par programmation

pour appeler l’assistant impression en ligne Windows Vista, appelez l’interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) avec l’identificateur de classe (CLSID) suivant :


```
CLSID_PublishDropTarget
```



Ce CLSID est défini dans ShObjIdl. h et ShObjIdl. idl. les fichiers à traiter par l’assistant impression Windows Vista Online sont spécifiés dans un objet [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

l’exemple de code suivant montre comment appeler l’assistant impression en ligne Windows Vista.


```
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PublishDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



## <a name="accessing-the-online-print-wizard-icon"></a>Accès à l’icône de l’Assistant impression en ligne

l’assistant impression en ligne Windows Vista exporte une icône accessible et affichée par les applications qui l’appellent. l’illustration suivante montre l’icône de l’assistant impression en ligne Windows Vista.

![icône de l’Assistant impression en ligne de Windows Vista](images/opw-icon.png)

l’exemple de code suivant montre comment récupérer l’index de l’icône de l’assistant impression Windows Vista Online en lisant la propriété **OPWIcon** .


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;

spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

// Read the icon index from the properties set. 
CComVariant vtIcon;
int nIndex;
hr = spPropsBag->Read(L"OPWIcon", &vtIcon, NULL);

if SUCCEEDED(hr)
{
    nIndex = vtIcon.lVal;
}
```



## <a name="online-print-wizard-mru-properties"></a>Propriétés MRU de l’Assistant impression en ligne

l’assistant impression en ligne Windows Vista définit trois propriétés qui sont liées au détaillant d’impression en ligne (MRU) le plus récemment utilisé.



| Nom de la propriété | Valeur/fonction de la propriété                                                                                                                                                                                                                                                   |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MRUIcon**   | L’index de l’icône du détaillant d’impression en ligne utilisé le plus récemment peut être lu à partir de cette propriété.                                                                                                                                                                 |
| **MRUName**   | Le nom du détaillant d’impression en ligne utilisé le plus récemment peut être lu à partir de cette propriété.                                                                                                                                                                               |
| **UseMRU**    | Valeur de **variante** **VT \_ booléenne** indiquant si l’Assistant doit ignorer la page de sélection du détaillant pour l’impression en ligne, et utiliser le plus récemment le détaillant d’impression en ligne utilisé à la place. Affectez à cette propriété la **\_ valeur variant true** pour ignorer la page de sélection du détaillant. |



 

l’exemple de code suivant montre comment définir la propriété UseMRU de sorte que l’assistant impression en ligne Windows Vista contourne la page de sélection du détaillant pour l’impression en ligne et sélectionne automatiquement le dernier détaillant utilisé.


```
// A data object that contains the list of photos to order prints for.
IDataObject* pDataObject;

// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Set the UserMRU property to true to skip retailer selection and use 
// the MRU retailer instead.    
CComQIPtr<IPropertyBag> spPropsBag(spDropTarget);
if(spPropsBag) 
{
    VARIANT varTrue = {0};
    varTrue.vt = VT_BOOL;
    varTrue.boolVal = VARIANT_TRUE;
    spPropsBag->Write(L"UseMRU", &varTrue);
}

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);
```



L’exemple de code suivant montre comment lire les propriétés MRUName et MRUIcon.


```
// Create the Online Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
HRESULT hr = CoCreateInstance(CLSID_PublishDropTarget,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&spDropTarget));

// Get the Online Printing Wizard properties.
CComPtr<IPropertyBag> spPropsBag;
spDropTarget->QueryInterface(IID_PPV_ARGS(&spPropsBag));

CComVariant vtMRUName, vtMRUIconIndex;
CComBSTR bstrMRUName;
int nMRUIconIndex;

// Get the MRU name value.
hr = spPropsBag->Read(L"MRUName", &vtMRUName, NULL);
if SUCCEEDED(hr) 
{
    bstrMRUName = vtMRUName.bstrVal;
}

// Get the MRU icon index value.
hr = spPropsBag->Read(L"MRUIcon", &vtMRUIconIndex, NULL);
if SUCCEEDED(hr)
{
    nMRUIconIndex = vtMRUIconIndex.lVal;
}
```



 

 