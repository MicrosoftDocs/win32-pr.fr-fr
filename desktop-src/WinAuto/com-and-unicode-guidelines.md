---
title: Directives COM et Unicode
description: Étant donné que Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), les développeurs ont besoin d’un niveau modéré de compréhension des interfaces et des objets COM, et doivent savoir comment effectuer des tâches de base (par exemple, initialiser la bibliothèque COM).
ms.assetid: ed4bbef9-676a-4f4e-926a-044f71399c56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 023b1d58a1a31997142097d02d8fc7d80881111e08f0020d967c1984d9946c57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133902"
---
# <a name="com-and-unicode-guidelines"></a>Directives COM et Unicode

Étant donné que Microsoft Active Accessibility est basé sur le modèle COM (Component Object Model), les développeurs ont besoin d’un niveau modéré de compréhension des interfaces et des objets COM, et doivent savoir comment effectuer des tâches de base (par exemple, initialiser la bibliothèque COM). Les développeurs de serveurs doivent comprendre comment concevoir des classes qui implémentent l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) et comment créer des objets accessibles.

Vous avez également besoin d’un niveau modéré de compréhension d’Unicode pour utiliser un grand nombre des fonctions Microsoft Active Accessibility qui retournent des chaînes.

Pour utiliser Microsoft Active Accessibility efficacement, vous devez comprendre les fonctions, structures, types de données et interfaces COM et Unicode suivants. Des informations limitées sur certains de ces éléments sont fournies dans cette documentation.

### <a name="functions"></a>Fonctions :

-   [**Échec**](/windows/desktop/api/ole2/nf-ole2-oleinitialize)
-   [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [ **CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)
-   [**IUnknown :: AddRef**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref) et [ **IUnknown :: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)
-   [**VariantInit**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit) et [ **VariantClear**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear)
-   [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) et [ **WideCharToMultiByte**](/windows/desktop/api/stringapiset/nf-stringapiset-widechartomultibyte)
-   [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring) et [ **SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)

### <a name="structures-and-data-types"></a>Structures et types de données :

-   [**DIFFÉRENT**](variant-structure.md)
-   [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes)
-   [**BSTR**](/previous-versions/windows/desktop/automat/bstr)

### <a name="com-interfaces"></a>Interfaces COM :

-   [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)
-   [**IDispatch**](idispatch-interface.md)
-   [**IEnumVARIANT**](/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant)

## <a name="in-this-section"></a>Dans cette section

-   [Structure de variante](variant-structure.md)
-   [Interface IDispatch](idispatch-interface.md)
-   [Conversion de chaînes Unicode et ANSI](converting-unicode-and-ansi-strings.md)

 

 