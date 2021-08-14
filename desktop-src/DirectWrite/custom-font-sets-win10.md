---
title: Jeux de polices personnalisés
description: Cette rubrique décrit les différentes façons dont vous pouvez utiliser des polices personnalisées dans votre application.
ms.assetid: 50842838-d150-df9a-f1b7-67ce5ea2bc80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4b8b9c49895c2b137aaa33cf0788d9518a1d53834c74eb27feb6b44fa045d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118650283"
---
# <a name="custom-font-sets"></a>Jeux de polices personnalisés

Cette rubrique décrit les différentes façons dont vous pouvez utiliser des polices personnalisées dans votre application.

-   [Présentation ](#introduction)
-   [Résumé des API](#summary-of-apis)
-   [Concepts clés](#key-concepts)
-   [Polices et formats de fichier de police](#fonts-and-font-file-formats)
-   [Jeux de polices et collections de polices](#font-sets-and-font-collections)
-   [Scénarios courants](#common-scenarios)
    -   [Création d’un jeu de polices à l’aide de polices arbitraires dans le système de fichiers local](#creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system)
    -   [Création d’un jeu de polices à l’aide des polices connues dans le système de fichiers local](#creating-a-font-set-using-known-fonts-in-the-local-file-system)
    -   [Création d’un jeu de polices personnalisé à l’aide de polices distantes connues sur le Web](#creating-a-custom-font-set-using-known-remote-fonts-on-the-web)
    -   [Création d’un jeu de polices personnalisé à l’aide des données de police chargées en mémoire](#creating-a-custom-font-set-using-font-data-loaded-into-memory)
-   [Scénarios avancés](#advanced-scenarios)
    -   [Combinaison de jeux de polices](#combining-font-sets)
    -   [Utilisation des données de police WOFF ou WOFF2 locales ](#using-local-woff-or-woff2-font-data)
    -   [utilisation de DirectWrite mécanismes de police à distance avec une implémentation réseau de bas niveau personnalisée](#using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation)
    -   [scénarios de prise en charge des versions antérieures de Windows](#supporting-scenarios-on-earlier-windows-versions)

## <a name="introduction"></a>Introduction

La plupart du temps, les applications utilisent les polices installées localement sur le système. DirectWrite permet d’accéder à ces polices à l’aide des méthodes [**IDWriteFactory3 :: GetSystemFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset) ou [**IDWriteFactory :: GetSystemFontCollection**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) . dans certains cas, les applications peuvent également utiliser des polices incluses dans le cadre de Windows 10, mais qui ne sont pas installées actuellement sur le système actuel. ces polices sont accessibles à partir du service de police Windows à l’aide de la méthode **GetSystemFontSet** , ou en appelant [**IDWriteFactory3 :: GetSystemFontCollection**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection) avec includeDownloadableFonts défini sur TRUE. 

dans certains scénarios d’application, toutefois, les applications doivent utiliser des polices qui ne sont pas installées dans le système et qui ne sont pas fournies par le Service de police Windows. Voici quelques exemples de ces scénarios :

-   Les polices sont incorporées en tant que ressources dans un fichier binaire d’application.
-   Les fichiers de polices sont regroupés dans un package d’application et stockés sur le disque dans le dossier d’installation de l’application.
-   L’application est un outil de développement de polices qui doit charger les fichiers de police spécifiés par l’utilisateur. 
-   Les polices sont incorporées dans des fichiers de document qui peuvent être affichés ou modifiés dans l’application. 
-   L’application utilise des polices obtenues à partir d’un service de police Web public. 
-   L’application utilise les données de police diffusées en continu via un protocole de réseau privé. 

DirectWrite fournit des api pour l’utilisation de polices personnalisées dans ces scénarios similaires. Les données de police personnalisées peuvent provenir de fichiers dans le système de fichiers local ; à partir de sources Cloud accessibles à l’aide de HTTP ; ou à partir de sources arbitraires après avoir été chargées dans une mémoire tampon. 

> [!Note]  
> bien que DirectWrite ait fourni des api pour l’utilisation des polices personnalisées depuis Windows 7, des api plus récentes ont été ajoutées à Windows 10 et de nouveau dans le Windows 10 Creators Update (version préliminaire 15021 ou ultérieure) qui facilite l’implémentation de plusieurs scénarios mentionnés. Cette rubrique se concentre sur les API disponibles dans Windows 10. pour les applications qui doivent travailler sur des versions antérieures de Windows, consultez [Collections de polices personnalisées (Windows 7/8)](custom-font-collections.md). 

 

## <a name="summary-of-apis"></a>Résumé des API

Cette rubrique se concentre sur les fonctionnalités fournies par les API suivantes : 

-   Interface [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   Interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   Interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) 
-   Interface [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference)
-   Interface [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile)
-   [**IDWriteFactory :: CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) , méthode 
-   [**IDWriteFactory :: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) , méthode 
-   [**IDWriteFactory3 :: CreateFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-createfontfacereference) , méthodes 
-   [**DWRITE \_ Structure de la \_ propriété font**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) 
-   [**DWRITE \_ \_ \_**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) Énumération de l’ID de propriété de police 
-   Interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) 
-   [**IDWriteFactory :: RegisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-registerfontfileloader) , méthode 
-   [**IDWriteFactory :: UnregisterFontFileLoader**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-unregisterfontfileloader) , méthode 
-   [**IDWriteFactory5 :: CreateInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createinmemoryfontfileloader) , méthode 
-   Interface [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) 
-   [**IDWriteFactory5 :: CreateHttpFontFileLoader**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-createhttpfontfileloader) , méthode 
-   Interface [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) 
-   Interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) 
-   Interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) 
-   Interface [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) 
-   Interface [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) 
-   Interface [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) 
-   [**IDWriteFactory5 :: AnalyzeContainerType**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-analyzecontainertype) , méthode 
-   [**IDWriteFactory5 :: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile) , méthode 

 

## <a name="key-concepts"></a>Concepts clés

pour comprendre les api DirectWrite pour l’utilisation de polices personnalisées, il peut être utile de comprendre le modèle conceptuel sous-jacent à ces api. Les concepts clés sont décrits ici. 

lorsque DirectWrite effectue une mise en page ou un rendu de texte réel, il doit accéder aux données de police réelles. Un objet de type de police contient les données de police réelles, qui doivent exister dans le système local. Toutefois, pour d’autres opérations, telles que la vérification de la disponibilité d’une police particulière ou la présentation d’un choix de polices à un utilisateur, il suffit d’une référence à une police particulière, et non des données de police réelles. dans DirectWrite, un objet de référence de type de police contient uniquement les informations nécessaires pour localiser et instancier une police. étant donné que la référence de type de police ne contient pas de données réelles, DirectWrite pouvez gérer les références de type de police pour lesquelles les données réelles se trouvent dans un emplacement réseau distant, ainsi que lorsque les données réelles sont locales.

Un jeu de polices est un ensemble de références de type de police, ainsi que certaines propriétés de base et informations qui peuvent être utilisées pour faire référence à la police ou pour la comparer à d’autres polices, telles que le nom de famille ou une valeur de police. Les données réelles des différentes polices peuvent être locales, ou elles peuvent toutes être distantes ou être mélangées.

Un jeu de polices peut être utilisé pour obtenir un objet de collection de polices correspondant. Pour plus d’informations, consultez Jeux de polices et collections de polices ci-dessous. 

L’interface IDWriteFontSet fournit des méthodes qui permettent d’interroger des valeurs de propriété telles que le nom de famille ou le poids de police, ou des références de type de police qui correspondent à des valeurs de propriété particulières. Une fois le filtrage effectué vers une sélection particulière, une instance de l’interface [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) peut être obtenue, avec des méthodes de téléchargement (si les données de police réelles sont actuellement à distance), afin d’obtenir l’objet [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) correspondant qui peut être utilisé pour la disposition et le rendu. 

L’interface IDWriteFontFile sous-tend chaque type de police ou référence de type de police. Cela représente l’emplacement d’un fichier de polices et a deux composants : un chargeur de fichiers de polices et une clé de fichier de police. Le chargeur de fichiers de polices ([**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)) est utilisé pour ouvrir un fichier si nécessaire, et retourne un flux avec les données ([**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream)). Selon le chargeur, les données peuvent se trouver dans un chemin d’accès de fichier local, une URL distante ou dans une mémoire tampon. La clé est une valeur définie par le chargeur qui identifie de façon unique le fichier dans le contexte du chargeur, ce qui permet au chargeur de localiser les données et de créer un flux pour celui-ci. 

Vous pouvez facilement ajouter des polices personnalisées à un jeu de polices personnalisé, qui peut à son tour être utilisé pour filtrer ou organiser les informations de police à des fins telles que la création d’une interface utilisateur de sélecteur de polices. Le jeu de polices peut également être utilisé pour créer une collection de polices à utiliser dans des API de niveau supérieur telles que [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) et [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout). L’interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) peut être utilisée pour créer un jeu de polices personnalisé qui comprend plusieurs polices personnalisées. Il peut également être utilisé pour créer un jeu de polices personnalisé qui mélange des polices personnalisées et des polices fournies par le système. ou qui combine des polices avec des sources différentes pour les données réelles (stockage local, URL distantes et mémoire). 

Comme mentionné précédemment, une référence de type de police peut faire référence à des données de police sur une source distante, mais les données doivent être locales pour obtenir un objet de type de police qui peut être utilisé pour la mise en page et le rendu. Le téléchargement de données distantes est géré par une file d’attente de téléchargement de polices. Les applications peuvent utiliser l’interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) pour mettre en file d’attente les demandes de téléchargement des polices distantes pour initier le processus de téléchargement et inscrire un objet [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) pour prendre des mesures lorsque le processus de téléchargement est terminé. 

pour la plupart des interfaces décrites ici, DirectWrite fournit des implémentations du système. La seule exception est l’interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) , qu’une application implémente pour prendre des mesures spécifiques à l’application lorsque les polices distantes ont été téléchargées localement. Les applications peuvent avoir des raisons de fournir leurs propres implémentations personnalisées pour certaines autres interfaces, bien que cela ne soit nécessaire que dans des scénarios plus avancés et spécifiques. Par exemple, une application doit fournir une implémentation personnalisée de l’interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) pour gérer les fichiers de polices dans le stockage local qui utilisent le format de conteneur WOFF2. Des informations supplémentaires sont fournies ci-dessous. 

## <a name="fonts-and-font-file-formats"></a>Polices et formats de fichier de police

Un autre concept clé qui est utile pour comprendre la relation entre les polices et les fichiers de police qui les contiennent. L’idée d’un fichier de police OpenType (. ttf ou. OTF) contenant une police unique est familière. Toutefois, le format de police OpenType autorise également une collection de polices OpenType (. TTC ou. OTC), qui est un fichier unique qui contient plusieurs polices. Les fichiers de collection OpenType sont souvent utilisés pour les grandes polices étroitement liées et ayant des valeurs identiques pour certaines données de police : en combinant les polices dans un fichier unique, les données communes peuvent être dédupliquées. Pour cette raison, une référence de type police ou de police doit faire référence non seulement à un fichier de police (ou à une source de données équivalente), mais elle doit également spécifier un index de police dans ce fichier, pour le cas général dans lequel le fichier peut être un fichier de collection. 

Pour les polices utilisées sur le Web, les données de police sont souvent empaquetées dans certains formats de conteneur, WOFF ou WOFF2, qui fournissent une certaine compression des données de police et un certain niveau de protection contre le piratage et la violation des licences de polices. Fonctionnellement, un fichier WOFF ou WOFF2 est équivalent à une police OpenType ou à un fichier de collection de polices, mais les données sont encodées dans un format différent qui requiert une décompression avant de pouvoir être utilisées. 

certaines api DirectWrite peuvent gérer des visages de polices, tandis que d’autres peuvent gérer des fichiers qui peuvent inclure des fichiers de Collection OpenType qui contiennent plusieurs visages. De même, certaines API traitent uniquement les données brutes de format OpenType, tandis que les autres API peuvent gérer les formats de conteneur compressés, WOFF et WOFF2. Ces détails sont fournis dans la discussion ci-dessous. 

## <a name="font-sets-and-font-collections"></a>Jeux de polices et collections de polices

Certaines applications peuvent être implémentées pour fonctionner avec les polices à l’aide de l’interface [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) . Il existe une correspondance directe entre une collection de polices et un jeu de polices. Chaque peut contenir les mêmes polices, mais elles sont présentées avec une autre organisation. À partir de n’importe quelle collection de polices, un jeu de polices correspondant peut être obtenu, et vice versa.

Lorsque vous travaillez avec plusieurs polices personnalisées, il est plus facile d’utiliser une interface de générateur de jeu de polices pour créer un jeu de polices personnalisé, puis d’obtenir une collection de polices après la création du jeu de polices. Le processus de création d’un jeu de polices personnalisé est décrit en détail ci-dessous. Pour obtenir une interface [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) à partir d’un jeu de polices, la méthode [**IDWriteFactory3 :: CreateFontCollectionFromFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-createfontcollectionfromfontset) est utilisée.

Si l’application possède un objet collection et doit obtenir un jeu de polices correspondant, cette opération peut être effectuée à l’aide de la méthode [**IDWriteFontCollection1 :: GetFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontcollection1-getfontset) . 

## <a name="common-scenarios"></a>Scénarios courants

Cette section décrit certains des scénarios les plus courants impliquant des jeux de polices personnalisés :

-   Création d’un jeu de polices personnalisé à l’aide de polices arbitraires dans les chemins d’accès du système de fichiers local.
-   Création d’un jeu de polices personnalisé à l’aide de polices connues (éventuellement fournies avec l’application) stockées dans le système de fichiers local.
-   Création d’un jeu de polices personnalisé à l’aide de polices distantes connues sur le Web.
-   Création d’un jeu de polices personnalisé à l’aide des données de police chargées en mémoire.

les implémentations complètes pour ces scénarios sont fournies dans l' [exemple de jeux de polices personnalisés DirectWrite](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). Cet exemple illustre également un scénario plus avancé pour gérer les données de police compressées dans des formats de conteneur WOFF ou WOFF2, qui seront abordés ci-dessous. 

### <a name="creating-a-font-set-using-arbitrary-fonts-in-the-local-file-system"></a>Création d’un jeu de polices à l’aide de polices arbitraires dans le système de fichiers local

En cas de traitement d’un ensemble arbitraire de fichiers de polices dans le stockage local, la méthode [**IDWriteFontSetBuilder1 :: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) est pratique, car, dans un seul appel, elle peut gérer toutes les visages de police dans un fichier de collection de polices OpenType, ainsi que toutes les instances pour une police de variable OpenType. cette option est disponible dans le Windows 10 Creators Update (version préliminaire 15021 ou ultérieure), et est recommandée chaque fois qu’elle est disponible. 

Pour utiliser cette méthode, utilisez le processus suivant.

<dl> 1. Commencez par créer l’interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5">IDWriteFactory5</a> : 


```C++
IDWriteFactory5* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
  DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



   
2. Utilisez la fabrique pour obtenir l' <a href=""></a> interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) : 


```C++
IDWriteFontSetBuilder1* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
}  
                
```



  
3. Pour chaque fichier de police dans le système de fichiers local, créez un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) qui y fait référence : 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



   
4. Ajoutez l’objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) au générateur de jeu de polices à l’aide de la méthode [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) : 


```C++
hr = pFontSetBuilder->AddFontFile(pFontFile); 
```

Si le chemin d’accès au fichier spécifié dans l’appel à [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) fait appel à autre chose qu’un fichier OpenType pris en charge, l’appel à [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) RENVERRA une erreur, DWRITE \_ E \_ FILEFORMAT.

5. Une fois que tous les fichiers ont été ajoutés au générateur de jeux de polices, le jeu de polices personnalisé peut être créé : 


```C++
IDWriteFontSet* pFontSet; 
hr = pFontSetBuilder->CreateFontSet(&pFontSet); 
```



   
</dl>

si l’application doit s’exécuter sur Windows 10 versions antérieures à la Windows 10 Creators Update, la méthode AddFontFile n’est pas disponible. La disponibilité peut être détectée en créant une interface [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) , puis en utilisant QueryInterface pour essayer d’obtenir une interface [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) : si cela se déroule correctement, l’interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) et la méthode [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) sont également disponibles.

Si la méthode AddFontFile n’est pas disponible, la méthode [**IDWriteFontSetBuilder :: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) doit être utilisée pour ajouter des visages de police individuels. Pour autoriser les fichiers de collection de polices OpenType qui contiennent plusieurs visages, la méthode [**IDWriteFontFile :: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) peut être utilisée pour déterminer le nombre de faces contenues dans le fichier. Le processus est le suivant.

<dl> 1. Commencez par créer l’interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3">IDWriteFactory3</a> : 


```C++
IDWriteFactory3* pDWriteFactory; 
HRESULT hr = DWriteCreateFactory( 
DWRITE_FACTORY_TYPE_SHARED, 
  __uuidof(IDWriteFactory5), 
  reinterpret_cast<IUnknown**>(&pDWriteFactory) 
); 
```



  
2. Utilisez la fabrique pour obtenir l’interface [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) : 


```C++
IDWriteFontSetBuilder* pFontSetBuilder; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontSetBuilder(&pFontSetBuilder); 
} 
```



  
3. Pour chaque fichier de polices, créez un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), comme indiqué ci-dessus : 


```C++
IDWriteFontFile* pFontFile; 
if (SUCCEEDED(hr)) 
{ 
  hr = pDWriteFactory->CreateFontFileReference(pFilePath, /* lastWriteTime*/ nullptr, &pFontFile); 
} 
```



Au lieu d’ajouter le fichier directement dans le générateur de jeux de polices, nous devons déterminer le nombre de visages et créer des objets [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuels.   
4. Utilisez la méthode [**analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) pour connaître le nombre de visages dans le fichier. 


```C++
BOOL isSupported; 
DWRITE_FONT_FILE_TYPE fileType; 
UINT32 numberOfFonts; 
hr = pFontFile->Analyze(&isSupported, &fileType, /* face type */ nullptr, &numberOfFonts); 
```



La méthode [**analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) définit également les valeurs des paramètres IsSupported et filetype. Si le fichier n’est pas un format pris en charge, isSupported a la valeur FALSe, et les actions appropriées, telles que l’ignorance du fichier, peuvent être effectuées.   
5. Parcourez le nombre de polices défini dans le paramètre numberOfFonts. Dans la boucle, créez un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) pour chaque paire fichier/index, puis ajoutez-le au générateur de jeu de polices. 


```C++
for (uint32_t fontIndex = 0; fontIndex < numberOfFonts; fontIndex++) 
{ 
  IDWriteFontFaceReference* pFontFaceReference;
  hr = pDWriteFactory->CreateFontFaceReference(pFontFile, fontIndex, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);

  if (SUCCEEDED(hr))
  {
    hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference);
  }
} 
```



  
6. Une fois toutes les visages ajoutées au générateur de jeu de polices, créez le jeu de polices personnalisé, comme indiqué ci-dessus.  
</dl>

une application peut être conçue pour utiliser la méthode [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) par défaut lors de l’exécution sur le Windows 10 Creators Update, mais revenir à l’utilisation de la méthode [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) lors de l’exécution sur des versions Windows 10 antérieures. Testez la disponibilité de l’interface [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) , comme décrit ci-dessus, puis branchement en conséquence. cette approche est illustrée dans la [DirectWrite exemple de jeux de polices personnalisés](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="creating-a-font-set-using-known-fonts-in-the-local-file-system"></a>Création d’un jeu de polices à l’aide des polices connues dans le système de fichiers local

Comme indiqué ci-dessus, chaque référence de type de police dans un jeu de polices est associée à certaines propriétés d’information, telles que le nom de famille et l’épaisseur de police. Lorsque des polices personnalisées sont ajoutées à un générateur de jeux de polices à l’aide des appels d’API répertoriés ci-dessus, ces propriétés d’information sont obtenues directement à partir des données de police réelles, qui sont lues lors de l’ajout de la police. Toutefois, dans certaines situations, si une application a une autre source d’informations sur une police, elle peut souhaiter fournir ses propres valeurs personnalisées pour ces propriétés. 

À titre d’exemple, supposons qu’une application regroupe certaines polices utilisées pour présenter des éléments particuliers de l’interface utilisateur dans l’application. Dans certains cas, par exemple avec une nouvelle version de l’application, les polices spécifiques que l’application utilise pour ces éléments devront peut-être être modifiées. Si l’application a encodé des références aux polices spécifiques, le remplacement d’une police par une autre nécessite la modification de l’une de ces références. Au lieu de cela, si l’application utilise des propriétés personnalisées pour assigner des alias fonctionnels en fonction du type d’élément ou de texte rendu, mappe chaque alias à une police spécifique dans un emplacement, puis utilise les alias dans tous les contextes où les polices sont créées et manipulées, puis le remplacement d’une police par une autre nécessite uniquement la modification de l’emplacement où l' 

Des valeurs personnalisées pour les propriétés d’information peuvent être assignées quand la méthode [**IDWriteFontSetBuilder :: AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) est appelée. Pour ce faire, procédez comme suit : il peut être utilisé sur n’importe quelle version de Windows 10. 

Comme indiqué ci-dessus, commencez par obtenir les interfaces [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) et [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) . Pour chaque type de police personnalisé à ajouter, créez un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference), comme indiqué ci-dessus. Avant que cette opération soit ajoutée au générateur de jeu de polices (dans la boucle à l’étape 5, illustrée ci-dessus), l’application définit les valeurs de propriété personnalisées à utiliser. 

Un ensemble de valeurs de propriétés personnalisées est défini à l’aide d’un tableau de structures de [**\_ \_ propriété de police DWRITE**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_property) . Chacun d’entre eux identifie une propriété particulière de l’énumération de l' [**\_ ID de \_ propriété \_ de police DWRITE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id) et la valeur de propriété correspondante à utiliser.  

Notez que toutes les valeurs de propriété sont affectées en tant que chaînes. Si ces derniers peuvent être affichés ultérieurement pour les utilisateurs, d’autres valeurs pour une propriété donnée pour différentes langues peuvent être définies, mais cela n’est pas obligatoire. Notez également que si des valeurs de propriété personnalisées sont définies par l’application, seules les valeurs spécifiées seront utilisées dans le jeu de polices. DirectWrite ne dérivera pas de valeurs directement à partir de la police pour les propriétés d’information utilisées dans un jeu de polices. 

L’exemple suivant définit des valeurs personnalisées pour trois propriétés d’information : le nom de famille, le nom complet et l’épaisseur de police. 


```C++
DWRITE_FONT_PROPERTY props[] = 
{ 
  { DWRITE_FONT_PROPERTY_ID_FAMILY_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_FULL_NAME, L"My Icon Font", L"en-US" }, 
  { DWRITE_FONT_PROPERTY_ID_WEIGHT, L"400", nullptr } 
}; 
               
            
```



Après avoir défini le tableau souhaité de valeurs de propriété pour une police, effectuez un appel à AddFontFaceRefence, en passant le tableau de propriétés ainsi que la référence de type de police. 


```C++
hr = pFontSetBuilder->AddFontFaceReference(pFontFaceReference, props, ARRAYSIZE(props)); 
```



 

Une fois que toutes les polices personnalisées ont été ajoutées au générateur de jeu de polices, avec leurs propriétés personnalisées, créez le jeu de polices personnalisé, comme indiqué ci-dessus. 

### <a name="creating-a-custom-font-set-using-known-remote-fonts-on-the-web"></a>Création d’un jeu de polices personnalisé à l’aide de polices distantes connues sur le Web

Les propriétés personnalisées sont importantes pour l’utilisation des polices distantes. Chaque référence de type de police doit avoir des propriétés d’informations pour caractériser la police et la distinguer des autres polices. étant donné que les données de police des polices distantes ne sont pas locales, DirectWrite ne peut pas dériver des propriétés directement à partir des données de police. Par conséquent, les propriétés doivent être fournies explicitement lors de l’ajout d’une police à distance au générateur de jeu de polices.

La séquence d’appels d’API permettant d’ajouter des polices distantes à un jeu de polices est semblable à celle décrite dans le scénario précédent. Dans la mesure où les données de police sont distantes, les opérations impliquées dans la lecture des données de police réelles sont différentes de celles que vous utilisez pour travailler avec des fichiers dans le stockage local. Dans ce cas, une nouvelle interface de niveau inférieur, [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader), a été ajoutée au Windows 10 Creators Update. 

pour utiliser le chargeur de fichiers de polices à distance, il doit d’abord être inscrit auprès d’une fabrique de DirectWrite. Le chargeur doit être détenu par l’application tant que les polices qui lui sont associées sont utilisées. Une fois que les polices ne sont plus utilisées, et à un moment donné avant la destruction de la fabrique, le chargeur doit être désinscrit. Cela peut être fait dans le destructeur de la classe qui possède l’objet Loader. Ces étapes sont présentées ci-dessous. 

La méthode de création d’un jeu de polices personnalisé à l’aide de polices distantes est la suivante : Cela nécessite la Windows 10 Creators Update.  

<dl> 1. Créez une interface IDWriteFactory5, comme illustré ci-dessus.   
2. Créez une interface <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder">IDWriteFontSetBuilder</a> , comme illustré ci-dessus.   
3. Utilisez la fabrique pour obtenir un <a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader">IDWriteRemoteFontFileLoader</a>. 


```C++
IDWriteRemoteFontFileLoader* pRemoteFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateHttpFontFileLoader( 
        /* referrerURL */ nullptr, 
        /* extraHeaders */ nullptr, 
        &pRemoteFontFileLoader 
    ); 
} 
```



Cela retourne une implémentation fournie par le système de l’interface de chargeur de fichiers de polices distantes qui est en mesure de gérer les interactions HTTP pour le téléchargement des données de police pour le compte de l’application. Une URL de point d’accès ou des en-têtes supplémentaires peuvent être spécifiés si requis par le service de police ou les services qui constituent la source des polices.    

> [!IMPORTANT]
> Remarque relative à la sécurité : lorsqu’une tentative est effectuée pour extraire une police distante, il est possible qu’une personne malveillante usurpe le serveur prévu qui sera appelé. Dans ce cas, les URL de cible et de référent et les détails d’en-tête sont divulgués à la personne malveillante. Les développeurs d’applications sont responsables de l’atténuation de ce risque. Il est recommandé d’utiliser le protocole HTTPs plutôt que HTTP. 

 

Un chargeur de fichiers de polices à distance unique peut être utilisé pour plusieurs polices, même si différents chargeurs peuvent être utilisés si des polices sont obtenues à partir de plusieurs services qui ont des exigences différentes pour l’URL de renvoi ou les en-têtes supplémentaires.   
4. Inscrivez le chargeur de fichiers de polices à distance avec la fabrique. 


```C++
 if (SUCCEEDED(hr)) 
 { 
     hr = pDWriteFactory->RegisterFontFileLoader(pRemoteFontFileLoader); 
 } 
```



À partir de ce point, les étapes de création du jeu de polices personnalisé sont similaires à celles décrites pour les fichiers de polices locales connus, avec deux exceptions importantes. Tout d’abord, l’objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) est créé à l’aide de l’interface du chargeur de fichiers de polices distantes au lieu d’utiliser la fabrique. Deuxièmement, la méthode Analyze ne peut pas être utilisée, car les données de police ne sont pas locales. Au lieu de cela, l’application doit savoir si le fichier de police à distance est un fichier de collection de polices OpenType et, si tel est le cas, il doit savoir laquelle des polices de la collection sera utilisée et l’index de chaque. Par conséquent, les étapes restantes sont les suivantes.   
5. Pour chaque fichier de polices à distance, utilisez l’interface du chargeur de fichier de police à distance pour créer un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile), en spécifiant l’URL requise pour accéder au fichier de polices. 


```C++
 IDWriteFontFile* pFontFile; 
 hr = pRemoteFontFileLoader->CreateFontFileReferenceFromUrl( 
     pDWriteFactory, 
     /* baseUrl */ L"https://github.com/", 
     /* fontFileUrl */ L"winjs/winjs/blob/master/src/fonts/Symbols.ttf?raw=true", 
     &pFontFile 
 ); 
```



Notez que l’URL complète peut être spécifiée dans le paramètre fontFileUrl, ou elle peut être fractionnée en portions de base et relatives. si une url de base est spécifiée, la concaténation des valeurs de baseUrl et fontFileUrl doit fournir l’url complète, DirectWrite ne fournira pas de délimiteur supplémentaire.  

> [!IMPORTANT]
> remarque relative à la sécurité et aux performances : lors d’une tentative d’extraction d’une police distante, il n’y a aucune garantie que Windows recevra une réponse du serveur. Dans certains cas, un serveur peut répondre avec une erreur de fichier introuvable pour une URL relative non valide, mais ne plus répondre s’il reçoit plusieurs demandes non valides. si le serveur ne répond pas, Windows finit par expirer, mais cela peut prendre plusieurs minutes si plusieurs extractions sont lancées. Vous devez effectuer ce qui vous permet de vous assurer que les URL sont valides lorsque des appels sont effectués. 

 

Notez également que l’URL peut pointer vers un fichier de police OpenType brut (. ttf,. otf,. TTC,. OTC), mais elle peut également pointer vers des polices dans un fichier conteneur WOFF ou WOFF2. si un fichier WOFF ou WOFF2 est référencé, l’implémentation DirectWrite du chargeur de fichiers de polices distantes décompresse automatiquement les données de police du fichier conteneur.   
6. Pour chaque index de type de police dans le fichier de polices à distance à utiliser, créez un [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference). 


```C++
 IDWriteFontFaceReference* pFontFaceReference; 
 hr = pDWriteFactory->CreateFontFaceReference(pFontFile, /* faceIndex */ 0, DWRITE_FONT_SIMULATIONS_NONE, &pFontFaceReference);
```



  
7. Définissez les propriétés personnalisées du type de police, comme indiqué ci-dessus.   
8. Ajoutez la référence de type de police avec les propriétés personnalisées au générateur de jeu de polices, comme indiqué ci-dessus.   
9. Une fois que toutes les polices ont été ajoutées au générateur de jeu de polices, créez le jeu de polices, comme indiqué ci-dessus.   
10. À un moment donné, lorsque les polices distantes ne sont plus utilisées, annulez l’inscription du chargeur de fichiers de polices distantes. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pRemoteFontFileLoader); 
```



  
</dl>

Une fois qu’un jeu de polices personnalisé avec des polices distantes personnalisées est créé, le jeu de polices contient des références et des propriétés d’informations pour les polices distantes, mais les données réelles sont toujours distantes. DirectWrite la prise en charge des polices distantes, vous pouvez conserver une référence de type de police dans le jeu de polices, et pour qu’une police soit sélectionnée pour une mise en page et un rendu, mais que les données réelles ne sont pas téléchargées jusqu’à ce qu’il y ait un réel besoin de l’utiliser, par exemple lorsque la disposition du texte sera effectuée.  

une application peut prendre une approche initiale en demandant que DirectWrite télécharger les données de police, puis attendre la confirmation d’un téléchargement réussi avant le début du traitement de la police. Toutefois, un téléchargement réseau implique une certaine latence de durée imprévisible, et la réussite est également incertaine. Pour cette raison, il est généralement préférable d’adopter une approche différente, ce qui permet d’effectuer la mise en page et le rendu initialement à l’aide de polices alternatives ou de secours déjà locales, tout en demandant le téléchargement de la police distante souhaitée en parallèle, puis en mettant à jour les résultats une fois que la police souhaitée a été téléchargée. 

Pour demander que la police entière soit téléchargée avant d’être utilisée, la méthode [**IDWriteFontFaceReference :: EnqueueFontDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuefontdownloadrequest) peut être utilisée. Si la police est très volumineuse, seule une partie des données peut être nécessaire pour traiter des chaînes particulières. DirectWrite fournit des méthodes supplémentaires qui peuvent être utilisées pour demander des portions des données de police nécessaires à un contenu particulier, [**EnqueueCharacterDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueuecharacterdownloadrequest) et [**EnqueueGlyphDownloadRequest**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference-enqueueglyphdownloadrequest).  

Supposons que l’approche à prendre dans l’application consiste à permettre au traitement d’être effectué initialement à l’aide de polices locales, alternatives ou de secours. La méthode IDWriteFontFallback ::[**MapCharacters**](idwritefontfallback-mapcharacters.md) peut être utilisée pour identifier les polices de secours locales et met automatiquement en file d’attente une requête pour télécharger la police par défaut. en outre, si [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) est utilisé et que tout ou partie du texte de la disposition est mis en forme à l’aide d’une référence de police à distance, DirectWrite utilise automatiquement la méthode **MapCharacters** pour obtenir les polices de secours locales et mettre en file d’attente une requête pour télécharger les données de police distantes. 

DirectWrite gère une file d’attente de téléchargement de polices pour chaque fabrique, et les requêtes effectuées à l’aide des méthodes mentionnées ci-dessus sont ajoutées à cette file d’attente. La file d’attente de téléchargement de la police peut être obtenue à l’aide de la méthode [**IDWriteFactory3 :: GetFontDownloadQueue**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getfontdownloadqueue) . 

Si une demande de téléchargement est effectuée alors que les données de police sont déjà locales, cela aboutit à une absence d’opération : rien n’est ajouté à la file d’attente de téléchargement. Une application peut vérifier si la file d’attente est vide ou s’il y a des demandes de téléchargement en attente en appelant la méthode [**IDWriteFontDownloadQueue :: IsEmpty**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-isempty) . 

Une fois que des demandes de polices distantes ont été ajoutées à la file d’attente, le processus de téléchargement doit être initié. Lorsque des polices distantes sont utilisées dans [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout), le téléchargement est lancé automatiquement quand l’application appelle les méthodes **IDWriteTextLayout** qui forcent les opérations de disposition ou de rendu, telles que les méthodes GetLineMetrics ou Draw. Dans d’autres scénarios, l’application doit lancer le téléchargement directement en appelant [**IDWriteFontDownloadQueue :: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload).  

Une fois le téléchargement terminé, il revient à l’application de prendre les mesures appropriées, en effectuant les opérations en attente ou en répétant les opérations qui ont été effectuées initialement avec les polices de secours. (si la disposition du texte de DirectWrite est utilisée, [**IDWriteTextLayout3 :: InvalidateLayout**](idwritetextlayout3-invalidatelayout.md) peut être utilisé pour effacer les résultats temporaires calculés à l’aide des polices de secours.) Pour que l’application soit notifiée lorsque le processus de téléchargement est terminé et pour prendre les mesures appropriées, l’application doit fournir une implémentation de l’interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) et la transmettre à l’appel BeginDownload. 

> [!IMPORTANT]
> remarque relative à la sécurité et aux performances : lors d’une tentative d’extraction d’une police distante, il n’y a aucune garantie que Windows recevra une réponse du serveur. si le serveur ne répond pas, Windows finit par expirer, mais cela peut prendre plusieurs minutes si plusieurs polices distantes sont récupérées mais échouent. L’appel BeginDownload est retourné immédiatement. Les applications ne doivent pas bloquer l’interface utilisateur en attendant l’appel de [**IDWriteFontDownloadListener ::D ownloadcompleted**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadlistener-downloadcompleted) . 

 

des exemples d’implémentations de ces interactions avec la file d’attente de téléchargement de police de DirectWrite et de l’interface [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) peuvent être vus dans le [DirectWrite exemple de jeux de polices personnalisées](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/), ainsi que dans le [DirectWrite exemple de polices téléchargeables](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont). 

### <a name="creating-a-custom-font-set-using-font-data-loaded-into-memory"></a>Création d’un jeu de polices personnalisé à l’aide des données de police chargées en mémoire

Tout comme les opérations de bas niveau pour la lecture de données à partir d’un fichier de polices sont différentes pour les fichiers sur un disque local et les fichiers distants sur le Web, il en va de même pour les données de police chargées dans une mémoire tampon. une nouvelle interface de bas niveau pour gérer les données de police en mémoire a été ajoutée dans le Windows 10 Creators Update, [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader). 

comme avec un chargeur de fichiers de polices à distance, un chargeur de fichier de police en mémoire doit d’abord être inscrit auprès d’une fabrique de DirectWrite. Le chargeur doit être détenu par l’application tant que les polices qui lui sont associées sont utilisées. Une fois que les polices ne sont plus utilisées, et à un moment donné avant la destruction de la fabrique, le chargeur doit être désinscrit. Cela peut être fait dans le destructeur de la classe qui possède l’objet Loader. Ces étapes sont présentées ci-dessous. 

Si l’application a des informations distinctes sur les visages de police représentées par les données, elle peut ajouter des références de type de police à un générateur de jeu de polices avec des propriétés personnalisées spécifiées. Dans la mesure où les données de police sont dans la mémoire locale, toutefois, cela n’est pas obligatoire. DirectWrite serez en mesure de lire les données directement pour dériver les valeurs de propriété. 

DirectWrite suppose que les données de police sont au format raw, opentype, équivalentes à un fichier opentype (. ttf,. otf,. ttc,. otc), mais en mémoire plutôt que sur le disque. Les données ne peuvent pas être dans un format de conteneur WOFF ou WOFF2. Les données peuvent représenter une collection de polices OpenType. Si les propriétés personnalisées ne sont pas utilisées, la méthode [**IDWriteFontSetBuilder1 :: AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) peut être utilisée pour ajouter toutes les faces de police dans les données en un seul appel. 

Un point important à prendre en compte pour le scénario en mémoire est la durée de vie des données. si un pointeur vers la mémoire tampon est fourni à DirectWrite sans indiquer clairement qu’il existe un propriétaire, DirectWrite fera une copie des données dans une nouvelle mémoire tampon qu’il possédera. Pour éviter la copie de données et l’allocation de mémoire supplémentaire, l’application peut passer un objet de propriétaire de données qui implémente IUnknown et qui possède la mémoire tampon contenant les données de police. en implémentant cette interface, DirectWrite pouvez ajouter au nombre de références de l’objet, garantissant ainsi la durée de vie des données détenues. 

La méthode de création d’un jeu de polices personnalisé à l’aide des données de police en mémoire est la suivante : Cela nécessite la Windows 10 Creators Update. Cela suppose un objet propriétaire de données implémenté par l’application, qui implémente IUnknown et possède également des méthodes qui retournent un pointeur vers la mémoire tampon et la taille de la mémoire tampon. 

<dl> 1. Créez une interface IDWriteFactory5, comme illustré ci-dessus.  
2. Créez une interface [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) , comme illustré ci-dessus.  
3. Utilisez la fabrique pour obtenir un IDWriteInMemoryFontFileLoader. 


```C++
 IDWriteInMemoryFontFileLoader* pInMemoryFontFileLoader; 
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->CreateInMemoryFontFileLoader(&pInMemoryFontFileLoader); 
}
```



Cela retourne une implémentation fournie par le système de l’interface de chargeur de fichier de police en mémoire.   
4. Enregistrez le chargeur de fichier de police en mémoire avec la fabrique. 


```C++
if (SUCCEEDED(hr)) 
{ 
    hr = pDWriteFactory->RegisterFontFileLoader(pInMemoryFontFileLoader); 
}
```



   
5. Pour chaque fichier de police en mémoire, utilisez le chargeur de fichier de police en mémoire pour créer un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile). 


```C++
IDWriteFontFile* pFontFile; 
hr = pInMemoryFontFileLoader->CreateInMemoryFontFileReference( 
    pDWriteFactory, 
    pFontDataOwner->fontData /* returns void* */, 
    pFontDataOwner->fontDataSize /* returns UINT32 */, 
    pFontDataOwner /* ownerObject, owns the memory with font data and implements IUknown */, 
    &pFontFile 
); 
```



   
6. Ajoutez l’objet [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) au générateur de jeu de polices à l’aide de la méthode [**AddFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder1-addfontfile) , comme indiqué ci-dessus.  En cas de besoin, l’application peut créer des objets [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) individuels basés sur le **IDWriteFontFile**, éventuellement définir des propriétés personnalisées pour chaque référence de type de police, puis ajouter la référence de type de police avec des propriétés personnalisées au jeu de polices à l’aide de la méthode [**AddFontFaceReference**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontfacereference(idwritefontfacereference)) , comme indiqué ci-dessus.   
7. Une fois que toutes les polices ont été ajoutées au générateur de jeu de polices, créez le jeu de polices personnalisé, comme indiqué ci-dessus.   
8. À un moment donné, lorsque les polices en mémoire ne seront plus utilisées, annulez l’inscription du chargeur de fichier de police en mémoire. 


```C++
hr = pDWriteFactory->UnregisterFontFileLoader(pInMemoryFontFileLoader);
```



  
</dl>

 

## <a name="advanced-scenarios"></a>Scénarios avancés

Certaines applications peuvent avoir des exigences spéciales qui nécessitent un traitement plus avancé que celui décrit ci-dessus. 

### <a name="combining-font-sets"></a>Combinaison de jeux de polices

Certaines applications peuvent avoir besoin de créer un jeu de polices qui comprend une combinaison d’éléments issus d’autres jeux de polices. Par exemple, une application peut souhaiter créer un jeu de polices qui combine toutes les polices installées sur le système avec une sélection de polices personnalisées, ou qui combine des polices installées correspondant à certains critères avec d’autres polices. DirectWrite possède des api pour prendre en charge la manipulation et la combinaison de jeux de polices. 

Pour combiner deux jeux de polices ou plus, la méthode [**IDWriteFontSetBuilder :: AddFontSet**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontsetbuilder-addfontset) ajoute toutes les polices dans un jeu de polices donné à ajouter à un générateur de jeu de polices en un seul appel. Si seules certaines polices d’un jeu de polices existant sont souhaitées dans le nouveau jeu de polices, la méthode [**IDWriteFontSet :: GetMatchingFonts**](idwritefontset-getmatchingfonts-overload.md) peut être utilisée pour dériver un nouvel objet de jeu de polices qui a été filtré pour inclure uniquement les polices correspondant aux propriétés spécifiées. Ces méthodes offrent un moyen simple de créer un jeu de polices personnalisé combinant des polices à partir de deux jeux de polices ou plus existants. 

### <a name="using-local-woff-or-woff2-font-data"></a>Utilisation des données de police WOFF ou WOFF2 locales

si une application possède des fichiers de polices dans le système de fichiers local ou dans une mémoire tampon, mais qu’elle utilise les formats de conteneur WOFF ou WOFF2, DirectWrite (Windows 10 Creator Update ou version ultérieure) fournit une méthode pour décompresser le format de conteneur, [**IDWriteFactory5 :: UnpackFontFile**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory5-unpackfontfile), qui retourne un [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream). 

Toutefois, l’application doit disposer d’un moyen d’obtenir le [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) dans un objet de chargeur de fichiers de polices. Une façon de procéder consiste à créer une implémentation personnalisée de [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) qui encapsule le flux. Comme avec les autres chargeurs de fichiers de polices, il doit être inscrit avant son utilisation et désinscrit avant que la fabrique ne soit hors de portée.  

Si le chargeur personnalisé est également utilisé avec des fichiers de polices bruts (non compressés), l’application doit également fournir une implémentation personnalisée de l’interface [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) pour la gestion de ces fichiers. Toutefois, il existe des méthodes plus simples pour gérer les fichiers de polices brutes qui utilisent les API abordées ci-dessus. La nécessité d’une implémentation de flux personnalisé peut être évitée en utilisant des chemins de code distincts pour les fichiers de polices compressés et les fichiers de polices brutes. 

Après la création d’un objet de chargeur de fichiers de polices personnalisé, les données compressées du fichier de polices sont ajoutées au chargeur par des moyens spécifiques à l’application. Le chargeur peut gérer plusieurs fichiers de police, chacun d’eux étant identifié à l’aide d’une clé définie par l’application qui est opaque pour DirectWrite. Une fois qu’un fichier de police compressé a été ajouté au chargeur, la méthode [**IDWriteFactory :: CreateCustomFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createcustomfontfilereference) est utilisée pour obtenir un [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) basé sur ce chargeur pour les données de police identifiées par une clé donnée.  

le décompactage réel des données de police peut être effectué à mesure que des polices sont ajoutées au chargeur, mais elles peuvent également être gérées dans la méthode [**IDWriteFontFileLoader :: CreateStreamFromKey**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfileloader-createstreamfromkey) , que DirectWrite appelle lorsqu’il doit d’abord lire les données de police. 

Une fois qu’un objet IDWriteFontFile a été créé, les étapes restantes pour ajouter les polices à un jeu de polices personnalisé sont décrites ci-dessus. 

une implémentation à l’aide de cette approche est illustrée dans la [DirectWrite exemple de jeux de polices personnalisés](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/). 

### <a name="using-directwrite-remote-font-mechanisms-with-custom-low-level-network-implementation"></a>utilisation de DirectWrite mécanismes de police à distance avec une implémentation réseau de bas niveau personnalisée

les mécanismes de DirectWrite pour gérer les polices distantes peuvent être divisés en mécanismes de niveau supérieur, avec des jeux de polices qui incluent des références de type police pour les polices distantes, la vérification de la localité des données de police et la gestion de la file d’attente pour les demandes de téléchargement de polices, ainsi que les mécanismes de niveau inférieur qui gèrent le téléchargement réel. Certaines applications peuvent utiliser les mécanismes de police à distance de niveau supérieur, mais elles nécessitent également des interactions réseau personnalisées, telles que la communication avec les serveurs à l’aide de protocoles autres que HTTP. 

Dans ce cas, une application doit créer une implémentation personnalisée de l’interface [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) qui interagit avec d’autres interfaces de niveau inférieur de la manière requise. L’application doit également fournir des implémentations personnalisées de ces interfaces de niveau inférieur : [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream)et [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult). ces trois interfaces ont des méthodes de rappel que DirectWrite appellera pendant les opérations de téléchargement. 

quand [**IDWriteFontDownloadQueue :: BeginDownload**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontdownloadqueue-begindownload) est appelé, DirectWrite effectue des requêtes au chargeur de fichiers de polices distantes à propos de la localité des données et demande le flux distant. Si les données ne sont pas locales, elle appellera la méthode BeginDownload du flux. l’implémentation de flux ne doit pas bloquer sur cet appel, mais doit retourner immédiatement, en retournant un objet [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) qui fournit le handle d’attente DirectWrite utilisera pour attendre l’opération de téléchargement asynchrone. L’implémentation du flux personnalisé est chargée de gérer la communication à distance. lorsque l’événement d’achèvement s’est produit, DirectWrite appellera [**IDWriteAsyncResult :: GetResult**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwriteasyncresult-getresult) pour déterminer le résultat de l’opération. Si le résultat réussit, il est prévu que les appels ReadFragment suivants au flux pour les plages téléchargées réussiront. 

> [!IMPORTANT]
> Remarque relative à la sécurité et aux performances : lors d’une tentative d’extraction d’une police distante, il est possible qu’un attaquant usurpe l’identité du serveur prévu appelé ou que le serveur ne réponde pas. Si vous implémentez des interactions réseau personnalisées, vous pouvez mieux contrôler les atténuations que lors du traitement des serveurs tiers. Toutefois, il vous revient de prendre en compte les mesures d’atténuation appropriées pour éviter la divulgation d’informations ou le déni de service. Les protocoles sécurisés, tels que HTTPs, sont recommandés. en outre, vous devez créer un délai d’expiration pour que le handle d’événement retourné à DirectWrite soit défini. 

 

### <a name="supporting-scenarios-on-earlier-windows-versions"></a>scénarios de prise en charge des versions antérieures de Windows

les scénarios décrits peuvent être pris en charge dans DirectWrite sur les versions antérieures de Windows, mais nécessitent une implémentation bien plus personnalisée sur la partie de l’application à l’aide des api plus limitées qui étaient disponibles avant Windows 10. pour plus d’informations, consultez [Collections de polices personnalisées (Windows 7/8)](custom-font-collections.md).

 

 