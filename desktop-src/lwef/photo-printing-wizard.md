---
title: Assistant impression de photos
description: L’Assistant impression de photos aide les utilisateurs à imprimer des photos en fournissant une interface d’assistant facile à utiliser.
ms.assetid: 9cc2c7d4-a2aa-4abc-9c63-b091e044804f
keywords:
- Assistant impression de photos
- IDropTarget, Assistant impression de photos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38199f7977e428f41cbc0560e0eab9ad2e106709579255ec8c3a1e74d7f7a402
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475444"
---
# <a name="photo-printing-wizard"></a>Assistant impression de photos

L’Assistant impression de photos aide les utilisateurs à imprimer des photos en fournissant une interface d’assistant facile à utiliser. L’Assistant permet à l’utilisateur de spécifier des tailles d’impression photo et d’autres options d’impression, puis envoie les photos à l’imprimante. L’Assistant est conçu afin de pouvoir être appelé par programme par une application qui souhaite offrir aux utilisateurs la possibilité d’imprimer des photos et de spécifier le dimensionnement et d’autres options d’impression. l’assistant impression de photos est disponible sur Windows XP et Windows Vista.

-   [Fonctionnalités fournies par l’Assistant impression de photos](#features-provided-by-the-photo-print-wizard)
-   [Formats de fichier photo pris en charge](#supported-photo-file-formats)
-   [Lancement de l’Assistant impression de photos par programmation](#programmatically-launching-the-photo-print-wizard)

## <a name="features-provided-by-the-photo-print-wizard"></a>Fonctionnalités fournies par l’Assistant impression de photos

L’Assistant impression de photos offre plusieurs options qui peuvent ne pas être disponibles dans les boîtes de dialogue d’imprimante courantes, telles que les modèles à plusieurs dispositions avec des dimensions précises. Les modèles de disposition permettent aux utilisateurs de tirer le meilleur parti de l’espace disponible sur le papier d’impression photographique. Les autres options qui peuvent être spécifiées ou accessibles via l’Assistant impression de photos sont les suivantes :

-   Sélection d’une imprimante dans une liste d’imprimantes disponibles ou de destinations d’impression virtuelles (par exemple, Microsoft XPS document Writer). sur Windows Vista, les options suivantes peuvent être disponibles, en fonction des fonctionnalités de l’imprimante ou de la destination d’impression virtuelle :
    -   Format du papier. Par exemple, « letter », « Legal », « a3 ».
    -   Qualité d’impression, en termes de résolutions de points par pouce (dpi) prises en charge.
    -   Type de papier. Par exemple, « plain » ou « brillante ».
-   Lancement des préférences et des propriétés d’impression pour une imprimante particulière.
-   définir les **Copies de chaque image** (sur Windows Vista) ou le **nombre d’utilisations de chaque image** (sur Windows XP) valeurs de la zone de sélection numérique.
-   Spécification d’un modèle de mise en page. Par exemple, les **photos en pleine page** ou les **tirages Wallet**.
-   sélection de l’option **adapter l’image au cadre** (disponible uniquement sur Windows Vista).
-   Aperçu de la photo imprimée avec les options actuellement spécifiées.
-   accès aux options d’impression avancées, telles que la **netteté pour l’impression** et la **gestion des couleurs** (disponible sur Windows Vista uniquement).

Toute application peut bénéficier de la fonctionnalité d’impression de photos et de fonctionnalités offerte par l’Assistant impression de photos. Une application peut transmettre les fichiers à imprimer. L’Assistant impression de photos prend alors soin de préparer le fichier pour l’impression en fonction des options spécifiées par l’utilisateur et envoie les fichiers préparés à l’imprimante.

l’illustration suivante montre l’interface de l’assistant impression de photos sur Windows Vista

![Assistant impression de photos sur Windows Vista](images/ppw-vista.png)

l’illustration suivante montre l’interface de l’assistant impression de photos sur Windows XP

![Assistant impression de photos sur Windows XP](images/ppw-xp.png)

## <a name="supported-photo-file-formats"></a>Formats de fichier photo pris en charge

sur Windows XP, l’assistant impression de photos prend en charge tous les formats de fichiers graphiques pris en charge par Windows GDI+. Actuellement, ces formats de fichier sont les suivants :

-   Bitmap (BMP)
-   format GIF (Graphics Interchange Format)
-   Joint Photographic Experts Group (JPEG)
-   Fichier image d’échange (EXIF)
-   format PNG (Portable Network Graphics)
-   format TIFF (Tagged Image File Format)

pour plus d’informations sur les formats de fichiers graphiques pris en charge par GDI+, consultez [Types de bitmaps](../gdiplus/-gdiplus-types-of-bitmaps-about.md).

sur Windows Vista, l’assistant impression de photos prend en charge tout format de fichier image pour lequel un codec WIC (Windows Imaging Component) est installé. WIC fournit plusieurs codecs standard, notamment :

-   Bitmap (BMP)
-   GIF
-   Format d’icône (ICO)
-   JPEG
-   PNG
-   TIFF
-   Windows Format de photo multimédia

pour plus d’informations sur les codecs wic et wic, consultez [Windows composant de création d’images](https://msdn.microsoft.com/library/ms737408(VS.85).aspx)

## <a name="programmatically-launching-the-photo-print-wizard"></a>Lancement de l’Assistant impression de photos par programmation

Pour appeler l’Assistant impression de photos, appelez l’interface [IDropTarget](/windows/win32/api/oleidl/nn-oleidl-idroptarget) avec l’identificateur de classe (CLSID) suivant :


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
```



Les fichiers à traiter par l’Assistant impression de photos sont spécifiés dans un objet [IDataObject](/windows/win32/api/objidl/nn-objidl-idataobject) .

L’exemple de code suivant montre comment appeler l’Assistant impression de photos.


```
static const CLSID CLSID_PrintPhotosDropTarget = 
  {0x60fd46de, 0xf830, 0x4894, {0xa6, 0x28, 0x6f, 0xa8, 0x1b, 0xc0, 0x19, 0x0d}};
            
// A data object that contains the list of photos to print.
IDataObject* pDataObject;

// Create the Photo Printing Wizard drop target.
CComPtr<IDropTarget> spDropTarget;
        
hr = CoCreateInstance(CLSID_PrintPhotosDropTarget,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_PPV_ARGS(&spDropTarget));

// Drop the data object onto the drop target.
POINTL pt = {0};
DWORD dwEffect = DROPEFFECT_LINK | DROPEFFECT_MOVE | DROPEFFECT_COPY;

spDropTarget->DragEnter(pDataObject, MK_LBUTTON, pt, &dwEffect);

spDropTarget->Drop(pDataObject, MK_LBUTTON, pt, &dwEffect);}
```



 

 