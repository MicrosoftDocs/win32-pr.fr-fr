---
title: IPropertySetStorage-implémentation autonome
description: L’implémentation autonome fournie par le système de IPropertySetStorage comprend une implémentation de IPropertyStorage et IPropertySetStorage.
ms.assetid: 0ea5aadf-0b3f-44ac-9bb7-a7e8292f04c2
keywords:
- IPropertySetStorage Strctd STG, implémentations
- IPropertySetStorage Strctd STG, implémentations, autonome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b4aec27afd0e02ffcb9886f13de2a17761c66eab106665fe4143ab42c86a35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117961278"
---
# <a name="ipropertysetstorage-stand-alone-implementation"></a>IPropertySetStorage-implémentation autonome

L’implémentation autonome fournie par le système de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) comprend une implémentation de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) et **IPropertySetStorage**. [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) est l’interface qui lit et écrit les propriétés dans un stockage de jeu de propriétés. [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) est l’interface qui crée et ouvre les jeux de propriétés dans un stockage. Les interfaces [**IEnumSTATPROPSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropstg) et [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) sont également fournies dans l’implémentation autonome.

Pour utiliser l’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage), obtenez d’abord un pointeur vers l’implémentation fournie par le système et autonome, et associez l’implémentation fournie par le système à votre objet de stockage. Pour obtenir un pointeur vers l’implémentation autonome de **IPropertySetStorage**, appelez la fonction [**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg) et fournissez le paramètre *pStorage* en spécifiant l’objet de stockage qui contiendra le jeu de propriétés. Cette fonction fournit un pointeur vers la nouvelle interface **IPropertySetStorage** pour l’objet de stockage spécifié.

L’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) crée des jeux de propriétés sur n’importe quel objet de stockage, pas seulement sur des stockages de fichiers composés. L’implémentation autonome ne dépend pas de fichiers composés et peut être utilisée avec n’importe quelle implémentation de stockage structuré. Toutes les restrictions sur les stockages structurés fournis par l’appelant s’appliquent à cette implémentation des jeux de propriétés. Par exemple, si vous fournissez un stockage en mode simple à [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg), le **IPropertySetStorage** résultant sera limité par l' [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)fourni.

Pour plus d’informations sur l’implémentation de fichier composé de cette interface, consultez la section [IPropertySetStorage-Implementation file Implementation](ipropertysetstorage-compound-file-implementation.md).

## <a name="when-to-use"></a>Quand l’utiliser

Appelez les méthodes de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) pour créer, ouvrir et supprimer des jeux de propriétés dans tout stockage structuré. Il existe également une méthode qui fournit un pointeur vers l’énumérateur [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) qui peut être utilisé pour énumérer les jeux de propriétés dans le stockage.

L’implémentation autonome fournit également les fonctions d’assistance [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) et [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) , en plus des méthodes [**Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) et [**Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open) , pour créer et ouvrir des jeux de propriétés. Ces deux fonctions ajoutent la prise en charge de la \_ valeur non mise en mémoire tampon PROPSETFLAG afin que vous puissiez écrire les modifications directement dans le jeu de propriétés au lieu de les mettre en mémoire tampon dans un cache. Pour plus d’informations, consultez [**constantes PROPSETFLAG**](propsetflag-constants.md).

## <a name="methods"></a>Méthodes

L’implémentation autonome de [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) prend en charge les méthodes suivantes.

<dl> <dt>

<span id="IPropertySetStorage__Create"></span><span id="ipropertysetstorage__create"></span><span id="IPROPERTYSETSTORAGE__CREATE"></span>[**IPropertySetStorage :: Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)
</dt> <dd>

Crée un nouveau jeu de propriétés dans le stockage et retourne un pointeur vers l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.

Si vous envisagez d’utiliser la \_ valeur non mise en mémoire tampon PROPSETFLAG, utilisez la fonction [**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg) à la place pour créer et ouvrir le nouveau jeu de propriétés et pour obtenir un pointeur vers l’implémentation autonome de l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.

</dd> <dt>

<span id="IPropertySetStorage__Open"></span><span id="ipropertysetstorage__open"></span><span id="IPROPERTYSETSTORAGE__OPEN"></span>[**IPropertySetStorage :: Open**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-open)
</dt> <dd>

Ouvre un jeu de propriétés existant dans le stockage et retourne un pointeur vers l’interface [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés.

Si vous envisagez d’utiliser la \_ valeur non mise en mémoire tampon PROPSETFLAG, utilisez la fonction [**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg) à la place pour obtenir un pointeur vers l’implémentation autonome de [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) sur le jeu de propriétés spécifié.

</dd> <dt>

<span id="IPropertySetStorage__Delete"></span><span id="ipropertysetstorage__delete"></span><span id="IPROPERTYSETSTORAGE__DELETE"></span>[**IPropertySetStorage ::D supprim**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-delete)
</dt> <dd>

Supprime un jeu de propriétés dans ce jeu de propriétés stockage.

</dd> <dt>

<span id="IPropertySetStorage__Enum"></span><span id="ipropertysetstorage__enum"></span><span id="IPROPERTYSETSTORAGE__ENUM"></span>[**IPropertySetStorage :: enum**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-enum)
</dt> <dd>

Crée un objet qui peut être utilisé pour énumérer des structures [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) . Chaque structure **STATPROPSETSTG** fournit des données relatives à un jeu de propriétés unique.

> [!Note]  
> La propriété DocumentSummaryInformation et UserDefined définie est unique en ce qu’elle peut avoir deux sections de jeu de propriétés dans un seul flux sous-jacent. Pour plus d’informations, consultez [les jeux de propriétés DocumentSummaryInformation et UserDefined](the-documentsummaryinformation-and-userdefined-property-sets.md) .

 

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[IPropertyStorage-implémentation autonome](ipropertystorage-stand-alone-implementation.md)
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
</dt> <dt>

[**StgCreatePropSetStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropsetstg)
</dt> <dt>

[**StgCreatePropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatepropstg)
</dt> <dt>

[**StgOpenPropStg**](/windows/desktop/api/coml2api/nf-coml2api-stgopenpropstg)
</dt> <dt>

[**Constantes STGM**](stgm-constants.md)
</dt> </dl>

 

 