---
title: Implémentation de fichiers IStorage-Compound
description: L’implémentation de fichier composé de IStorage vous permet de créer et de gérer des sous-stockages et des flux dans un objet de stockage résidant dans un objet de fichier composé.
ms.assetid: 2a2253f6-d3d3-403e-a9ba-53a541c7a31e
keywords:
- IStorage Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bf37b24a7c68bbe357d99f94e666bfcb613c472
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511496"
---
# <a name="istorage-compound-file-implementation"></a>Implémentation de fichiers IStorage-Compound

L’implémentation de fichier composé de [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) vous permet de créer et de gérer des sous-stockages et des flux dans un objet de stockage résidant dans un objet de fichier composé. Pour créer un objet de fichier composé et obtenir un pointeur **IStorage** , appelez la fonction d’API [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex). Pour ouvrir un objet de fichier composé existant et récupérer son pointeur **IStorage** racine, appelez [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex).

Les applications qui utilisent le stockage composite doivent être inscrites dans \_ \_ la racine SystemFileAssociations de classes HKEY \\ et doivent fournir leurs propres gestionnaires de propriétés. Pour plus d’informations, consultez la section « inscription de verbes et d’autres informations d’association de fichiers » de l' [inscription d’application](/windows/desktop/shell/app-registration).

## <a name="when-to-use"></a>Quand l’utiliser

La plupart des applications utilisent cette implémentation pour créer et gérer des flux de stockage et des flux.

## <a name="methods"></a>Méthodes

<dl> <dt>

<span id="IStorage__CreateStream"></span><span id="istorage__createstream"></span><span id="ISTORAGE__CREATESTREAM"></span>[**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream)
</dt> <dd>

Crée et ouvre un objet de flux avec le nom spécifié contenu dans cet objet de stockage. Le nom ne doit pas dépasser 31 caractères (à l’exclusion de la marque de fin de chaîne). Les caractères 000 à 01f qui servent de premier caractère au nom de flux/de stockage, sont réservés pour être utilisés par OLE. Il s'agit d'une restriction de fichier composé, pas d'une restriction de stockage de mémoire. L’implémentation de fichier composé COM de la méthode [**IStorage :: CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ne prend pas en charge les comportements suivants :

-   L' \_ indicateur STGM DELETEONRELEASE n’est pas pris en charge.
-   Le mode traité (STGM \_ traité) n’est pas pris en charge pour les objets de flux.
-   L’ouverture du même flux plusieurs fois à partir du même stockage n’est pas prise en charge. L’indicateur de mode de partage exclusif du partage STGM \_ \_ doit être spécifié dans le paramètre *grfMode* .

</dd> <dt>

<span id="IStorage__OpenStream"></span><span id="istorage__openstream"></span><span id="ISTORAGE__OPENSTREAM"></span>[**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)
</dt> <dd>

Ouvre un objet de flux existant dans cet objet de stockage à l’aide des modes d’accès spécifiés dans le paramètre *grfMode* . Les caractères 000 à 01f qui servent de premier caractère au nom de flux/de stockage, sont réservés pour être utilisés par OLE. Il s'agit d'une restriction de fichier composé, pas d'une restriction de stockage de mémoire. L’implémentation de fichier composé COM de la méthode [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ne prend pas en charge le comportement suivant :

-   Indicateur STGM \_ DELETEONRELEASE.
-   Mode traité (STGM \_ traité) pour les objets de flux.
-   Ouverture du même flux plusieurs fois à partir du même stockage. L' \_ indicateur STGM share \_ exclusive doit être spécifié.

</dd> <dt>

<span id="IStorage__CreateStorage"></span><span id="istorage__createstorage"></span><span id="ISTORAGE__CREATESTORAGE"></span>[**IStorage :: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage)
</dt> <dd>

Crée et ouvre un nouvel objet de stockage avec le nom spécifié dans le mode d’accès spécifié. Le nom ne doit pas dépasser 31 caractères (à l’exclusion de la marque de fin de chaîne). Les caractères 000 à 01f qui servent de premier caractère au nom de flux/de stockage, sont réservés pour être utilisés par OLE. Il s'agit d'une restriction de fichier composé, pas d'une restriction de stockage de mémoire. L’implémentation de fichier composé COM de la méthode [**IStorage :: CreateStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstorage) ne prend pas en charge le comportement suivant :

-   \_Indicateur de priorité STGM pour les stockages sans racine.
-   Ouverture d’un même objet de stockage plusieurs fois à partir du même stockage parent. L' \_ indicateur STGM share \_ exclusive doit être spécifié.
-   Indicateur STGM \_ DELETEONRELEASE. Si cet indicateur est spécifié, la fonction retourne STG \_ E \_ INVALIDFLAG.

</dd> <dt>

<span id="IStorage__OpenStorage"></span><span id="istorage__openstorage"></span><span id="ISTORAGE__OPENSTORAGE"></span>[**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage)
</dt> <dd>

Ouvre un objet de stockage existant avec le nom spécifié dans le mode d’accès spécifié. Les caractères 000 à 01f qui servent de premier caractère au nom de flux/de stockage, sont réservés pour être utilisés par OLE. Il s'agit d'une restriction de fichier composé, pas d'une restriction de stockage de mémoire. L’implémentation de fichier composé COM de la méthode [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) ne prend pas en charge le comportement suivant :

-   \_Indicateur de priorité STGM pour les stockages sans racine.
-   Ouverture d’un même objet de stockage plusieurs fois à partir du même stockage parent. L' \_ indicateur STGM share \_ exclusive doit être spécifié.
-   Indicateur STGM \_ DELETEONRELEASE. Si cet indicateur est spécifié, la fonction retourne STG \_ E \_ INVALIDFUNCTION.

</dd> <dt>

<span id="IStorage__CopyTo"></span><span id="istorage__copyto"></span><span id="ISTORAGE__COPYTO"></span>[**IStorage :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)
</dt> <dd>

Copie uniquement les sous-stockages et les flux de cet objet de stockage ouvert dans un autre objet de stockage. Le paramètre *rgiidExclude* peut être défini sur IID \_ IStream pour copier uniquement les sous-stockages ou sur IID \_ IStorage pour copier uniquement les flux.

</dd> <dt>

<span id="IStorage__MoveElementTo"></span><span id="istorage__moveelementto"></span><span id="ISTORAGE__MOVEELEMENTTO"></span>[**IStorage :: MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)
</dt> <dd>

Copie ou déplace un sous-stockage ou un flux de cet objet de stockage vers un autre objet de stockage.

</dd> <dt>

<span id="IStorage__Commit"></span><span id="istorage__commit"></span><span id="ISTORAGE__COMMIT"></span>[**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)
</dt> <dd>

Garantit que toutes les modifications apportées à un objet de stockage ouvert en mode transactionnel sont reflétées dans le stockage parent. pour un stockage racine, reflète les modifications apportées à l’appareil réel. par exemple, un fichier sur le disque. Pour un objet de stockage racine ouvert en mode direct, cette méthode n’a aucun effet, sauf pour vider toutes les mémoires tampons de mémoire sur le disque. Pour les objets de stockage non racine en mode direct, cette méthode n’a aucun effet.

L’implémentation de fichiers composés fournis par COM utilise un processus de validation en deux phases, sauf si \_ le remplacement de STGC est spécifié dans le paramètre *grfCommitFlags* . Ce processus en deux phases garantit la robustesse des données, en cas d’échec de l’opération de validation. Tout d’abord, toutes les nouvelles données sont écrites dans un espace inutilisé dans le fichier sous-jacent. Si nécessaire, un nouvel espace est alloué au fichier. Une fois cette étape terminée, une table dans le fichier est mise à jour à l’aide d’une opération d’écriture sur un seul secteur pour indiquer que les nouvelles données doivent être utilisées à la place de l’ancienne. Les anciennes données deviennent de l’espace libre à utiliser lors de la prochaine opération de validation. Ainsi, les anciennes données sont disponibles et peuvent être restaurées si une erreur se produit lors de la validation des modifications. Si \_ le remplacement de STGC est spécifié, une opération de validation à phase unique est utilisée. Pour plus d’informations sur les indicateurs de mode transactionnel, consultez énumération [**STGC**](/windows/win32/api/wtypes/ne-wtypes-stgc) .

</dd> <dt>

<span id="IStorage__Revert"></span><span id="istorage__revert"></span><span id="ISTORAGE__REVERT"></span>[**IStorage :: Revert**](/windows/desktop/api/Objidl/nf-objidl-istorage-revert)
</dt> <dd>

Ignore toutes les modifications apportées à l’objet de stockage depuis la dernière opération de validation.

</dd> <dt>

<span id="IStorage__EnumElements"></span><span id="istorage__enumelements"></span><span id="ISTORAGE__ENUMELEMENTS"></span>[**IStorage :: EnumElements**](/windows/desktop/api/Objidl/nf-objidl-istorage-enumelements)
</dt> <dd>

Crée et récupère un pointeur vers un objet énumérateur qui peut être utilisé pour énumérer le stockage et les objets de flux contenus dans cet objet de stockage. L’implémentation du fichier composé fourni par COM prend un instantané de ces informations. Par conséquent, les modifications apportées aux flux et aux stockages ne sont pas reflétées dans l’énumérateur jusqu’à ce qu’un nouvel énumérateur soit obtenu.

</dd> <dt>

<span id="IStorage__DestroyElement"></span><span id="istorage__destroyelement"></span><span id="ISTORAGE__DESTROYELEMENT"></span>[**IStorage ::D estroyElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-destroyelement)
</dt> <dd>

Supprime l’élément spécifié (sous-stockage ou flux) de cet objet de stockage.

</dd> <dt>

<span id="IStorage__RenameElement"></span><span id="istorage__renameelement"></span><span id="ISTORAGE__RENAMEELEMENT"></span>[**IStorage :: RenameElement**](/windows/desktop/api/Objidl/nf-objidl-istorage-renameelement)
</dt> <dd>

Renomme le sous-stockage ou le flux spécifié dans cet objet de stockage. Les caractères 000 à 01f qui servent de premier caractère au nom de flux/de stockage, sont réservés pour être utilisés par OLE. Il s'agit d'une restriction de fichier composé, pas d'une restriction de stockage de mémoire.

</dd> <dt>

<span id="IStorage__SetElementTimes"></span><span id="istorage__setelementtimes"></span><span id="ISTORAGE__SETELEMENTTIMES"></span>[**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dd>

Définit les heures de modification, d’accès et de création de l’élément de stockage spécifié. L’implémentation de fichier composé COM assure la modification et l’heure de modification des objets de stockage internes. Les objets de stockage racine prennent en charge tout ce qui est pris en charge par le système de fichiers sous-jacent (ou par [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)). L’implémentation de fichier composé ne conserve aucun horodatage pour les flux internes. Les horodatages non pris en charge sont signalés comme zéro, ce qui permet à l’appelant de tester la prise en charge.

</dd> <dt>

<span id="IStorage__SetClass"></span><span id="istorage__setclass"></span><span id="ISTORAGE__SETCLASS"></span>[**IStorage :: SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)
</dt> <dd>

Affecte le CLSID spécifié à cet objet de stockage.

</dd> <dt>

<span id="IStorage__SetStateBits"></span><span id="istorage__setstatebits"></span><span id="ISTORAGE__SETSTATEBITS"></span>[**IStorage :: SetStateBits**](/windows/desktop/api/Objidl/nf-objidl-istorage-setstatebits)
</dt> <dd>

Stocke jusqu’à 32 bits d’informations d’État dans cet objet de stockage. L’état défini par cette méthode est destiné à un usage externe uniquement. L’implémentation du fichier composé fourni par COM n’effectue aucune action en fonction de l’État.

</dd> <dt>

<span id="IStorage__Stat"></span><span id="istorage__stat"></span><span id="ISTORAGE__STAT"></span>[**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat)
</dt> <dd>

Récupère la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) pour cet objet de stockage ouvert.

</dd> </dl>

## <a name="remarks"></a>Notes

Si l’objet de stockage est ouvert en mode simple, l’utilisation des méthodes ci-dessus est limitée. Un stockage est en mode simple s’il est ouvert à l’aide de l' \_ élément simple STGM spécifié dans le paramètre *grfMode* de la fonction [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Pour plus d’informations sur les stockages en mode simple, consultez [**constantes STGM**](stgm-constants.md). Si l’objet de stockage en mode simple a été obtenu à partir de la fonction **StgCreateStorageEx** , la méthode [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) peut être appelée, mais la méthode [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ne peut pas. Si l’objet de stockage en mode simple a été obtenu à partir de la fonction **StgOpenStorageEx** , la méthode **OpenStream** peut être appelée, mais la méthode **CreateStream,** ne peut pas.

Lorsqu’un objet de stockage en mode simple est utilisé pour créer un flux, la taille minimale de ce flux est généralement de 4096 octets. Si moins de données sont écrites dans le flux, la taille est arrondie à 4096 octets.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Limites d’implémentation des fichiers composés](structured-storage-interfaces.md)
</dt> <dt>

[**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes)
</dt> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IRootStorage**](/windows/desktop/api/Objidl/nn-objidl-irootstorage)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> <dt>

[**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex)
</dt> </dl>

 

 