---
title: Interfaces DirectWrite
description: Répertorie les interfaces définies par DirectWrite.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite, interfaces
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff423289eb76a3506edb3537875a99a364be457
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588034"
---
# <a name="directwrite-interfaces"></a>Interfaces DirectWrite

DirectWrite définit les interfaces suivantes.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Représente le résultat d’une opération asynchrone. Un client peut utiliser l’interface pour attendre que l’opération se termine et obtenir le résultat.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, que vous pouvez utiliser pour restituer des glyphes. |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | Encapsule une bitmap indépendante du périphérique 32 bits et un contexte de périphérique, qui peut être utilisé pour le rendu des glyphes. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Cette interface permet à l’application d’énumérer les exécutions de glyphes de couleurs. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Énumérateur pour une collection ordonnée de glyphes de couleurs. |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Utilisé pour créer tous les objets DirectWrite suivants. Cette interface est l’interface de fabrique racine pour tous les objets DirectWrite. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | Interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory2**](idwritefactory2.md) | Interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | Interface de fabrique racine pour tous les objets [DirectWrite](direct-write-portal.md) . |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | Interface de fabrique racine pour tous les objets DirectWrite. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | Interface de fabrique racine pour tous les objets DirectWrite. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Représente un objet de fabrique à partir duquel tous les objets DirectWrite sont créés. **IDWriteFactory6** ajoute de nouvelles fonctionnalités pour travailler avec les polices et les ressources de police. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Cette interface représente un objet de fabrique à partir duquel tous les objets DirectWrite sont créés. **IDWriteFactory7** ajoute de nouvelles fonctionnalités pour travailler avec les polices système. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Représente une police physique dans une collection de polices. Cette interface est utilisée pour créer des visages de polices à partir de polices physiques, ou pour récupérer des informations telles que les métriques de type police ou les noms de police des visages de police existants. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Représente une police physique dans une collection de polices. |
| [**IDWriteFont2**](idwritefont2.md) | Représente une police physique dans une collection de polices. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Représente une police dans une collection de polices. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Objet qui encapsule un ensemble de polices, telles que le jeu de polices installées sur le système ou le jeu de polices dans un répertoire particulier. L’API de collection de polices peut être utilisée pour découvrir les familles de polices et les polices disponibles, et pour obtenir des métadonnées sur les polices. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Objet qui encapsule un ensemble de polices, telles que le jeu de polices installées sur le système ou le jeu de polices dans un répertoire particulier. L’API de collection de polices peut être utilisée pour découvrir les familles de polices et les polices disponibles, et pour obtenir des métadonnées sur les polices. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Cette interface encapsule un ensemble de polices, telles que l’ensemble de polices installées sur le système ou l’ensemble de polices d’un répertoire particulier. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Cette interface encapsule un ensemble de polices, telles que l’ensemble de polices installées sur le système ou l’ensemble de polices d’un répertoire particulier. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Utilisé pour construire une collection de polices en fonction d’un type particulier de clé.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Interface de rappel définie par l’application qui reçoit les notifications de la file d’attente de téléchargement de polices (interface [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) ). Les rappels se produisent sur le thread de téléchargement, et les objets doivent être préparés pour gérer les appels sur leurs méthodes à tout moment à partir d’autres threads. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Interface qui met en file d’attente les demandes de téléchargement pour les polices, les caractères, les glyphes et les fragments de police distants.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Cette interface expose diverses données de police, telles que les métriques, les noms et les contours de glyphe. Il contient le type de police, les références de fichier appropriées et les données d’identification de visage. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Contient le type de police, les références de fichier appropriées et les données d’identification de visage.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Cette interface contient le type de police, les références de fichier appropriées et les données d’identification de visage. Elle ajoute la possibilité de vérifier si un chemin de rendu des couleurs est potentiellement nécessaire.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Contient le type de police, les références de fichier appropriées et les données d’identification de visage. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Contient le type de police, les références de fichier appropriées et les données d’identification de visage. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Cette interface contient le type de police, les références de fichier appropriées et les données d’identification de visage. Il ajoute de nouvelles fonctionnalités telles que la comparaison de deux visages de police, la récupération des valeurs d’axe des polices et la récupération de la ressource de police sous-jacente. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Représente une référence à un type de police. Référence identifiant de façon unique à une police, à partir de laquelle vous pouvez créer un type de police pour interroger les métriques de police et les utiliser pour le rendu. Une référence de type de police se compose d’un fichier de police, d’un index de type de police et d’une simulation de type de police. Il se peut que les données du fichier soient physiquement présentes sur l’ordinateur local.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Représente une référence à un type de police. Référence identifiant de façon unique à une police, à partir de laquelle vous pouvez créer un type de police pour interroger les métriques de police et les utiliser pour le rendu. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Vous permet d’accéder aux polices de secours à partir de la liste police. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Vous permet de créer des mappages de substitution de police Unicode et de créer une police qui revient à l’objet de ces mappages. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Représente une famille de polices associées. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Représente une famille de polices associées. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Représente une famille de polices associées. **IDWriteFontFamily2** ajoute de nouvelles fonctionnalités, notamment la récupération des polices par valeurs d’axe des polices. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Représente un fichier de polices. Les applications telles que les gestionnaires de polices ou les visionneuses de polices peuvent appeler [**IDWriteFontFile :: Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) pour déterminer si un fichier particulier est un fichier de police et s’il s’agit d’un type de police pris en charge par le système de police. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Encapsule une collection de fichiers de polices. Le système de polices utilise cette interface pour énumérer les fichiers de polices lors de la génération d’une collection de polices. |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Gère le chargement des ressources de fichier de police d’un type particulier à partir d’une clé de référence de fichier de police dans un objet de flux de fichier de police.  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Charge des données de fichier de police à partir d’un chargeur de fichier de polices personnalisé.  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Représente une liste de polices. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Représente une liste de polices. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Représente une liste de polices. **IDWriteFontList2** ajoute de nouvelles fonctionnalités, notamment la récupération du jeu de polices sous-jacent utilisé par la liste. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Représente un jeu de polices. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Représente un jeu de polices. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Représente un jeu de polices. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Représente un jeu de polices. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Contient des méthodes pour générer un jeu de polices. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Contient des méthodes pour générer un jeu de polices. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Contient des méthodes pour générer un jeu de polices. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Fournit l’interopérabilité avec GDI, comme les méthodes permettant de convertir un type de police en une structure LOGFONT ou de convertir une description de police GDI en une police de police. Il est également utilisé pour créer des objets cibles de rendu bitmap. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Fournit l’interopérabilité avec GDI, comme les méthodes permettant de convertir un type de police en une structure LOGFONT ou de convertir une description de police GDI en une police de police. Il est également utilisé pour créer des objets cibles de rendu bitmap. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md) est un **typedef** de l’interface [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . Pour plus d’informations, consultez la page de référence de [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) . |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Contient les informations de bas niveau utilisées pour restituer une exécution de glyphe. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Encapsule un graphique Inline défini par l’application, ce qui permet à DWrite d’interroger les mesures comme si le graphique était un glyphe en ligne avec le texte. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Représente un chargeur de fichier de police qui peut accéder aux polices en mémoire. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Implémentation intégrée de l’interface [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) , qui opère sur des fichiers de polices locales et expose des informations de fichier de police locale à partir de la clé de référence du fichier de police. Les références de fichiers de polices créées à l’aide de [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) utilisent ce chargeur de fichier de police. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Représente une collection de chaînes indexées par nom de paramètres régionaux. |
| [**IDWriteNumberSubstitution**](./idwritenumbersubstitution.md) | Contient les chiffres et la ponctuation numériques appropriés pour les paramètres régionaux spécifiés. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Définit les propriétés d’accrochage des pixels, telles que les pixels par DIP (pixel indépendant du périphérique) et la matrice de transformation actuelle d’un convertisseur de texte. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Représente un chargeur de fichiers de polices qui peut accéder à des polices distantes (par exemple, téléchargeables).  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Représente un flux de fichier de police dont les parties peuvent être non locales.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Représente des paramètres de rendu de texte tels que le niveau ClearType, le contraste amélioré et la correction gamma pour la pixellisation et le filtrage de glyphes. Une application obtient généralement un objet de paramètres de rendu en appelant la méthode [**IDWriteFactory :: CreateMonitorRenderingParams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) . |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Représente les paramètres de rendu de texte pour la pixellisation et le filtrage de glyphes. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Représente les paramètres de rendu de texte pour la pixellisation et le filtrage de glyphes. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Représente les paramètres de rendu de texte pour la pixellisation et le filtrage de glyphes. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Représente une collection de chaînes indexées par nombre. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Cette interface est implémentée par le client de l’analyseur de texte pour recevoir la sortie d’une analyse de texte donnée.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Interface que vous implémentez pour recevoir la sortie des analyseurs de texte. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Implémenté par le client de l’analyseur de texte pour fournir du texte à l’analyseur. Elle permet la séparation entre la vue logique du texte en tant que flux continu de caractères identifiables par les positions de texte uniques et la disposition réelle de la mémoire des blocs de texte potentiellement discrets dans le magasin de stockage du client.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | L’interface que vous implémentez pour fournir les informations nécessaires à l’analyseur de texte, comme le texte et les propriétés de texte associées. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analyse diverses propriétés de texte pour le traitement complexe des scripts, tels que la prise en charge bidirectionnelle (bidirectionnel) pour les langages tels que l’arabe, la détermination des opportunités de saut de ligne, le placement de glyphes et la substitution de nombres. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analyse diverses propriétés de texte pour le traitement complexe des scripts. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analyse diverses propriétés de texte pour le traitement complexe des scripts. |
| [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | L’interface [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte, et elle décrit les informations relatives aux paramètres régionaux.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Décrit les propriétés de police et de paragraphe utilisées pour mettre en forme le texte et décrit les informations relatives aux paramètres régionaux. |
| [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | L’interface [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) représente un bloc de texte une fois qu’elle a été entièrement analysée et mise en forme. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Représente un bloc de texte une fois qu’il a été entièrement analysé et mis en forme.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Représente un ensemble de rappels définis par l’application qui effectuent le rendu du texte, les objets inline et les décorations telles que les traits de soulignement. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Représente un ensemble de rappels définis par l’application qui effectuent le rendu du texte, les objets inline et les décorations telles que les traits de soulignement.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Représente un paramètre de typographie de police. |