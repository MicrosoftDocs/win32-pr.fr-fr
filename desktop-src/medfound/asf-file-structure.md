---
description: Cette rubrique décrit la structure d’un fichier ASF (Advanced Systems Format).
ms.assetid: 4a817efa-5452-46bf-8921-2ba199c21949
title: Structure de fichiers ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 672067b5f933884326038a93b6d4538c68558856
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413064"
---
# <a name="asf-file-structure"></a>Structure de fichiers ASF

Cette rubrique décrit la structure d’un fichier ASF (Advanced Systems Format).

Pour plus d’informations sur les fichiers ASF, téléchargez la [spécification ASF](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea). vous pouvez également utiliser l’outil [Windows Media ASF Viewer 9 Series](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea) pour voir la structure d’un fichier ASF existant.

L’unité de base de l’Organisation pour les fichiers ASF est appelée un *objet*. Un objet fichier ASF contient les données suivantes.



| Données                                                        | Taille     |
|-------------------------------------------------------------|----------|
| GUID qui identifie l’objet.                          | 128 bits |
| Taille de l'objet.                                     | 64-bits. |
| Données d’objet. Les données d’objet peuvent contenir d’autres objets ASF. | Varie.  |



 

> [!Note]  
> Un objet fichier ASF est simplement un bloc de données. Il ne s’agit pas d’un objet dans le sens de la programmation informatique.

 

Un fichier ASF contient trois types d’objets de fichier de niveau supérieur.



| Objet fichier ASF                                                                                                                      | Description                                          |
|--------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="_Header_Object"></span><span id="_header_object"></span><span id="_HEADER_OBJECT"></span> Objet d’en-tête<br/>         | Contient des informations sur le fichier ASF.<br/>  |
| <span id="Data_Object"></span><span id="data_object"></span><span id="DATA_OBJECT"></span>Objet de données<br/>                     | Contient des paquets de données multimédias.<br/>           |
| <span id="_Index_Object_s_"></span><span id="_index_object_s_"></span><span id="_INDEX_OBJECT_S_"></span> Objet (s) d’index<br/> | Contient un ou plusieurs index. (Facultatif.)<br/> |



 

Le diagramme suivant illustre la structure de fichiers ASF.

![Diagramme montrant la structure des fichiers ASF, y compris les éléments contenus dans l’en-tête, les données et l’index](images/asf-components04.png)

Ce diagramme n’est pas dessiné pour être mis à l’échelle ; en général, l’objet de données comprend la plus grande partie du fichier.

### <a name="header-object"></a>Objet d’en-tête

L’objet d’en-tête est obligatoire et apparaît au début de chaque fichier ASF. Il contient des attributs de fichier globaux et des informations sur les flux dans le fichier ASF. Ces informations permettent d’interpréter et de lire les données contenues dans le fichier.

L’objet Header contient plusieurs sous-objets madatory :

-   L’objet de propriétés de fichier décrit les attributs globaux du fichier, tels que la taille de fichier, la durée de lecture, le nombre de paquets de données, la taille de paquet minimale et maximale et la vitesse de transmission maximale.
-   L’objet d’extension d’en-tête permet d’ajouter des fonctionnalités supplémentaires à un fichier ASF tout en conservant la compatibilité descendante.
-   L’objet de propriétés de flux décrit un flux dans le fichier. Un fichier ASF doit contenir au moins un flux et, par conséquent, au moins un objet de propriétés de flux.

L’objet d’en-tête peut contenir des informations facultatives supplémentaires, y compris des métadonnées sur le fichier (par exemple, titre et auteur), une liste des codecs utilisés pour encoder le fichier et des informations de protection du contenu.

### <a name="data-object"></a>Objet de données

L’objet de données ASF contient toutes les données multimédias du fichier ASF. Cet objet est obligatoire et doit suivre l’objet d’en-tête ASF.

L’objet de données est divisé en *paquets* de données. Chaque paquet contient des données pour un ou plusieurs flux dans le fichier. Un paquet de données contient un en-tête de paquet de données qui fournit des informations d’analyse de paquets, suivies des données de charge utile des données de support numérique réelles. L’heure de la présentation est associée à tous les paquets de données et elles sont organisées dans l’ordre de réception.

Les informations sur le contenu de l’objet de données, telles que la taille du paquet et le nombre de paquets, sont stockées dans l’objet d’en-tête.

### <a name="index-object"></a>Index (objet)

L’objet index est facultatif et est le dernier objet du fichier ASF. Un fichier ASF peut contenir plusieurs objets index. L’objet index fournit un accès aléatoire basé sur le temps à l’objet de données ASF.

Un objet index simple est un autre type d’index.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge ASF dans Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




