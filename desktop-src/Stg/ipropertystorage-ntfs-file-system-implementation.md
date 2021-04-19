---
title: IPropertyStorage-implémentation du système de fichiers NTFS
description: La version NTFS 5,0 fournit une implémentation de l’interface IPropertyStorage pour les fichiers sur un volume NTFS lorsque les fichiers ne sont pas des fichiers composés.
ms.assetid: d0ffd975-5bc2-4de3-b0c1-c9188541f46a
keywords:
- IPropertyStorage Strctd STG, implémentations, système de fichiers NTFS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca359bebbd05e67a034494023d7fc23089396b32
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106530792"
---
# <a name="ipropertystorage-ntfs-file-system-implementation"></a>IPropertyStorage-implémentation du système de fichiers NTFS

La version NTFS 5,0 fournit une implémentation de l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pour les fichiers sur un volume NTFS lorsque les fichiers ne sont pas des fichiers composés.

**Pour obtenir un pointeur vers l’implémentation du système de fichiers NTFS de IPropertySetStorage**

1.  Appelez [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) à l’aide de l’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).
2.  Appelez [**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) à l’aide de l’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage).

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pour gérer les propriétés dans un même jeu de propriétés. Ses méthodes prennent en charge la lecture, l’écriture et la suppression de propriétés, ainsi que les noms de chaînes facultatifs qui peuvent être associés à des identificateurs de propriété. Une autre méthode vous permet de définir les heures associées au stockage des propriétés, et une autre permet l’affectation d’un CLSID, utilisé pour associer un autre code, tel que le code de l’interface utilisateur, au jeu de propriétés. L’appel de la méthode [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fournit un pointeur vers l’implémentation NTFS de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), qui vous permet d’énumérer les propriétés du jeu.

## <a name="remarks"></a>Notes

L’implémentation NTFS fournit essentiellement les mêmes fonctionnalités que l’implémentation de fichiers composés. Pour plus d’informations, consultez [IPropertyStorage-composed file Implementation](ipropertystorage-compound-file-implementation.md).

Étant donné que NTFS est un système de fichiers robuste, un jeu de propriétés NTFS ne sera jamais dans un état incorrect. Lorsque le contenu d’un [**IPROPERTYSTORAGE**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) NTFS est vidé dans le fichier NTFS sous-jacent, tout ou partie de l’État est écrit dans le fichier sous la forme d’une opération atomique, même en cas d’échec au cours de l’opération, comme un arrêt anormal du processus. Pour obtenir un comportement similaire avec l’implémentation de fichier composé, l’interface [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) parente doit être ouverte en mode traité.

Ce niveau de robustesse est uniquement possible lors de l’accès à une propriété NTFS définie sur un volume NTFS 5,0. Il est possible d’accéder à des jeux de propriétés NTFS sur des versions antérieures de NTFS (par exemple, un ordinateur fonctionnant sous Windows NT ou Windows 2000 qui accède aux jeux de propriétés sur un serveur de fichiers qui s’exécute sur Windows NT 4,0), mais il n’est pas garanti qu’il se trouve dans un état correct en cas de défaillance inattendue.

Bien que l’implémentation NTFS de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ne prenne pas en charge la transaction, l’implémentation NTFS de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) la prend en charge. Autrement dit, **STGM \_ traitée** peut être spécifiée dans le paramètre *grfMode* aux méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de **IPropertySetStorage**. Comme dans l’implémentation de fichier composé, le mode transactionnel est possible uniquement pour les stockages de propriétés non simples (en spécifiant **PROPSETFLAG non \_ simple** dans le paramètre *grfFlags* ).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[IPropertySetStorage-implémentation du système de fichiers NTFS](ipropertysetstorage-ntfs-file-system-implementation.md)
</dt> </dl>

 

 