---
description: OpenXPS est le format Open XML Paper Specification pour les documents, et il est basé sur la spécification standard ECMA (European cartons Association).
ms.assetid: 52FB5B3F-BEBF-4851-8BE9-5DC7AE535313
title: Prise en charge des applications pour l’impression OpenXPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 914d8c365209ea3486bedd5e0352e63a8e31086f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518226"
---
# <a name="app-support-for-openxps-printing"></a>Prise en charge des applications pour l’impression OpenXPS

OpenXPS est le format Open XML Paper Specification pour les documents, qui est basé sur la spécification standard ECMA (European Computer Manufacturers Association).

Windows 8 prend entièrement en charge l’impression OpenXPS via le modèle de pilote d’imprimante v4, côte à côte avec la prise en charge continue du format Microsoft XPS. Et cette rubrique se concentre sur la partie de cette prise en charge qui s’applique aux développeurs d’applications Windows. Pour plus d’informations sur la configuration requise du pilote pour la prise en charge de OpenXPS, consultez [prise en charge des pilotes pour OpenXPS](/windows-hardware/drivers/print/printer-driver-overview).

## <a name="sending-xps-data-to-the-print-system"></a>Envoi de données XPS au système d’impression

Nous vous recommandons d’utiliser [**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget) pour l’envoi de tous les travaux d’impression XPS au système d’impression. **IPrintDocumentPackageTarget** accepte le modèle d’objet XPS (OM) sans sérialisation et permet d’améliorer les performances globales.

Voici un bref résumé de l’interface **IPrintDocumentPackageTarget** :

-   Cette interface prend en charge l’impression à partir de solutions personnalisées, ainsi que d’applications de bureau.

-   Pour les applications de bureau, cette fonctionnalité peut être utilisée à la place de [**StartXpsPrintJob1**](/windows/win32/api/xpsprint/nf-xpsprint-startxpsprintjob1).

-   Disponible sur Windows 7 avec Service Pack 1 (SP1) + mise à jour de la plateforme et Windows 8.

-   Incluez *DocumentTarget. h* dans les projets pour utiliser ces API.

Les applications qui utilisent des documents OpenXPS doivent noter que le type MIME pour OpenXPS est le suivant :

<dl> oxps de l’application \\  
</dl>

## <a name="sending-openxps-data-to-the-xps-print-api"></a>Envoi de données OpenXPS à l’API d’impression XPS

Spécifique à OpenXPS, XPS OM accepte à la fois MSXPS et OpenXPS, et fournit des méthodes pour la conversion et la sérialisation dans l’un ou l’autre format. Cela permet aux développeurs d’applications d’être agnostiques du pilote cible, s’ils le souhaitent. Cela signifie également que les développeurs d’applications peuvent toujours envoyer des travaux d’impression en tant que modèle OM XPS à StartXpsPrintJob1 ou IDocumentPackageTarget, sachant que le système d’impression gère toutes les conversions nécessaires.

Bien entendu, la prévention de la conversion entre les formats XPS améliorera les performances de bout en bout. À partir de l’application, le développeur peut vérifier la clé de Registre suivante pour déterminer le format XPS préféré du pilote d’impression ciblé :

``` syntax
HKLM\SOFTWARE\Microsoft\Windows NT\CurrentVersion\Print\Printers\[PrintDriverName]\PrintDriverData\XpsFormat
```

Une fois le format XPS préféré déterminé, l’application peut fournir des objets OM XPS qui ne nécessitent pas de conversion. Une note particulière est l’utilisation de la photo HD dans MSXPS et JPEGXR dans OpenXPS. La conversion de JPEGXR en photo HD est relativement légère puisque la principale différence dans cette conversion est que la photo HD ignore 4 bits de contrôle requis par JPEGXR. Toutefois, la conversion de la photo HD en JPEGXR nécessite que la totalité de l’image soit à nouveau codée afin de générer les bits de contrôle requis. Ainsi, le fait de fournir des images JPEGXR pour les images haute résolution garantit la compatibilité avec OpenXPS et réduit le coût de conversion de l’image pour MSXPS.

L’en-tête *Xpsobjectmodel \_ 1. h* définit les API et les objets supplémentaires pour OpenXPS. L’interface IXpsOMObjectFactory1 fournit des méthodes supplémentaires pour la conversion d’images. Voici la syntaxe :


```C++
IXpsOMObjectFactory1->ConvertHDPhotoToJpegXR(IXpsOMImageResource *imageResource);

IXpsOMObjectFactory1->ConvertJpegXRToHDPhoto(IXpsOMImageResource *imageResource);
```



Windows 8 fournit les énumérations nouvelles et mises à jour suivantes.

Nouvelle énumération :

<dl>

[**\_type de document XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)  
</dl>

Énumération mise à jour

<dl>

[**\_type d’image XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)  
</dl>

Les nouvelles méthodes GetDocumentType, permettent à une application de déterminer le format de document XPS. Celles-ci sont disponibles dans [**IXpsOMObjectFactory1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsomobjectfactory1), [**IXpsOMPackage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompackage1)et [**IXpsOMPage1**](/windows/desktop/api/XpsObjectModel_1/nn-xpsobjectmodel_1-ixpsompage1). Voici une liste des méthodes.

<dl>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)  
[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)  
[**IXpsOMPackage1 :: GetDocumentType,**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)  
[**IXpsOMPage1 :: GetDocumentType,**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)  
</dl>

Windows 8 fournit les nouveaux codes d’erreur suivants pour la prise en charge de OpenXPS :

<dl> \_espace de \_ noms incompatible avec XPS E \_ . <dl> Cette erreur est retournée s’il existe un espace de noms incompatible.  
</dl> </dd> XPS\_E\_ABSOLUTE\_REFERENCE. <dl> Cette erreur est retournée si MSXPS utilise des URI absolus dans les références internes ou s’il tente d’utiliser des références internes pour sérialiser dans le flux. Cela est dû au fait que XPS OM génère des URI relatifs. Et bien que MSXPS prenne en charge les URI relatifs et absolus, OpenXPS requiert des URI relatifs.  
</dl> </dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge des pilotes pour OpenXPS](/windows-hardware/drivers/print/printer-driver-overview)
</dt> <dt>

[**IPrintDocumentPackageTarget**](/windows/win32/api/documenttarget/nn-documenttarget-iprintdocumentpackagetarget)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromFile**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromfile)
</dt> <dt>

[**IXpsOMObjectFactory1::GetDocumentTypeFromStream**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsomobjectfactory1-getdocumenttypefromstream)
</dt> <dt>

[**IXpsOMPackage1 :: GetDocumentType,**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompackage1-getdocumenttype)
</dt> <dt>

[**IXpsOMPage1 :: GetDocumentType,**](/windows/desktop/api/XpsObjectModel_1/nf-xpsobjectmodel_1-ixpsompage1-getdocumenttype)
</dt> <dt>

[**\_type de document XPS \_**](/windows/win32/api/xpsobjectmodel_1/ne-xpsobjectmodel_1-xps_document_type)
</dt> <dt>

[**\_type d’image XPS \_**](/windows/win32/api/xpsobjectmodel/ne-xpsobjectmodel-xps_image_type)
</dt> </dl>

 

 
