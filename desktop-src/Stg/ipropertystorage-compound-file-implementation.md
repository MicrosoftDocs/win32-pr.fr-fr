---
title: Implémentation de fichiers IPropertyStorage-Compound
description: L’implémentation COM de l’architecture de stockage structurée est appelée fichiers composés.
ms.assetid: c4b4f313-de58-44f2-8ce1-a07cc187d8ca
keywords:
- IPropertyStorage Strctd STG, implémentations, fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03d927b0145077f12e5ba508ca65554ca33633a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842422"
---
# <a name="ipropertystorage-compound-file-implementation"></a>Implémentation de fichiers IPropertyStorage-Compound

L’implémentation COM de l’architecture de stockage structurée est appelée [fichiers composés](istorage-compound-file-implementation.md). Les objets de stockage tels qu’ils sont implémentés dans les fichiers composés incluent une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l’interface qui gère un jeu de propriétés persistantes unique et [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), l’interface qui gère les groupes de jeux de propriétés persistantes. Pour plus d’informations sur l’interface **IPropertyStorage** , consultez [considérations relatives au stockage des propriétés](property-storage-considerations.md)et **IPropertyStorage** .

Pour obtenir un pointeur vers l’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), appelez [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) pour créer un objet de fichier composé ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) pour ouvrir un objet de fichier composé créé précédemment. Dans le cas de **StgCreateStorageEx**, le paramètre *stgfmt* doit être défini sur \_ stockage stgfmt. Dans le cas de **StgOpenStorageEx**, le paramètre *stgfmt* doit être défini sur \_ stockage stgfmt ou stgfmt \_ Any. Dans les deux cas, le paramètre *riid* doit avoir la valeur IID \_ IPropertySetStorage. Les deux fonctions fournissent un pointeur vers l’interface de l’objet [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) . En appelant la méthode [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de cette interface, vous obtiendrez un pointeur vers l’interface **IPropertyStorage** , que vous pouvez utiliser pour appeler l’une de ses méthodes.

Une autre façon d’obtenir un pointeur vers l’implémentation de fichier composé de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) consiste à appeler les fonctions [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) et [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) plus anciennes, ou à spécifier un paramètre *riid* d’IID \_ IStorage pour la fonction [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) . Dans les deux cas, un pointeur vers l’interface [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) de l’objet est retourné. Avec les jeux de propriétés persistants, appelez [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour l’interface **IPropertySetStorage** , en spécifiant le nom défini par l’en-tête pour l’IID (identificateur d’interface) IID \_ IPropertySetStorage.

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pour gérer les propriétés dans un même jeu de propriétés. Ses méthodes prennent en charge la lecture, l’écriture et la suppression des propriétés et des noms de chaînes facultatifs qui peuvent être associés à des identificateurs de propriété. Les autres méthodes prennent en charge la validation standard et les opérations de restauration de stockage. Il existe également une méthode qui vous permet de définir les heures associées au stockage des propriétés, et une autre qui autorise l’attribution d’un CLSID qui peut être utilisé pour associer un autre code, tel que le code de l’interface utilisateur, au jeu de propriétés. L’appel de la méthode [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fournit un pointeur vers l’implémentation de fichier composé de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), qui vous permet d’énumérer les propriétés dans le jeu.

> [!Note]  
> Si vous obtenez un pointeur vers [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) en appelant [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile), [**StgCreateStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatestorageex), [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) ou [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) sur un stockage de jeu de propriétés en mode simple, les méthodes **IPropertyStorage** adhèrent aux règles des flux en mode simple. Le stockage de jeu de propriétés est un mode simple s’il a été obtenu pour un fichier qui a été créé ou ouvert avec l' \_ indicateur simple STGM. Dans ce cas, il n’est pas toujours possible de rendre le flux sous-jacent plus grand et il n’est pas possible de remplacer des propriétés existantes par des propriétés plus grandes. Pour plus d’informations, consultez [IPropertySetStorage-composed file Implementation](ipropertysetstorage-compound-file-implementation.md).

 

## <a name="ipropertystorage-and-caching"></a>IPropertyStorage et mise en cache

L’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) met en cache les jeux de propriétés ouverts en mémoire afin d’améliorer les performances. Par conséquent, les modifications apportées à un jeu de propriétés ne sont pas écrites dans le fichier composé tant que les méthodes [**Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ou **Release** (dernière référence) ne sont pas appelées.

## <a name="simple-mode-property-sets"></a>Jeux de propriétés en mode simple

Un objet de stockage de propriétés est en mode simple s’il est créé à partir d’un objet de stockage de jeu de propriétés de mode simple. Par exemple, un objet de stockage de jeu de propriétés serait en mode simple s’il a été obtenu à partir de la fonction [**StgOpenStorageEx**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorageex) , avec l' \_ indicateur simple STGM défini dans le paramètre *grfMode* . Notez que « mode simple » n’est pas lié aux « jeux de propriétés simples ». Un jeu de propriétés est simple s’il est créé en appelant [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) avec l’indicateur PROPSETFLAG non \_ simple défini dans le paramètre *grfFlags* . Pour plus d’informations sur les jeux de propriétés simples et simples, consultez [stockage et objets de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md).

Lorsqu’un objet de stockage de propriété en mode simple est créé, il n’y a aucune restriction sur son utilisation. Lorsqu’un objet de stockage de propriétés en mode simple existant est ouvert, l’objet de flux sous-jacent qui stocke le jeu de propriétés ne peut pas être augmenté. Par conséquent, il n’est pas toujours possible de modifier un tel objet de stockage de propriétés si la modification requiert un flux de plus grande taille.

## <a name="property-set-formats"></a>Formats de jeu de propriétés

L’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les formats de sérialisation des jeux de propriétés version 0 et version 1. Le format version 1 est pris en charge sur les ordinateurs qui exécutent Windows 2000. Pour plus d’informations, consultez [sérialisation du jeu de propriétés](version-0-vs--version-1-property-set-serialization.md). Les jeux de propriétés sont créés au format version 0 et restent dans ce format, sauf si de nouvelles fonctionnalités sont demandées. Lorsque cela se produit, le format est mis à jour vers la version 1.

Par exemple, si un jeu de propriétés est créé avec l' \_ indicateur par défaut PROPSETFLAG, son format est version 0. Tant que les types de propriété conformes au format de version 0 sont écrits et lus à partir de ce jeu de propriétés, le jeu de propriétés reste au format de la version 0. Si un type de propriété de la version 1 est écrit dans le jeu de propriétés, le jeu de propriétés est automatiquement mis à jour vers la version 1. Par la suite, ce jeu de propriétés ne peut plus être lu par les implémentations qui reconnaissent uniquement la version 0.

## <a name="ipropertystorage-and-variant-types"></a>Types IPropertyStorage et variant

L’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ne prend pas en charge les types variant VT \_ Unknown ou VT \_ Dispatch dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Le tableau suivant répertorie les types variant pris en charge dans un SafeArray. autrement dit, ces valeurs peuvent être combinées avec \_ un tableau VT dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Types variant pris en charge dans SafeArray par implémentation de fichier composé de IPropertyStorage

VT \_ I1

\_UI1 VT

VT \_ I2

\_UI2 VT

VT \_

VT \_ UI4

VT \_ int

VT \_ uint

VT \_ R4

VT \_ R8

VT \_ ca

\_Date VT

VT \_ BSTR

VT \_ bool

\_valeur décimale VT

\_erreur VT

\_variante VT

 



 

Lorsque VT \_ Variant est combiné avec \_ un tableau VT, le SAFEARRAY lui-même contient des structures [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) . Toutefois, les types de ces éléments doivent être extraits de la liste précédente, ne peuvent pas être des \_ variantes VT et ne peuvent pas inclure les \_ indicateurs de vecteur VT, de \_ matrice VT ou VT \_ .

## <a name="ipropertystorage-methods"></a>Méthodes IPropertyStorage

L’implémentation de fichier composé de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les méthodes suivantes :

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lit les propriétés spécifiées dans le tableau *rgpspec* et fournit les valeurs de toutes les propriétés valides dans le tableau *rgvar* de PROPVARIANTs. Dans l’implémentation de fichier composé COM, les identificateurs de propriété dupliqués qui font référence à des types de flux ou de stockage entraînent plusieurs appels à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) et la réussite ou l’échec de **ReadMultiple** dépend de la capacité de l’implémentation de stockage sous-jacente à partager les opérations d’ouverture. Étant donné que dans un fichier composé \_ , le partage STGM \_ exclusif est forcé, le fait que plusieurs tentatives d’ouverture échouent. L’ouverture d’un même objet de stockage plusieurs fois à partir du même stockage parent n’est pas prise en charge. L' \_ indicateur STGM share \_ exclusive doit être spécifié.

En outre, pour garantir une opération thread-safe si la même propriété de flux ou de valeur de stockage est demandée plusieurs fois via le même pointeur [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) dans l’implémentation de fichier composé com, l’opération d’ouverture réussira ou échouera selon que la propriété est déjà ouverte et si le système de fichiers sous-jacent gère plusieurs ouvertures d’un flux ou d’un stockage. Ainsi, l’opération **ReadMultiple** sur une propriété de flux ou de valeur de stockage entraîne toujours un appel à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), qui passe l’accès (STGM ReadWrite, etc. \_ ) et les indicateurs de partage (STGM \_ share \_ exclusive, etc.) spécifiés lors de l’ouverture ou de la création du jeu de propriétés d’origine.

Si la méthode échoue, les valeurs écrites dans *rgvar* \[ \] ne sont pas définies. Si certaines propriétés de flux ou de stockage sont ouvertes avec succès mais qu’une erreur se produit avant la fin de l’exécution, celles-ci doivent être libérées avant le retour de la méthode.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Écrit les propriétés spécifiées dans le tableau *rgpspec* , en leur \[ \] assignant les balises et les valeurs [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) spécifiées dans *rgvar* \[ \] . Les valeurs **PROPVARIANT** spécifiées sont affectées aux propriétés qui existent déjà. Les propriétés qui n’existent pas sont créées.

</dd> <dt>

<span id="IPropertyStorage__DeleteMultiple"></span><span id="ipropertystorage__deletemultiple"></span><span id="IPROPERTYSTORAGE__DELETEMULTIPLE"></span>[**IPropertyStorage ::D eleteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletemultiple)
</dt> <dd>

Supprime les propriétés spécifiées dans *rgpspec* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__ReadPropertyNames"></span><span id="ipropertystorage__readpropertynames"></span><span id="IPROPERTYSTORAGE__READPROPERTYNAMES"></span>[**IPropertyStorage::ReadPropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readpropertynames)
</dt> <dd>

Lit les noms de chaîne existants associés aux ID de propriété spécifiés dans le tableau *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__WritePropertyNames"></span><span id="ipropertystorage__writepropertynames"></span><span id="IPROPERTYSTORAGE__WRITEPROPERTYNAMES"></span>[**IPropertyStorage::WritePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writepropertynames)
</dt> <dd>

Attribue des noms de chaîne spécifiés dans le tableau *rglpwstrName* aux ID de propriété spécifiés dans le tableau *rgpropid* .

</dd> <dt>

<span id="IPropertyStorage__DeletePropertyNames"></span><span id="ipropertystorage__deletepropertynames"></span><span id="IPROPERTYSTORAGE__DELETEPROPERTYNAMES"></span>[**IPropertyStorage ::D eletePropertyNames**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-deletepropertynames)
</dt> <dd>

Supprime les noms de propriété pour les propriétés spécifiées dans le tableau *rgpropid* \[ \] .

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Définit le **CLSID** du flux de jeu de propriétés. Dans l’implémentation de fichier composé, la définition du CLSID sur un jeu de propriétés non simple (un qui peut légalement contenir des propriétés de stockage ou de valeur de flux, comme décrit dans [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) définit également le CLSID sur le sous-stockage sous-jacent afin qu’il puisse être obtenu via un appel à [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Pour les jeux de propriétés simples et simples, vide l’image mémoire du jeu de propriétés sur le stockage sous-jacent. En outre, pour les jeux de propriétés de mode transactionnel non simple, cette méthode effectue une validation (comme dans [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit)) sur le stockage qui contient le jeu de propriétés.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage :: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Pour les jeux de propriétés qui ne sont pas simples, appelle la méthode [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) du stockage sous-jacent et ouvre à nouveau le flux de contenu. Pour les jeux de propriétés simples, cette interface retourne toujours S \_ OK. Les jeux de propriétés insimples sont ceux qui ont été créés à l’aide de l' \_ indicateur PROPSETFLAG unsimple dans la méthode [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) . Pour plus d’informations, consultez [stockage et objets de flux pour un jeu de propriétés](storage-vs--stream-for-a-property-set.md) .

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Construit une instance de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), dont les méthodes peuvent être appelées pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) qui fournissent des informations sur chacune des propriétés de l’ensemble. Cette implémentation crée un tableau dans lequel le jeu de propriétés entier est lu et qui peut être partagé quand **IEnumSTATPROPSTG :: Clone** est appelé. Les modifications apportées au jeu de propriétés ne sont pas reflétées dans une instance **IEnumSTATPROPSTG** ouverte. Pour voir ces modifications, une nouvelle instance de cet énumérateur doit être construite.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage :: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Remplit les membres d’une structure [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , qui contient les données relatives à la propriété définie dans son ensemble. Au retour, fournit un pointeur vers la structure. Pour les jeux de stockage qui ne sont pas simples, cette implémentation appelle [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) pour obtenir les heures du flux ou du stockage sous-jacent. Pour les jeux de stockage simples, aucune heure n’est conservée.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Pour les jeux de propriétés qui ne sont pas simples, définit les heures prises en charge par le stockage sous-jacent. L’implémentation du stockage de fichiers composés prend en charge les trois éléments suivants : modification, accès et création. Cette implémentation de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) appelle la méthode [**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) du stockage sous-jacent pour récupérer ces heures.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> </dl>

 

 