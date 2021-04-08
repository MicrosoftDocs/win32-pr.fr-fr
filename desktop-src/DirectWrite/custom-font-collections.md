---
title: Collections de polices personnalisées (Windows 7/8)
description: DirectWrite permet d’accéder à la collection de polices système à l’aide de la méthode IDWriteFactory GetSystemFontCollection.
ms.assetid: ec892904-6778-4fbd-93b4-62d0db5b82ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39aa764330f27b72051ef682c6ce5f1176c42c7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728684"
---
# <a name="custom-font-collections-windows-78"></a>Collections de polices personnalisées (Windows 7/8)

[DirectWrite](direct-write-portal.md) permet d’accéder à la collection de polices système à l’aide de la méthode [**IDWriteFactory :: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . Il s’agit de la collection de polices la plus fréquemment utilisée. Toutefois, certaines applications doivent utiliser des polices qui ne sont pas installées sur le système, telles que des fichiers de polices inclus ou des fichiers de police incorporés dans l’application.

Si les polices que vous souhaitez ne sont pas dans la collection de polices système, vous pouvez créer une collection de polices personnalisée dérivée de [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection).

Cette vue d’ensemble se compose des éléments suivants :

-   [Inscription et annulation de l’inscription d’un chargeur de collection de polices](#registering-and-unregistering-a-font-collection-loader)
-   [IDWriteFontCollectionLoader](#idwritefontcollectionloader)
-   [IDWriteFontFileEnumerator](#idwritefontfileenumerator)
-   [CreateCustomFontFileReference](#createcustomfontfilereference)
-   [IDWriteFontFileLoader](#idwritefontfileloader)
-   [IDWriteFontFileStream](#idwritefontfilestream)

## <a name="registering-and-unregistering-a-font-collection-loader"></a>Inscription et annulation de l’inscription d’un chargeur de collection de polices

Vous inscrivez un chargeur de collection de polices à l’aide de la méthode [**IDWriteFactory :: RegisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontcollectionloader) et en lui transmettant une interface [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implémentée par l’application en tant qu’objet singleton. Cet objet chargera les polices lorsque la collection personnalisée sera demandée. La collection de polices système et les collections de polices personnalisées sont mises en cache, de sorte que les polices ne sont chargées qu’une seule fois.

Le chargeur de collection de polices doit éventuellement être déchargé à l’aide de [**IDWriteFactory :: UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader).

> [!Note]  
> L’inscription du chargeur de collection de polices ajoute au décompte de références. n’appelez pas [**UnregisterFontCollectionLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontcollectionloader) à partir du destructeur ou l’objet chargeur de collection ne sera jamais inscrit.

 

## <a name="idwritefontcollectionloader"></a>IDWriteFontCollectionLoader

Vous créez un objet [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) à l’aide de [**IDWriteFactory :: CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) et en lui transmettant une clé définie par l’application. La clé est un pointeur void et le type de données, le format et la signification sont définis par l’application et sont opaques pour le système de polices.

Alors que la clé peut être n’importe quoi, [DirectWrite](direct-write-portal.md) requiert que chaque clé soit à la fois :

-   Unique à une collection de polices unique dans l’étendue du chargeur.
-   Valide jusqu’à ce que le chargeur soit désinscrit à l’aide de la fabrique.

Lorsque la méthode [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection) est appelée, [DirectWrite](direct-write-portal.md) rappelle une interface [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) implémentée en tant qu’objet singleton par l’application. La méthode de rappel [**IDWriteFontCollectionLoader :: CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) est utilisée par DirectWrite pour récupérer un objet [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) implémenté par l’application. L’objet [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) utilisé pour créer la collection est passé à cette méthode et doit être utilisé par l’énumérateur de fichier de police pour créer les objets [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) à inclure dans la collection.

La clé passée à cette méthode identifie la collection de polices et est la même clé passée à [**CreateCustomFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontcollection).

## <a name="idwritefontfileenumerator"></a>IDWriteFontFileEnumerator

L’objet [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) défini par l’application qui a été créé par la méthode [**CreateEnumeratorFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontcollectionloader-createenumeratorfromkey) est utilisé pour énumérer les fichiers de polices dans une collection, en créant un objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) pour chaque fichier. La méthode [**IDWriteFontFileEnumerator :: MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) remplace la position par le fichier de police suivant. Si un fichier se trouve à la position, il affecte la valeur **true** à *hasCurrentFile* . Dans le cas contraire, elle est définie sur **false** et la méthode retourne **S \_ OK**.

> [!Note]  
> L’énumérateur de fichier de police doit commencer par être positionné avant le premier élément et avancé au premier appel de [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext).

 

Un objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) est généré par la méthode [**IDWriteFontFileEnumerator :: GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) . S’il n’y a aucun fichier de police à la position actuelle, car [**MoveNext**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-movenext) n’a pas encore été appelé ou hasCurrentFile a été défini sur **false**, **GetCurrentFontFile** retourne alors **E \_ Fail**.

## <a name="createcustomfontfilereference"></a>CreateCustomFontFileReference

La sortie de l’objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) par [**GetCurrentFontFile**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileenumerator-getcurrentfontfile) peut être créée en appelant [**IDWriteFactory :: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference). La clé de référence de fichier de police identifie une référence de fichier de police spécifique et doit être unique dans le chargeur de fichier de police qui chargera le fichier.

## <a name="idwritefontfileloader"></a>IDWriteFontFileLoader

La méthode [**CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) prend un objet [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) implémenté par l’application utilisée pour charger la police. La méthode de rappel [**IDWriteFontFileLoader :: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) reçoit la clé et génère un objet [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) .

## <a name="idwritefontfilestream"></a>IDWriteFontFileStream

L’objet [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) implémenté par l’application fournit les données de fichier de police pour une référence de fichier de police d’un chargeur de fichier de polices personnalisé. Avec la taille de fichier et l’heure de la dernière écriture, il fournit une méthode ([**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment)) pour la récupération des fragments de fichier qui doivent être compilés dans un objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) .

> [!Note]  
> Les implémentations de [**ReadFileFragment**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfilestream-readfilefragment) doivent retourner une erreur si le fragment demandé se trouve en dehors des limites du fichier.

 

Un [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) peut récupérer le contenu du fichier de police où que vous soyez, par exemple le lecteur de disque dur local ou les ressources incorporées.

 

 