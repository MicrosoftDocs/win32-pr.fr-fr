---
description: cette rubrique présente le langage de requête de métadonnées pour le composant WIC (Windows Imaging Component).
ms.assetid: 5ffa0a69-b53d-4be3-b802-deaaa743e6bd
title: Vue d’ensemble du langage de requête de métadonnées
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c69effefd288f13c72239a41c5ace1a518775337cc496a2defa864d179cd6cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668230"
---
# <a name="metadata-query-language-overview"></a>Vue d’ensemble du langage de requête de métadonnées

cette rubrique présente le langage de requête de métadonnées pour le composant WIC (Windows Imaging Component). Vous utilisez le langage de requête de métadonnées pour créer des expressions qui recherchent des données spécifiques (éléments de métadonnées) et des emplacements (blocs de métadonnées) dans les métadonnées d’une image.

Cette rubrique contient les sections suivantes.

-   [Composants requis](#prerequisites)
-   [Introduction](#introduction)
-   [Anatomie d’une expression de chemin d’accès](#anatomy-of-a-path-expression)
    -   [Sélection de bloc](#block-selection)
    -   [Sélection de l’élément](#item-selection)
    -   [Caractère d’échappement](#escape-character)
    -   [Exemples d'expressions](#sample-expressions)
-   [Expressions de stratégie de métadonnées de photo](#photo-metadata-policy-expressions)
-   [Résumé du langage des requêtes de métadonnées](#metadata-query-language-summary)
-   [Rubriques connexes](#related-topics)

## <a name="prerequisites"></a>Prérequis

Pour comprendre cette rubrique, vous devez être familiarisé avec le système de métadonnées WIC, comme décrit dans la [vue d’ensemble des métadonnées WIC](-wic-about-metadata.md) et l’accès aux métadonnées, comme décrit dans [vue d’ensemble de la lecture et de l’écriture de métadonnées d’image](-wic-codec-readingwritingmetadata.md).

## <a name="introduction"></a>Introduction

Vous interagissez avec la plateforme de métadonnées principalement par le biais de deux composants COM (Component Object Model) : un lecteur de requêtes, représenté par l’interface [**IWICMetadataQueryReader**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) , et un générateur de requêtes, représenté par l’interface [**IWICMetadataQueryWriter**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Ces composants vous permettent de lire ou d’écrire des métadonnées à l’aide du langage de requête de métadonnées. Le langage de requête décrit la syntaxe d’une expression de chemin d’accès et les composants de requête utilisent cette expression de chemin d’accès pour accéder aux métadonnées souhaitées. Cette expression de chemin d’accès décrit l’emplacement d’un bloc ou d’un élément de métadonnées.

Un bloc de métadonnées est un groupe nommé de métadonnées dans un format spécifique. Un bloc de métadonnées peut contenir des éléments de métadonnées individuels tels que l’auteur ou l’heure de création, ainsi que des blocs de métadonnées supplémentaires. Le nom d’un bloc de métadonnées est déterminé par son format. Par exemple, un bloc de métadonnées contenant des métadonnées App1 serait nommé « App1 ». Les formats de métadonnées courants incluent App1, EXIF, IFD et XMP.

Un élément de métadonnées est une paire nom/valeur qui décrit des caractéristiques telles que l’auteur, le titre et l’évaluation.

Une expression de chemin d’accès contient un ou plusieurs noms de blocs de métadonnées. Il peut également spécifier un élément de métadonnées dans un bloc de métadonnées. L’expression de chemin d’accès suivante représente un bloc App1 qui contient un bloc IFD contenant l’élément de métadonnées :

-   /App1/IFD/{UShort = 18249}

Le diagramme suivant illustre la composition d’un exemple d’image JPEG avec quatre blocs de métadonnées racine : APP0, App1, XMP et un bloc inconnu. Chaque élément en surbrillance note le type de métadonnées (bloc ou élément) et l’expression de requête utilisée pour récupérer les données.

![image JPEG avec des légendes de métadonnées](graphics/jpegwithcallouts.png)

> [!Note]  
> Le contenu de ce diagramme est référencé dans ce document et utilisé dans la plupart des exemples.

 

## <a name="anatomy-of-a-path-expression"></a>Anatomie d’une expression de chemin d’accès

Pour accéder aux métadonnées à l’aide des API WIC, une expression de requête complète doit être utilisée dans la plupart des cas. Cette rubrique traite des expressions qualifiées complètes pour l’accès aux métadonnées. Si vous avez besoin d’informations sur les cas d’utilisation d’expressions non complètes, reportez-vous à la section expression de stratégie de métadonnées de photo plus loin dans ce document.

Qu’est-ce qu’une expression de requête complète ? Dans WIC, une expression qualifiée complète est une chaîne qui commence par la barre oblique de caractères de chemin d’accès (/), suivie d’un chemin de navigation vers un bloc de métadonnées ou un élément de métadonnées spécifique. Chaque étape du chemin de navigation est séparée par une barre oblique, formant une expression permettant d’accéder à un bloc de métadonnées ou à un élément de métadonnées. Par exemple, voici une expression de requête complète qui accède à l’évaluation de photo Microsoft dans un bloc IFD imbriqué dans un bloc App1 :

-   /App1/IFD/{UShort = 18249}

Lorsque WIC analyse cette expression, il recherche d’abord le bloc de métadonnées App1 dans les métadonnées de l’image. Si le bloc App1 est trouvé, il poursuit sa recherche en recherchant le bloc de métadonnées IFD imbriqué. Si le bloc IFD est trouvé, il recherche l’élément de métadonnées spécifique, dans ce cas l’évaluation MicrosoftPhoto sous la balise 18249, dans le bloc de métadonnées IFD. Si, à un moment donné, WIC ne trouve pas de bloc ou d’élément de métadonnées, il abandonne la requête.

### <a name="block-selection"></a>Sélection de bloc

L’expression de requête de métadonnées WIC la plus simple est une expression pour obtenir un enregistreur/lecteur de requête pour un bloc de métadonnées spécifique. L’obtention d’un enregistreur/lecteur de requête vous permet de diriger directement les requêtes suivantes vers un bloc de métadonnées imbriqué sans avoir à gérer son bloc parent. Une expression de requête de sélection de bloc est un chemin de navigation vers le bloc de métadonnées souhaité. Par exemple, dans l’illustration précédente, il y a cinq blocs de métadonnées, dont deux sont imbriqués dans d’autres blocs de métadonnées. Voici les expressions de chemin d’accès à chaque bloc de métadonnées dans l’exemple JPEG :

-   /app0
-   /App1
-   /app1/ifd
-   /app1/ifd/exif
-   /xmp

Lorsque vous utilisez une requête de lecture/écriture pour exécuter une requête, elle retourne un nouveau lecteur/enregistreur de requête qui permet de servir des requêtes dans la portée du bloc de métadonnées spécifié. Par exemple, si vous exécutez la requête « /App1 », un nouveau lecteur de requête est obtenu et les requêtes vers le nouveau lecteur sont relatives au bloc App1. Cela signifie que la requête « /IFD » est valide pour le nouveau lecteur, car le bloc App1 contient un bloc IFD. Toutefois, « /XMP » ne fonctionne pas, car ce bloc App1 ne contient pas de bloc de métadonnées XMP.

Le langage de requête prend également en charge une notation d’index. La notation d’index donne accès à un bloc de métadonnées spécifique lorsque plusieurs blocs du même type existent. Pour l’exemple JPEG, l’expression de chemin d’accès indexée suivante peut être utilisée :

-   /\[0 \] App1/ \[ 0 \] IFD

Dans le langage de requête, tous les index commencent à zéro. Dans l’expression précédente, les premières requêtes portant sur le premier bloc App1 et la deuxième valeur zéro interrogent le premier bloc IFD imbriqué. La notation d’index peut toujours être utilisée même lorsque plusieurs blocs du même type n’existent pas. Si l’exemple JPEG incluait un deuxième bloc App1 avec un bloc IFD incorporé, l’expression « / \[ 1 \] App1/IFD » serait utilisée pour accéder au deuxième bloc App1.

La notation d’index devient plus courante lors du traitement des blocs de texte PNG, car il est probable que l’image PNG aura plusieurs blocs de texte.

> [!Note]  
> Les index de tableau multidimensionnel ne sont pas pris en charge.

 

### <a name="item-selection"></a>Sélection de l’élément

Vous pouvez accéder aux éléments de métadonnées dans un bloc de métadonnées en générant sur les expressions de sélection de bloc. Considérez les propriétés XMP et Microsoft Photo Rating dans l’exemple JPEG. Ces métadonnées existent dans deux blocs de métadonnées : les blocs App1/IFD et XMP. Par conséquent, plusieurs expressions peuvent être utilisées pour accéder aux mêmes données. L’expression suivante accède à l’évaluation MicrosoftPhoto dans le bloc XMP :

-   /XMP/XMP : évaluation

La partie « XMP : » de l’expression est un identificateur convivial de schéma. XMP est une norme extensible qui permet aux entités tierces de publier leurs propres schémas qui définissent le mode de stockage de certains éléments de métadonnées. Un schéma XMP est entièrement identifié par une URL, mais WIC fournit un ensemble d’identificateurs conviviaux pour les schémas bien connus. Pour plus d’informations, consultez la rubrique [requêtes de métadonnées de format d’image native](-wic-native-image-format-metadata-queries.md) .

Pour les images JPEG, les informations d’évaluation peuvent également être stockées dans le bloc IFD imbriqué App1. Toutefois, contrairement à l’exemple d’évaluation XMP, le bloc IFD n’utilise pas de nom de schéma pour accéder aux informations d’évaluation. Vous utilisez une expression de données à la place. L’expression suivante est utilisée pour accéder à l’évaluation MicrosoftPhoto dans le bloc IFD imbriqué App1 :

-   /App1/IFD/{UShort = 18249}

Dans cette expression, la partie « /App1/IFD » de l’expression est le chemin de navigation vers le bloc IFD (comme indiqué précédemment dans la section sélection de bloc). La deuxième partie de l’expression « /{UShort = 18249} » accède aux données. Cette partie de l’expression indique à l’analyseur de requête de rechercher les données incorporées dans la balise short non signée qui a l’identificateur de balise 18249.

> [!Note]  
> Pour obtenir la liste des formats de métadonnées courants pris en charge par chaque format d’image, consultez la rubrique [requêtes de métadonnées de format d’image native](-wic-native-image-format-metadata-queries.md) .

 

{UShort = 18249} est une expression de données et peut prendre plusieurs formes. Une expression de données est une expression en deux parties contenant la balise ou la clé de métadonnées demandée, dans ce cas « 18249 », et le type de données de la clé, dans ce cas « UShort ». Les deux parties sont séparées par un signe égal (=). WICsupports la majorité des types de données C/C++ courants. Les types de données suivants sont acceptés par le langage de requête :

-   char
-   UCHAR
-   short
-   ushort
-   long
-   ulong
-   int
-   uint
-   longlong
-   float
-   double
-   str
-   WSTR
-   guid
-   bool

> [!Note]  
> Cette liste spécifie uniquement les types de données pris en charge par le langage de requête de métadonnées. Utilisez ces types de données lors de la création d’une expression de données de requête de métadonnées telle que {UShort = 18249}. Le WIC retourne la valeur de l’élément de métadonnées sous la forme de PROPVARIANT, qui définit son propre système de type.

 

Dans l’exemple, « 18249 » est la balise de données. Ce nombre particulier est défini par Microsoft pour contenir l’évaluation MicrosoftPhoto. La balise de données peut être un nombre, une chaîne ou un GUID en fonction de l’élément de données que vous recherchez.

Contrairement à l’exemple d’évaluation XMP, il n’existe aucune collision de nom pour la valeur d’évaluation dans le bloc App1/IFD. Cela est dû au fait que la valeur d’évaluation XMP est stockée sous une autre balise UShort, 18246. Ainsi, l’expression permettant d’accéder à l’évaluation XMP dans le bloc App1/IFD est la suivante :

-   /App1/IFD/{UShort = 18246}

> [!Note]  
> Pour obtenir une description formelle du langage de requête de métadonnées, consultez la section Résumé du langage de requête de métadonnées plus loin dans ce document.

 

### <a name="escape-character"></a>Caractère d'échappement

Le langage de requête ne tient pas compte de la casse et traite tous les caractères en minuscules. Toutefois, certains formats de métadonnées (tels que XMP) respectent la casse. Lorsque vous utilisez un format de métadonnées respectant la casse, utilisez la barre oblique inverse ( \\ ) lorsque vous souhaitez spécifier un caractère majuscule.

Le caractère d’échappement est consommé par l’analyseur de langage et le caractère suivant qui le suit est interprété directement. Par exemple, l’expression {char = \\ \\ } est résolue en tant que' \\ 'et {char = \\ C} est résolu en tant que C majuscule. Sans le caractère d’échappement, {char = \\ } est une expression non valide et {char = C} est interprété comme un C minuscule. Veillez à utiliser le caractère d’échappement barre oblique inverse avant toutes les lettres majuscules dans les formats de métadonnées qui respectent la casse.

### <a name="sample-expressions"></a>Exemples d'expressions

Le tableau suivant fournit des exemples d’expressions et des descriptions de leurs interprétations par l’analyseur de langage de requête. 

| Expression                     | Description                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| IFD/XMP/EXIF : auteur            | Correspond au chemin de navigation suivant : bloc « IFD » > bloc XMP-> propriété « auteur » dans le schéma « EXIF ».                                                                                                                                                                                                                                            |
| /\[1 \] IFD/ \[ 0 \] XMP/EXIF : auteur | Identique au premier élément de ce tableau, sauf que le \[ \# \] préfixe décrit l’élément à parcourir en cas de collision de nom.                                                                                                                                                                                                                                |
| /IFD/{UShort = 700}/Author       | Identique au premier élément de ce tableau, sauf qu’il utilise une expression de données pour référencer le bloc XMP au lieu du nom de bloc « XMP » (le bloc XMP est incorporé sous l’identificateur de balise abrégé non signé 700). En outre, la propriété « Author » ne spécifie pas de schéma. L’analyseur de requêtes essaiera de faire correspondre la propriété à tous les schémas et de retourner la première correspondance. |
| /ifd/xmp                       | Fournit un chemin de navigation vers un bloc de métadonnées. Si le bloc est trouvé, un nouveau lecteur/enregistreur de métadonnées est retourné.                                                                                                                                                                                                                                                 |
| /\[\*\]Texte/mot clé            | Obtient ou définit la propriété de mot clé pour un bloc PNG. Étant donné que la spécification de métadonnées png autorise plusieurs segments d’un type particulier, la \[ \* \] notation Obtient/définit le segment de données png avec la propriété appropriée. Conformément à la spécification PNG, deux blocs ne peuvent pas avoir les mêmes propriétés.                                                                |



 

Chaque bloc de métadonnées est également identifié de façon unique par le GUID de métadonnées qui peut être utilisé à la place du nom de bloc convivial. La syntaxe suivante peut être utilisée à la place de la fourniture de noms de bloc : « /{GUID = GUID}/ \[ n \] {GUID = GUID}/Schema : tagidentifier »

Le tableau suivant fournit des exemples non valides et les raisons pour lesquelles elles seraient rejetées. 

| Expression non valide         | Description du rejet                                                                                                                                                  |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /IFD/ \[ 0 \] \[ 2 \] EXIF/       | Rejeté, car les index de tableau multidimensionnels ne sont pas pris en charge.                                                                                                    |
| /IFD/{UShort = 1}/{UShort = 2} | Rejeté, à moins que l’IFD ait un tagID = 1, qui est un gestionnaire de métadonnées contenant un élément de métadonnées avec un tagID = 2.                                                        |
| /{UShort = 1}                | Rejeté si le traitement de la requête est relatif à un niveau supérieur de la hiérarchie de métadonnées. Cela est dû au fait que le niveau supérieur contient uniquement des blocs de métadonnées et non des éléments de données. |



 

## <a name="photo-metadata-policy-expressions"></a>Expressions de stratégie de métadonnées de photo

Comme indiqué précédemment, une expression de requête complète commence par une barre oblique (/). Les expressions qui ne commencent pas par la barre oblique sont évaluées en tant qu’expressions de stratégie. une expression de stratégie vous permet d’interroger les métadonnées de la photo pour les propriétés de l' [interpréteur](https://msdn.microsoft.com/library/ms788673(VS.85).aspx)de Windows relatives aux images. Dans la section de sélection des données, plus haut dans ce document, l’expression « /XMP/XMP : Rating » a été utilisée pour accéder à la propriété d’évaluation XMP. Cette propriété peut également être interrogée à l’aide de l’expression de stratégie suivante :

-   System. SimpleRating

Pour accéder à la propriété Rating à partir du schéma MicrosoftPhoto, vous pouvez utiliser l’expression de requête suivante :

-   System. Rating

Les expressions de stratégie de métadonnées de photos se comportent différemment des requêtes de métadonnées complètes, en quelques points.

Tout d’abord, lors de l’accès aux métadonnées à l’aide d’une expression de stratégie, WIC effectue une résolution d’arbitrage et de conflit dans le cas où la même propriété est disponible dans plusieurs blocs de métadonnées. Par exemple, les valeurs d’évaluation MicrosoftPhoto et XMP sont stockées à la fois dans le bloc App1/IFD et dans le bloc XMP. La stratégie de métadonnées de photos détermine la précédence pour laquelle la valeur de bloc est retournée lors de la lecture des métadonnées. Lorsque vous écrivez des métadonnées, la stratégie de métadonnées de photos garantit que les mêmes propriétés dans différents blocs sont cohérentes. Si vous utilisez une requête de métadonnées telle que « /XMP/XMP : Rating », vous êtes responsable de l’arbitrage entre les différents emplacements de métadonnées.

> [!Note]  
> Pour obtenir la liste des expressions de stratégie prises en charge et leurs stratégies de mappage, consultez la rubrique [stratégies de métadonnées de photos](photo-metadata-policies.md) .

 

Deuxièmement, les expressions de stratégie de métadonnées de photo sont indépendantes du format d’image, contrairement aux requêtes de métadonnées complètes. Par exemple, la requête « /XMP/XMP : Rating » est spécifique au format JPEG. Les images TIFF prennent également en charge les métadonnées XMP, mais elles sont stockées différemment par rapport au format JPEG, de sorte que la requête TIFF serait « /IFD/XMP/XMP : Rating ». Toutefois, dans les deux cas, l’expression de stratégie serait « System. SimpleRating ».

Les expressions de stratégie de métadonnées de photos fournissent un niveau supérieur d’abstraction et de simplicité par rapport aux requêtes de métadonnées complètes, et devraient donc être préférées dans les cas où l’accès aux métadonnées de bas niveau n’est pas nécessaire. Toutefois, les expressions de stratégie fournissent uniquement un accès à un ensemble limité de métadonnées d’image, tandis que le langage de requête de métadonnées permet d’accéder à presque toutes les métadonnées stockées dans un fichier image.

## <a name="metadata-query-language-summary"></a>Résumé du langage des requêtes de métadonnées

Le tableau suivant est une définition formelle du langage de requête de métadonnées WIC. Chaque symbole de grammaire représente une expression composée d’autres symboles. L’expression peut être un autre symbole ou une séquence d’autres symboles séparés par une barre verticale ( \| ), indiquant un choix « ou ». L’expression entière à droite est une substitution possible pour le symbole spécifié sur la gauche. 

| Symbole                   | Expression                                                                                                                                                                  |
|--------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<path>             | \<name> \| '/' \<property path>                                                                                                                                   |
| \<property path>    | \<metadata item> \| \<property path> '/' \<property path>                                                                                                    |
| \<metadata item>    | \<index name> \| \<item name> \| \<schema name> ':' \<item name>                                                                                        |
| \<schema name>      | \<item name>                                                                                                                                                           |
| \<item name>        | \<metadata item> \| <indexed item><index>                                                                                                                  |
| \<indexed item>     | \<item> \| \<implied metadata>\<item>                                                                                                                        |
| \<implied metadata> | ' < ' \<name> ' > '                                                                                                                                                    |
| \<item>             | \<name> \| \<index> \<data> \| \<data>                                                                                                                  |
| \<data>             | '{' \<data type> '=' \<value> '}'                                                                                                                                 |
| \<index>            | '\[' \<number> \| \<star> '\]'                                                                                                                                    |
| \<data type>        | 'Char' \| 'UCHAR' \| 'short' ' \| UShort' \| 'long' \| 'ulong' \| 'int' \| 'uint' \| 'LongLong' \| 'ULONGLONG' \| 'float' ' \| double' \| 'str' ' \| WSTR' \| 'GUID' \| 'bool' |
| \<data value>       | \<number> \| \<name> \| \<guid>                                                                                                                              |
| \<star>             | '\*'                                                                                                                                                                        |
| \<number>           | nombre                                                                                                                                                                      |
| \<name>             | string                                                                                                                                                                      |
| \<guid>             | guid                                                                                                                                                                        |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Windows Vue d’ensemble du composant de création d’images](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Vue d’ensemble des métadonnées WIC](-wic-about-metadata.md)
</dt> <dt>

[Vue d’ensemble de la lecture et de l’écriture des métadonnées d’image](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Vue d’ensemble de l’extensibilité des métadonnées](-wic-codec-metadatahandlers.md)
</dt> <dt>

[Comment : recoder une image JPEG avec des métadonnées](-wic-codec-jpegmetadataencoding.md)
</dt> </dl>

 

 



