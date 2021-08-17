---
title: Implémentation de fichiers IPropertySetStorage-Compound
description: L’implémentation d’objet de stockage de fichiers composés COM comprend une implémentation de IPropertyStorage, l’interface qui gère un jeu de propriétés persistantes unique et IPropertySetStorage, l’interface qui gère les groupes de jeux de propriétés persistantes.
ms.assetid: de2cb778-c6eb-4487-996b-87405674f603
keywords:
- IPropertySetStorage Strctd STG, implémentations, fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec3bc0d423b304b6d456ccddab158a48ba0b6d5f3f310d293c6aed0dedb2a556
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662659"
---
# <a name="ipropertysetstorage-compound-file-implementation"></a>Implémentation de fichiers IPropertySetStorage-Compound

L' [implémentation d’objet de stockage de fichiers composés com](ipropertystorage-compound-file-implementation.md) comprend une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l’interface qui gère un jeu de propriétés persistantes unique et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l’interface qui gère les groupes de jeux de propriétés persistantes.

Pour obtenir un pointeur vers l’implémentation de fichier composé de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), spécifiez le nom défini par l’en-tête de l’ID d’IID \_ IStorage comme paramètre *riid* , ou utilisez les fonctions [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Dans les deux cas, spécifiez \_ le stockage STGFMT comme paramètre *STGFMT* . (STGFMT \_ TOUT peut également être spécifié dans le cas de **StgOpenStorageEx**.) Spécifiez également le nom défini d’en-tête pour l’IID (ID d’interface) \_ IPropertySetStorage IID comme paramètre *riid* . Les deux fonctions fournissent un pointeur vers l’interface de l’objet **IPropertySetStorage** .

Une autre façon d’obtenir un pointeur vers l’implémentation de fichier composé consiste à spécifier le nom défini d’en-tête pour l’IID d’identificateur \_ IStorage comme paramètre *riid* , ou à utiliser les fonctions [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) . Un pointeur vers l’interface de l’objet [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) est alors fourni. Lorsque vous souhaitez gérer les jeux de propriétés persistants, appelez [**IStorage :: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) .

## <a name="when-to-use-ipropertysetstorage"></a>Quand utiliser IPropertySetStorage

Appelez les méthodes de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour créer, ouvrir ou supprimer des jeux de propriétés dans le stockage de jeux de propriétés de fichier composé actuel. Il existe également une méthode, [**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), qui fournit un pointeur vers un énumérateur qui peut être utilisé pour énumérer les jeux de propriétés dans le stockage.

## <a name="methods"></a>Méthodes

[**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)

Crée un nouveau jeu de propriétés dans le stockage de fichiers composés actuel et fournit un pointeur d’interface vers l’implémentation de fichier composé [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Dans cette implémentation, les jeux de propriétés peuvent être traités uniquement si PROPSETFLAG non \_ simple est spécifié. Cette méthode exige que le mode de partage spécifié dans le paramètre *grfMode* soit STGM \_ share \_ exclusive, et que le mode d’accès soit STGM \_ Read ou STGM \_ ReadWrite (le mode d’écriture STGM \_ n’est pas pris en charge).

[**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)

Ouvre un jeu de propriétés existant dans le stockage de propriétés actuel. Au retour, elle fournit un pointeur d’interface vers l’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Cette méthode exige que le mode de partage spécifié dans le paramètre *grfMode* soit STGM \_ share \_ exclusive et que le mode d’accès soit STGM \_ Read ou STGM \_ ReadWrite (STGM \_ Write n’est pas pris en charge).

[**IPropertySetStorage ::D supprim**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)

Supprime un jeu de propriétés dans ce stockage de propriétés.

[**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)

Crée un objet utilisé pour énumérer les structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Chaque structure **STATPROPSETSTG** fournit des données relatives à un jeu de propriétés unique.

## <a name="remarks"></a>Remarques

à compter de Windows 2000, l’implémentation de fichier composé de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) prend en charge le mode simple. Le mode simple est indiqué en spécifiant l' \_ indicateur simple STGM pour les fonctions [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) et [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Si le fichier composé est ouvert en mode simple, l’implémentation de **IPropertySetStorage** associée est limitée comme suit :

-   Seuls les jeux de propriétés simples peuvent être créés. Autrement dit, la spécification de la \_ valeur non simple PROPSETFLAG dans le paramètre *grfFlags* de la méthode [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) génère une erreur.
-   Une fois que vous avez créé un fichier composé avec [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) à l’aide \_ de STGM simple et que vous interrogez l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , vous ne pouvez appeler [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) qu’une seule fois. Vous devez ensuite libérer l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) avant d’appeler à nouveau la méthode **Create** . Pour plus d’informations sur le mode simple, consultez [**constantes STGM**](stgm-constants.md).
-   Vous ne pouvez pas utiliser la méthode [**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) pour ouvrir une propriété définie après l’utilisation de [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) pour créer l’objet de stockage. Au lieu de cela, vous devez utiliser [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) avant d’interroger [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et d’appeler la méthode **Open** .
-   Après avoir ouvert un fichier composé avec [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) à l’aide de l' \_ indicateur simple STGM et de la requête de l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) , vous pouvez ouvrir une propriété définie à la fois à l’aide de [**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open). En outre, il n’est pas possible que la taille totale de la propriété définie soit augmentée alors que le jeu de propriétés est ouvert.

Les jeux de propriétés simples ne peuvent pas être traités. Vous ne pouvez pas spécifier STGM \_ avec transaction dans le paramètre *grfMode* des méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , sauf si vous spécifiez également PROPSETFLAG \_ unsimple dans le paramètre *grfFlags* . N’oubliez pas que les jeux de propriétés simples et non simples ne sont pas liés aux jeux de propriétés en mode simple décrits ci-dessus. pour plus d’informations sur les jeux de propriétés simples et simples, consultez [Stockage et objets de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md).

> [!Note]  
> Les jeux de propriétés DocumentSummaryInformation et UserDefined sont uniques en ce qu’ils peuvent avoir deux sections de jeu de propriétés. Pour plus d’informations, consultez [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md).

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IPropertyStorage-implémentation de fichier composé](ipropertystorage-compound-file-implementation.md)
</dt> <dt>

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage :: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dt>

[**Constantes PROPSETFLAG**](propsetflag-constants.md)
</dt> <dt>

[**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg)
</dt> </dl>

 

 