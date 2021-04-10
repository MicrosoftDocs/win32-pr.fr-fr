---
title: Implémentations de jeux de propriétés dans COM
description: Implémentations de jeux de propriétés dans COM
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- Stockage structuré Strctd STG, utilisation de, jeu de propriétés utilise dans COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941093"
---
# <a name="property-set-implementations-in-com"></a>Implémentations de jeux de propriétés dans COM

Bien que le potentiel d’utilisation des jeux de propriétés persistantes ne soit pas entièrement exploité, il existe actuellement deux utilisations principales :

-   Stockage d’informations de synthèse avec un objet tel qu’un document
-   Transfert de données de propriété entre des objets

Les jeux de propriétés COM ont été conçus pour stocker des données adaptées à la représentation sous la forme d’une collection de valeurs affinées de taille moyenne. Les jeux de données qui sont trop volumineux pour être réalisables doivent être décomposés en flux, stockages et/ou jeux de propriétés distincts. Le format de données du jeu de propriétés COM n’était pas destiné à fournir un substitut pour une base de données de nombreux objets minuscules.

COM fournit des implémentations des interfaces de jeu de propriétés pour différents objets, ainsi que trois fonctions d’assistance. La section suivante décrit certaines caractéristiques de performances de ces implémentations. Pour plus d’informations sur des interfaces spécifiques et sur la façon d’obtenir un pointeur vers ces interfaces, reportez-vous aux éléments suivants dans la section de référence COM :

-   [IPropertySetStorage : implémentation de fichier composé](ipropertysetstorage-compound-file-implementation.md)

    L’implémentation de fichier composé, qui fournit les interfaces [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) et [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) , fournit également les interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . En raison de l’implémentation d’un fichier composé de **IStorage**, l’interface **IPropertySetStorage** peut être obtenue en appelant [**IUnknown :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).

-   [IPropertySetStorage – implémentation du système de fichiers NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)

    Les interfaces [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) peuvent également être obtenues pour les fichiers NTFS qui ne sont pas des fichiers composés. Par conséquent, il est possible d’obtenir ces interfaces pour tous les fichiers sur un volume NTFS.

-   [IPropertySetStorage – implémentation autonome](ipropertysetstorage-stand-alone-implementation.md)

    Lorsque cette implémentation de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) est instanciée, elle reçoit un pointeur vers un objet qui prend en charge l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) . Il manipule ensuite les stockages de jeux de propriétés au sein de cet objet de stockage. Par conséquent, il est possible d’accéder et de manipuler les jeux de propriétés sur tout objet qui prend en charge.

-   [Considérations relatives à l’implémentation de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

    Il existe plusieurs problèmes à prendre en compte pour fournir une implémentation de l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . Pour plus d’informations sur ces *considérations d’implémentation* , consultez la section Référence com.

En outre, il existe quatre fonctions d’assistance, conçues pour faciliter la gestion des propriétés qui ont été lues à partir d’une propriété définie en mémoire (dans une structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) ) :

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

Les sections suivantes traitent des implémentations de jeux de propriétés dans COM plus en détail :

-   [Gestion des jeux de propriétés](managing-property-sets.md)
-   [Considérations relatives aux jeux de propriétés](property-set-considerations.md)
-   [Stockage des jeux de propriétés](storing-property-sets.md)
-   [Caractéristiques de performances](performance-characteristics.md)
-   [Implémentation du jeu de propriétés d’informations de résumé](implementing-the-summary-information-property-set.md)
-   [Considérations relatives à l’implémentation de IPropertySetStorage](ipropertysetstorage-implementation-considerations.md)

 

 