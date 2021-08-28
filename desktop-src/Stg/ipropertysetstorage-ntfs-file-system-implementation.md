---
title: IPropertySetStorage-implémentation du système de fichiers NTFS
description: La version NTFS 5,0 fournit une implémentation de IPropertySetStorage pour les fichiers sur un volume NTFS lorsque les fichiers eux-mêmes ne sont pas des fichiers composés.
ms.assetid: cd7290bb-bb4e-4dea-9bf6-2e1fdd0ebae8
keywords:
- IPropertySetStorage Strctd STG, implémentations, système de fichiers NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0794e2905cd9e8bd06804decb756b3f1f639c75e837b2d5f3181bb73939717f4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683039"
---
# <a name="ipropertysetstorage-ntfs-file-system-implementation"></a>IPropertySetStorage-implémentation du système de fichiers NTFS

La version NTFS 5,0 fournit une implémentation de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour les fichiers sur un volume NTFS lorsque les fichiers eux-mêmes ne sont pas des fichiers composés. L’implémentation de NTFS équivaut à l' [implémentation de fichier composé](ipropertysetstorage-compound-file-implementation.md). Pour plus d’informations sur les exceptions, consultez la section Notes.

**Pour obtenir un pointeur vers l’implémentation NTFS de IPropertySetStorage**

1.  Appelez [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) et spécifiez le **\_ fichier STGFMT** dans le paramètre *grfFlags* pour créer un nouveau fichier.
2.  Appelez [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) et spécifiez le **\_ fichier STGFMT** ou **STGFMT \_ toute** valeur d’énumération dans le paramètre *grfFlags* pour ouvrir un fichier existant.

Toutefois, vous ne pouvez pas obtenir l’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour un fichier composé. Lors de l’ouverture d’un fichier composé avec [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage), la spécification de la valeur d’énumération du **\_ fichier STGFMT** génère une erreur.

En outre, les jeux de propriétés simples ne peuvent pas être traités. Autrement dit, vous ne pouvez pas spécifier **STGM \_ traité** dans le paramètre *grfMode* des méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , sauf si vous spécifiez également **PROPSETFLAG \_ unsimple** dans le paramètre *grfFlags* . L’objet de stockage du jeu de propriétés ne prend pas en charge le traitement des transactions.

## <a name="when-to-use"></a>Quand l’utiliser

Appelez les méthodes [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour créer, ouvrir ou supprimer des jeux de propriétés dans le stockage de jeux de propriétés NTFS actuel. Il existe également une méthode, [**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum), qui fournit un pointeur vers un énumérateur qui peut être utilisé pour énumérer les jeux de propriétés dans le stockage.

## <a name="compatibility"></a>Compatibilité

les implémentations NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sont disponibles à partir de Windows 2000. Les versions antérieures ne peuvent pas accéder à ces jeux de propriétés.

L’implémentation NTFS stocke les jeux de propriétés dans les autres flux d’un fichier NTFS. Les flux de remplacement doivent être copiés lorsque le fichier principal est copié.

> [!Caution]  
> Tous les systèmes de fichiers ne prennent pas en charge ces flux. Si un fichier NTFS avec des jeux de propriétés est copié sur un volume FAT, seules les données du fichier sont copiées ; le jeu de propriétés est perdu. Dans ce cas, la fonction [**CopyFile**](/windows/desktop/api/winbase/nf-winbase-copyfile) ne retourne pas d’erreur.

 

> [!Caution]  
> si l’ordinateur qui effectue la copie de fichiers n’est pas un ordinateur qui s’exécute sur Windows 2000 ou une version ultérieure, les jeux de propriétés peuvent être perdus. par exemple, si un ordinateur exécutant le système d’exploitation Windows 95 copie un fichier ntfs, le jeu de propriétés est perdu même si le fichier de destination se trouve également sur un volume ntfs.

 

## <a name="methods"></a>Méthodes

L’implémentation du système de fichiers NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) prend en charge les méthodes suivantes.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crée un nouveau jeu de propriétés dans le stockage de fichiers NTFS actuel et fournit un pointeur d’interface vers l’implémentation de fichier NTFS [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) . Le mode de partage spécifié dans le paramètre *grfMode* doit être **STGM \_ share \_ exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Ouvre un jeu de propriétés existant dans le stockage de propriétés actuel. Au retour, elle fournit un pointeur d’interface vers l’implémentation de fichier NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage). Le mode de partage spécifié dans le paramètre *grfMode* doit être **STGM \_ share \_ exclusive**.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage ::D supprim**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Supprime un jeu de propriétés dans le stockage de propriétés actuel.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crée un objet utilisé pour énumérer les structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Chaque structure **STATPROPSETSTG** fournit des données relatives à un jeu de propriétés unique.

</dd> </dl>

## <a name="remarks"></a>Remarques

Les implémentations NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) et [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) stockent des jeux de propriétés dans un fichier sans affecter le contenu de ce fichier. Par exemple, si vous créez un jeu de propriétés dans un fichier HTML nommé Default.htm, ce fichier s’affiche toujours correctement dans un navigateur Web. Autrement dit, les modifications apportées à un fichier à l’aide de ces deux interfaces ne sont pas détectables lors de l’accès à un fichier avec la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

L’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) fournit une implémentation sécurisée lorsqu’elle est utilisée pour écrire des jeux de propriétés dans un fichier sur un volume NTFS version 5,0. Ces jeux de propriétés ne peuvent pas être endommagés par l’implémentation même en cas de défaillance du système. Par exemple, si la puissance d’un système échoue pendant un appel à [**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) alors que le jeu de propriétés est vidé sur le disque, le jeu de propriétés n’est jamais laissé dans un état intermédiaire. Soit la version précédente du jeu de propriétés est conservée, soit toutes les mises à jour sont enregistrées.

L’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) diffère de l’implémentation de fichier composé des manières suivantes :

-   Une structure [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) obtenue à partir de l’interface [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) contient un membre **CLSID** dont la valeur est toujours égale à zéro (**CLSID \_ null**). avec l’implémentation de fichier composé, le membre **clsid** correct est retourné pour les jeux de propriétés non simples (voir les [objets Stockage et de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md)).
-   Lors de l’obtention d’une implémentation NTFS du pointeur d’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) à l’aide de la fonction [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , le paramètre *grfMode* doit suivre les mêmes règles que pour l’implémentation de fichier composé.

    En outre, les indicateurs suivants ne peuvent pas être utilisés :

    **STGM \_ SIMPLE**, **STGM \_ traité**, **STGM \_ Convert**, **STGM \_ Priority** et **STGM \_ DELETEONRELEASE**.

-   Lorsqu’une interface [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS est obtenue par les fonctions [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , les modes de partage s’appliquent principalement à d’autres instances de cette interface, et non à des instances de l’ouverture du fichier lui-même. Par exemple, si une interface **IPROPERTYSETSTORAGE** NTFS est ouverte en appelant la fonction **StgOpenStorageEx** , avec le paramètre *grfMode* défini sur **STGM \_ ReadWrite \| STGM \_ share \_ exclusive**, il est possible d’ouvrir le fichier avec la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) .

    Ces instances simultanées d’ouverture de cette interface sont soumises aux contraintes suivantes : le paramètre *dwShareMode* dans la fonction [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) doit spécifier l’indicateur de **lecture de \_ partage \_ de fichiers** , et le paramètre *dwAccess* ne doit pas spécifier l’indicateur **Delete** . En outre, les fonctions [**DeleteFile**](/windows/desktop/api/fileapi/nf-fileapi-deletefilea) et [**MoveFile**](/windows/desktop/api/winbase/nf-winbase-movefile) ne doivent pas être appelées sur un fichier pour lequel ces interfaces de jeu de propriétés sont ouvertes, car ces fonctions requièrent l’accès en **suppression** au fichier.

-   Si une méthode [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS est ouverte en lecture seule et si le fichier n’a actuellement aucun jeu de propriétés, l’objet retourné ne contient pas réellement l’ouverture du fichier. Par conséquent, d’autres ouvertures de ce fichier échouent, même si le mode de partage de l’opération d’ouverture d’origine le rejette.

    Tels Si un [**IPROPERTYSETSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) NTFS est ouvert en mode **STGM \_ Read \| STGM \_ share \_ exclusive** et que le fichier n’a pas de jeu de propriétés, il est possible d’ouvrir simultanément le fichier **STGM \_ ReadWrite \| STGM \_ share \_ exclusive**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IPropertyStorage-implémentation du système de fichiers NTFS](ipropertystorage-ntfs-file-system-implementation.md)
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

 

 