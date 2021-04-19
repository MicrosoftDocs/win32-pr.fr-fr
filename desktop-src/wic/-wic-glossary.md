---
description: Définit les termes utilisés dans WIC.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: b066757a-8841-4976-b20b-989ebba5eb3b
title: Glossaire du composant de création d’images Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee6812024571727c8f769df88f8233119eed13ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522084"
---
# <a name="windows-imaging-component-glossary"></a>Glossaire du composant de création d’images Windows

## <a name="b"></a>B

<dl> <dt>

**profondeur de bit**
</dt> <dd>

Nombre de valeurs de couleur qui peuvent être affectées à un seul pixel dans une image. La profondeur des couleurs peut être comprise entre 1 bit (noir et blanc) et 32 bits (plus de 16,7 millions couleurs). Voir aussi : profondeur de couleur

</dd> <dt>

**bits par pixel (BPP)**
</dt> <dd>

Nombre de bits représentant la valeur de couleur de chaque pixel dans une image numérisée. Voir aussi : BPP

</dd> </dl>

## <a name="c"></a>C

<dl> <dt>

**Clipper**
</dt> <dd>

Objet IWICBitmapClipper.

</dd> <dt>

**Codec**
</dt> <dd>

Filtre qui compresse (encode) ou décompresse (décode) un flux de données.

</dd> <dt>

**contexte de couleur**
</dt> <dd>

Abstraction d’un profil de couleurs. Le profil peut être chargé à partir d’un fichier (par ex. « sRGB Color Space Profile. ICM ») ou à partir d’une mémoire tampon obtenue en lisant. Les informations de contexte de couleur sont définies par l’interface IWICColorContext pour WIC et sont récupérées avec la méthode GetColorContext.

</dd> <dt>

**transformation de couleur**
</dt> <dd>

Mappage des couleurs du contexte de couleur source au contexte de couleur de destination dans un format de pixel de sortie donné.

</dd> <dt>

**Modèle de couleurs CYMK**
</dt> <dd>

Espace colorimétrique multidimensionnel constitué des intensités cyan, magenta, jaune et noir qui composent une couleur donnée.

</dd> </dl>

## <a name="d"></a>D

<dl> <dt>

**décodeur**
</dt> <dd>

Voir le terme : codec

</dd> </dl>

## <a name="e"></a>E

<dl> <dt>

**codeur**
</dt> <dd>

Voir le terme : codec

</dd> </dl>

## <a name="l"></a>L

<dl> <dt>

**perte**
</dt> <dd>

Type de compression qui garantit que les données d’origine peuvent être récupérées exactement, sans perte de qualité d’image.

</dd> <dt>

**pertes**
</dt> <dd>

Processus de compression des données dans laquelle les informations jugées inutiles sont supprimées et ne peuvent pas être récupérées lors de la décompression. Généralement utilisé avec les données audio et visuelles dans lesquelles une légère dégradation de la qualité est acceptable.

</dd> </dl>

## <a name="m"></a>M

<dl> <dt>

**cloisonnement multithread (MTA)**
</dt> <dd>

Forme de multithread prise en charge par le modèle COM (Component Object Model). Dans un modèle à cloisonnement multithread, tous les threads du processus qui ont été initialisés en tant que threads libres résident dans un seul cloisonnement.

</dd> </dl>

## <a name="n"></a>N

<dl> <dt>

**format de pixel natif**
</dt> <dd>

L’un des formats de pixel fournis par WIC, où la disposition de la mémoire de chaque pixel dans une image bitmap est décrite.

</dd> </dl>

## <a name="p"></a>P

<dl> <dt>

**palette**
</dt> <dd>

Ensemble de couleurs utilisé par un objet ou une application.

</dd> <dt>

**stratégie de métadonnées de photos**
</dt> <dd>

Stratégie Windows pour la lecture, l’écriture et la suppression des métadonnées d’image.

</dd> <dt>

**format de pixel**
</dt> <dd>

Taille et disposition des composants de couleur de pixel en mémoire. Elle est spécifiée par le nombre total de bits utilisés par pixel et par le nombre de bits utilisés pour stocker les composants rouge, vert, bleu et alpha de la couleur. Par exemple, le format de pixel RGB24 utilise 24 bits pour stocker une couleur de pixel, avec huit bits chacun pour le rouge, le vert et le bleu. Le format de pixel ARGB32 utilise 32 bits, avec 24 bits d’informations de couleur et 8 bits d’informations de canal alpha.

</dd> <dt>

**décodage progressif**
</dt> <dd>

Processus de décodage d’images qui ont été encodées avec des informations sur les différents niveaux de décodage.

</dd> </dl>

## <a name="s"></a>S

<dl> <dt>

**train**
</dt> <dd>

Fait référence à une interface COM IStream qui peut être utilisée pour lire ou écrire des données séquentiellement dans des fichiers, de la mémoire ou des emplacements réseau.

</dd> </dl>

## <a name="t"></a>T

<dl> <dt>

**courbe tonale**
</dt> <dd>

Graphique utilisé dans la photographie numérique qui affiche la plage tonale de l’image.

</dd> </dl>

## <a name="w"></a>W

<dl> <dt>

**Composant Imagerie Windows (WIC)**
</dt> <dd>

Plateforme extensible qui fournit une API de bas niveau pour les images numériques.

</dd> </dl>

 

 



