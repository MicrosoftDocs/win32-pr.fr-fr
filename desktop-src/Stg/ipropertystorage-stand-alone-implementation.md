---
title: IPropertyStorage-implémentation autonome
description: L’implémentation autonome fournie par le système de IPropertySetStorage comprend une implémentation de IPropertyStorage, l’interface qui lit et écrit des propriétés dans un stockage de jeu de propriétés.
ms.assetid: 8de32538-de11-4e4d-9269-145b2accb099
keywords:
- IPropertyStorage-implémentation autonome
- IPropertyStorage Strctd STG, implémentations, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 200d7f328670b8945807b7db7f742feabe58ad32847e3c56aa98a34278a71fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119662549"
---
# <a name="ipropertystorage-stand-alone-implementation"></a>IPropertyStorage-implémentation autonome

L’implémentation autonome fournie par le système de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) comprend une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), l’interface qui lit et écrit des propriétés dans un stockage de jeu de propriétés. L’interface **IPropertySetStorage** crée et ouvre les jeux de propriétés dans un stockage. Les interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) et [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sont également fournies dans l’implémentation autonome.

Pour obtenir un pointeur vers l’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage), appelez la fonction [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) pour créer un nouveau jeu de propriétés ou [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) pour obtenir le pointeur d’interface sur un jeu de propriétés existant (ou appelez les méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) ou [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) de l’implémentation autonome [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) ).

L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) crée des jeux de propriétés sur n’importe quel objet de stockage ou de flux, pas seulement sur des flux et des stockages de fichiers composés. L’implémentation autonome ne dépend pas de fichiers composés et peut être utilisée avec n’importe quelle implémentation de stockage structuré. Pour plus d’informations sur l’implémentation de fichier composé de cette interface, consultez [implémentation de fichiers composés IPropertyStorage](ipropertystorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Quand l’utiliser

Utilisez [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) pour gérer les propriétés dans un même jeu de propriétés. Ses méthodes prennent en charge la lecture, l’écriture et la suppression des propriétés et des noms de chaînes facultatifs qui peuvent être associés à des ID de propriété. Les autres méthodes prennent en charge la validation standard et les opérations de restauration de stockage. Il existe également une méthode qui définit les heures associées au stockage des propriétés, et une autre qui permet l’affectation d’un CLSID à utiliser pour associer un autre code, tel que le code de l’interface utilisateur, au jeu de propriétés. La méthode [**enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum) fournit un pointeur vers l’implémentation autonome de [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), qui énumère les propriétés du jeu.

## <a name="version-0-and-version-1-property-set-formats"></a>Formats de jeu de propriétés de la version 0 et de la version 1

L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les formats de sérialisation des jeux de propriétés version 0 et version 1. Pour plus d’informations, consultez [sérialisation du jeu de propriétés](version-0-vs--version-1-property-set-serialization.md). Les jeux de propriétés sont créés au format version 0 et restent dans ce format, sauf si de nouvelles fonctionnalités sont demandées. À ce moment-là, le format est mis à jour vers la version 1.

Par exemple, si un jeu de propriétés est créé avec l' \_ indicateur par défaut PROPSETFLAG, son format est version 0. Tant que les types de propriété conformes au format de version 0 sont écrits et lus à partir de ce jeu de propriétés, le jeu de propriétés reste au format de la version 0. Si un type de propriété de la version 1 est écrit dans le jeu de propriétés, le jeu de propriétés est automatiquement mis à jour vers la version 1. Par la suite, ce jeu de propriétés ne peut plus être lu par les implémentations qui comprennent uniquement la version 0.

## <a name="ipropertystorage-and-variant-types"></a>Types IPropertyStorage et variant

L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) ne prend pas en charge les types variant VT \_ Unknown ou VT \_ Dispatch dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Les types variant suivants sont pris en charge dans un SafeArray ; autrement dit, ces valeurs peuvent être combinées avec \_ un tableau VT dans le membre **VT** de la structure [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .



Types variant pris en charge dans SafeArray par implémentation de fichier composé de [ **IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)

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

L’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) prend en charge les méthodes suivantes :

<dl> <dt>

<span id="IPropertyStorage__ReadMultiple"></span><span id="ipropertystorage__readmultiple"></span><span id="IPROPERTYSTORAGE__READMULTIPLE"></span>[**IPropertyStorage::ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple)
</dt> <dd>

Lit les propriétés spécifiées dans le tableau *rgpspec* et fournit les valeurs de toutes les propriétés valides dans le tableau *rgvar* d’éléments [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) .

Dans l’implémentation fournie par le système, les identificateurs de propriété dupliqués qui font référence aux types de flux ou de stockage entraînent plusieurs appels à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage) et la réussite ou l’échec de [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) dépend de la capacité de l’implémentation de stockage sous-jacente à partager les stockages ouverts.

En outre, pour garantir une opération thread-safe si la même propriété de flux ou de valeur de stockage est demandée plusieurs fois via le même pointeur [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) , l’ouverture réussira ou échouera selon que la propriété est déjà ouverte et que le système de fichiers sous-jacent gère plusieurs ouvertures d’un flux ou d’un stockage. Ainsi, l’opération [**ReadMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-readmultiple) sur une propriété de flux ou de valeur de stockage entraîne toujours un appel à [**IStorage :: OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream)ou [**IStorage :: OpenStorage**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstorage), en passant l’accès (STGM \_ ReadWrite, par exemple) et les valeurs de partage (STGM \_ partage \_ exclusive, par exemple) spécifié lors de l’ouverture ou de la création initiale du jeu de propriétés.

Si la méthode échoue, les valeurs écrites dans *rgvar* \[ \] ne sont pas définies. Si certaines propriétés de flux ou de valeur de stockage sont ouvertes avec succès mais qu’une erreur se produit avant la fin de l’exécution, ces propriétés doivent être libérées avant le retour de la méthode.

</dd> <dt>

<span id="IPropertyStorage__WriteMultiple"></span><span id="ipropertystorage__writemultiple"></span><span id="IPROPERTYSTORAGE__WRITEMULTIPLE"></span>[**IPropertyStorage::WriteMultiple**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-writemultiple)
</dt> <dd>

Écrit les propriétés spécifiées dans le tableau *rgpspec* , en leur \[ \] assignant les balises et les valeurs [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) spécifiées dans *rgvar* \[ \] . Les valeurs **PROPVARIANT** spécifiées sont affectées aux propriétés qui existent déjà, et les propriétés qui n’existent pas actuellement sont créées.

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

Supprime les noms de chaîne des ID de propriété spécifiés dans le tableau *rgpropid* en écrivant la **valeur null** dans le nom de la propriété.

</dd> <dt>

<span id="IPropertyStorage__SetClass"></span><span id="ipropertystorage__setclass"></span><span id="IPROPERTYSTORAGE__SETCLASS"></span>[**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)
</dt> <dd>

Définit le **CLSID** du flux de jeu de propriétés. Dans l’implémentation autonome, la définition du CLSID sur un jeu de propriétés non simple (un qui peut contenir des propriétés de stockage ou de valeur de flux, comme décrit dans [**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)) définit également le CLSID sur le sous-stockage sous-jacent afin qu’il puisse être obtenu via un appel à [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat).

</dd> <dt>

<span id="IPropertyStorage__Commit"></span><span id="ipropertystorage__commit"></span><span id="IPROPERTYSTORAGE__COMMIT"></span>[**IPropertyStorage :: Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit)
</dt> <dd>

Pour les jeux de propriétés simples et simples, vide l’image mémoire sur le sous-système de disque. En outre, pour les jeux de propriétés de mode transactionnel non simple, cette méthode appelle [**IStorage :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) sur le jeu de propriétés.

</dd> <dt>

<span id="IPropertyStorage__Revert"></span><span id="ipropertystorage__revert"></span><span id="IPROPERTYSTORAGE__REVERT"></span>[**IPropertyStorage :: Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert)
</dt> <dd>

Pour les jeux de propriétés qui ne sont pas simples, appelle la méthode [**Revert**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-revert) du stockage sous-jacent et ouvre à nouveau le flux de contenu. Pour les jeux de propriétés simples, retourne uniquement E \_ OK.

</dd> <dt>

<span id="IPropertyStorage__Enum"></span><span id="ipropertystorage__enum"></span><span id="IPROPERTYSTORAGE__ENUM"></span>[**IPropertyStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-enum)
</dt> <dd>

Crée un objet énumérateur qui implémente [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg), dont les méthodes peuvent être appelées pour énumérer les structures [**STATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) qui fournissent des informations sur chacune des propriétés de l’ensemble.

Cette implémentation crée un tableau dans lequel le jeu de propriétés entier est lu et qui peut être partagé quand [**IEnumSTATPROPSTG :: Clone**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) est appelé.

</dd> <dt>

<span id="IPropertyStorage__Stat"></span><span id="ipropertystorage__stat"></span><span id="IPROPERTYSTORAGE__STAT"></span>[**IPropertyStorage :: stat**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-stat)
</dt> <dd>

Remplit les membres d’une structure [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) , qui contient des informations sur la propriété définie dans son ensemble. Au retour, fournit un pointeur vers la structure.

Pour les jeux de stockage qui ne sont pas simples, cette implémentation appelle [**IStorage :: stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) (ou [**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)) pour obtenir les informations à partir du flux ou du stockage sous-jacent.

</dd> <dt>

<span id="IPropertyStorage__SetTimes"></span><span id="ipropertystorage__settimes"></span><span id="IPROPERTYSTORAGE__SETTIMES"></span>[**IPropertyStorage::SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes)
</dt> <dd>

Pour les jeux de propriétés qui ne sont pas simples, définit les heures prises en charge par le stockage sous-jacent. Cette implémentation de [**SetTimes**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-settimes) appelle la méthode [**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes) du stockage sous-jacent pour modifier les heures. Il prend en charge les heures prises en charge par la méthode sous-jacente, qui peuvent être l’heure de modification, le temps d’accès ou l’heure de création.

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IPropertySetStorage-implémentation autonome](ipropertysetstorage-stand-alone-implementation.md)
</dt> <dt>

[**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
</dt> <dt>

[**IStorage :: SetElementTimes**](/windows/desktop/api/Objidl/nf-objidl-istorage-setelementtimes)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> </dl>

 

 