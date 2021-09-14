---
title: IStream-implémentation de fichier composé
description: L’interface IStream prend en charge la lecture et l’écriture de données dans des objets de flux. Dans un objet de stockage structuré, les objets de flux contiennent les données et les stockages fournissent la structure.
ms.assetid: 52474e37-0e14-4dcc-8e04-4442cfd26eb3
keywords:
- IStream Strctd STG, implémentation de fichier composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16d15e671521f4a1e81b78579bc1225eccb48898
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008918"
---
# <a name="istream---compound-file-implementation"></a>IStream-implémentation de fichier composé

L’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) prend en charge la lecture et l’écriture de données dans des objets de flux. Dans un objet de stockage structuré, les objets de flux contiennent les données et les stockages fournissent la structure. Les données simples peuvent être écrites directement dans un flux, mais plus fréquemment, les flux sont des éléments imbriqués dans un objet de stockage. Elles sont similaires aux fichiers standard.

La spécification de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) définit davantage de fonctionnalités que celles prises en charge par l’implémentation com. Par exemple, l’interface **IStream** définit des flux d’une longueur maximale de 2 ⁶ ⁴ octets nécessitant un pointeur de recherche de 64 bits. Toutefois, l’implémentation COM prend uniquement en charge les flux allant jusqu’à 2 ³ octets ² en longueur (4 Go) et les opérations de lecture et d’écriture sont toujours limitées à 2 ³ ² octets à la fois. L’implémentation COM ne prend pas non plus en charge les transactions de flux ou le verrouillage de région.

Pour créer un flux simple basé sur la mémoire globale, récupérez un pointeur [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en appelant la fonction d’API [**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal). Pour obtenir un pointeur **IStream** dans un objet de fichier composé, appelez [**StgCreateDocFile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) ou [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage). Ces fonctions récupèrent un pointeur [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) , avec lequel vous pouvez ensuite appeler [**CreateStream,**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) ou [**OpenStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-openstream) pour un pointeur **IStream** . Dans les deux cas, le même code d’implémentation **IStream** est utilisé.

> [!Note]  
> L’implémentation de fichier composé de stockage structuré ne fonctionne pas sur une méthode [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour [**ISequentialStream**](/windows/desktop/api/Objidl/nn-objidl-isequentialstream), mais elle comprend les méthodes [**Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read) et [**Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write) via le pointeur d’interface [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) .

 

## <a name="when-to-use"></a>Quand l’utiliser

Appeler les méthodes de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pour lire et écrire des données dans un flux.

Étant donné que les objets de flux peuvent être marshalés vers d’autres processus, les applications peuvent partager les données dans des objets de stockage sans avoir à utiliser de la mémoire globale. Dans l’implémentation de fichier composé COM des objets de flux, les fonctions de marshaling personnalisées dans COM créent une version distante de l’objet d’origine dans le nouveau processus lorsque les deux processus ont accès à la mémoire partagée. Par conséquent, la version distante n’a pas besoin de communiquer avec le processus d’origine pour exécuter ses fonctions.

La version distante de l’objet de flux partage le même pointeur de recherche que le flux d’origine. Si vous ne souhaitez pas partager le pointeur de recherche, utilisez la méthode [**IStream :: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) pour fournir une copie de l’objet de flux pour le processus distant.

> [!Note]
> Si vous créez un objet de flux plus grand que le tas dans la mémoire de votre ordinateur et que vous utilisez un descripteur **HGLOBAL** à un objet de mémoire global, l’objet de flux appelle la méthode [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) en interne whe il requiert plus de mémoire. Étant donné que **GlobalReAlloc** copie toujours les données de la source vers la destination, le fait d’augmenter un objet de flux de 20 Mo à 25 Mo, par exemple, nécessite un temps considérable. Cela est dû à la taille des incréments copiés et est aggravé s’il y a moins de 45 Mo de mémoire sur l’ordinateur en raison de l’échange de disque.
>
> La solution recommandée consiste à implémenter une méthode [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) qui utilise la mémoire allouée par [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc) au lieu de [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc). Cela peut réserver un grand segment d’espace d’adressage virtuel, puis valider la mémoire dans cet espace d’adressage en fonction des besoins. Aucune copie de données ne se produit et la mémoire n’est validée que si nécessaire.
>
> Une alternative à [**GlobalReAlloc**](/windows/desktop/api/winbase/nf-winbase-globalrealloc) consiste à appeler la méthode [**IStream :: desets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize) sur l’objet de flux pour augmenter l’allocation de mémoire à l’avance. Toutefois, ce n’est pas aussi efficace que l’utilisation de [**VirtualAlloc**](/windows/desktop/api/memoryapi/nf-memoryapi-virtualalloc), comme décrit ci-dessus.

 

## <a name="methods"></a>Méthodes

<dl> <dt>

<span id="ISequentialStream__Read"></span><span id="isequentialstream__read"></span><span id="ISEQUENTIALSTREAM__READ"></span>[**ISequentialStream :: Read**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-read)
</dt> <dd>

Lit un nombre spécifié d'octets à partir de l'objet de flux dans la mémoire en commençant au niveau du pointeur de recherche actuel. Cette implémentation retourne S \_ OK si la fin du flux a été atteinte pendant la lecture. (Il s’agit du même comportement que celui de la « fin du fichier » trouvé dans le système de fichiers FAT MS-DOS.)

</dd> <dt>

<span id="ISequentialStream__Write"></span><span id="isequentialstream__write"></span><span id="ISEQUENTIALSTREAM__WRITE"></span>[**ISequentialStream :: Write**](/windows/desktop/api/Objidl/nf-objidl-isequentialstream-write)
</dt> <dd>

Écrit un nombre spécifié d’octets dans l’objet de flux, en commençant au pointeur de recherche actuel. Dans cette implémentation, les objets de flux ne sont pas éparpillés. Tout octet de remplissage est finalement alloué sur le disque et affecté au flux.

</dd> <dt>

<span id="IStream__Seek"></span><span id="istream__seek"></span><span id="ISTREAM__SEEK"></span>[**IStream :: Seek**](/windows/desktop/api/Objidl/nf-objidl-istream-seek)
</dt> <dd>

Modifie le pointeur de recherche vers un nouvel emplacement relatif au début du flux, à la fin du flux, ou au pointeur de recherche actuel.

</dd> <dt>

<span id="IStream__SetSize"></span><span id="istream__setsize"></span><span id="ISTREAM__SETSIZE"></span>[**IStream :: assets**](/windows/desktop/api/Objidl/nf-objidl-istream-setsize)
</dt> <dd>

Modifie la taille de l'objet de flux. Dans cette implémentation, il n’y a aucune garantie que l’espace alloué sera contigu.

</dd> <dt>

<span id="IStream__CopyTo"></span><span id="istream__copyto"></span><span id="ISTREAM__COPYTO"></span>[**IStream :: CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto)
</dt> <dd>

Copie un nombre spécifié d'octets à partir du pointeur de recherche actuel d'un flux vers le pointeur de recherche actuel d'un autre flux.

</dd> <dt>

<span id="IStream__Commit"></span><span id="istream__commit"></span><span id="ISTREAM__COMMIT"></span>[**IStream :: Commit**](/windows/desktop/api/Objidl/nf-objidl-istream-commit)
</dt> <dd>

L’implémentation de fichier composé de [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) prend en charge l’ouverture des flux uniquement en mode direct, et non en mode traité. Par conséquent, la méthode n’a aucun effet quand elle est appelée, sauf pour vider toutes les mémoires tampons de mémoire au niveau de stockage suivant.

Dans cette implémentation, peu importe si vous validez des modifications apportées aux flux, vous n’avez besoin que de valider les modifications des objets de stockage.

</dd> <dt>

<span id="IStream__Revert"></span><span id="istream__revert"></span><span id="ISTREAM__REVERT"></span>[**IStream :: Revert**](/windows/desktop/api/Objidl/nf-objidl-istream-revert)
</dt> <dd>

Cette implémentation ne prend pas en charge les flux transactionnels, donc un appel à cette méthode n’a aucun effet.

</dd> <dt>

<span id="IStream__LockRegion"></span><span id="istream__lockregion"></span><span id="ISTREAM__LOCKREGION"></span>[**IStream :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion)
</dt> <dd>

Le verrouillage de plage n’est pas pris en charge par cette implémentation, donc un appel à cette méthode n’a aucun effet.

</dd> <dt>

<span id="IStream__UnlockRegion"></span><span id="istream__unlockregion"></span><span id="ISTREAM__UNLOCKREGION"></span>[**IStream :: UnlockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-unlockregion)
</dt> <dd>

Supprime la restriction d’accès sur une plage d’octets précédemment restreinte avec [**IStream :: LockRegion**](/windows/desktop/api/Objidl/nf-objidl-istream-lockregion).

</dd> <dt>

<span id="IStream__Stat"></span><span id="istream__stat"></span><span id="ISTREAM__STAT"></span>[**IStream :: stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat)
</dt> <dd>

Récupère la structure [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg) pour ce flux

</dd> <dt>

<span id="IStream__Clone"></span><span id="istream__clone"></span><span id="ISTREAM__CLONE"></span>[**IStream :: Clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone)
</dt> <dd>

Crée un objet de flux avec son propre pointeur de recherche qui référence les mêmes octets que le flux d'origine.

</dd> </dl>

Un [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) en mode simple est soumis aux contraintes suivantes.

-   Un flux est en mode simple s’il a été créé ou ouvert à partir d’un stockage en mode simple. Un stockage est un mode simple s’il est créé ou ouvert avec l' \_ indicateur simple STGM défini dans le paramètre *grfMode* .
-   Les méthodes [**clone**](/windows/desktop/api/Objidl/nf-objidl-istream-clone) et [**CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istream-copyto) ne sont pas prises en charge.
-   La méthode [**Stat**](/windows/desktop/api/Objidl/nf-objidl-istream-stat) est prise en charge, mais la \_ valeur NoName StatFlag doit être spécifiée.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**CreateStreamOnHGlobal**](/windows/desktop/api/combaseapi/nf-combaseapi-createstreamonhglobal)
</dt> <dt>

[**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)
</dt> <dt>

[**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage)
</dt> </dl>

 

 