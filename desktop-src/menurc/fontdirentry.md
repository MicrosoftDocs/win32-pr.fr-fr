---
title: FONTDIRENTRY, structure
description: Contient des informations sur une police individuelle dans un groupe de ressources de polices. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Menus de la structure FONTDIRENTRY et autres ressources
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886739"
---
# <a name="fontdirentry-structure"></a>FONTDIRENTRY, structure

Contient des informations sur une police individuelle dans un groupe de ressources de polices. La définition de structure fournie ici est fournie à des fins d’explication uniquement. Il n’est présent dans aucun fichier d’en-tête standard.

## <a name="syntax"></a>Syntaxe


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>Membres

<dl> <dt>

**dfVersion**
</dt> <dd>

Type : **Word**

</dd> <dd>

Numéro de version défini par l’utilisateur pour les données de ressources que les outils peuvent utiliser pour lire et écrire des fichiers de ressources.

</dd> <dt>

**dfSize**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Taille du fichier, en octets.

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Type : **char**

</dd> <dd>

Informations de copyright du fournisseur de polices.

</dd> <dt>

**dfType**
</dt> <dd>

Type : **Word**

</dd> <dd>

Type de fichier de polices.

</dd> <dt>

**dfPoints**
</dt> <dd>

Type : **Word**

</dd> <dd>

Taille en points à laquelle ce jeu de caractères ressemble le mieux.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Type : **Word**

</dd> <dd>

Résolution verticale, en points par pouce, à laquelle ce jeu de caractères a été numérisé.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Type : **Word**

</dd> <dd>

Résolution horizontale, en points par pouce, à laquelle ce jeu de caractères a été numérisé.

</dd> <dt>

**dfAscent**
</dt> <dd>

Type : **Word**

</dd> <dd>

Distance entre le haut d’une cellule de définition de caractère et la ligne de base de la police typographique.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Type : **Word**

</dd> <dd>

Quantité de début dans les limites définies par le membre **dfPixHeight** . Des marques d’accentuation et d’autres caractères diacritiques peuvent se produire dans cette zone.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Type : **Word**

</dd> <dd>

Quantité d’espace de tête supplémentaire que l’application ajoute entre les lignes.

</dd> <dt>

**dfItalic**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Police en italique s’il n’est pas égal à zéro.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Police soulignée s’il n’est pas égal à zéro.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Police de barré s’il n’est pas égal à zéro.

</dd> <dt>

**dfWeight**
</dt> <dd>

Type : **Word**

</dd> <dd>

Poids de la police dans la plage comprise entre 0 et 1000. Par exemple, 400 est roman et 700 est gras. Si cette valeur est égale à zéro, une pondération par défaut est utilisée. Pour obtenir des valeurs définies supplémentaires, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfCharSet**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Jeu de caractères de la police. Pour les valeurs prédéfinies, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Type : **Word**

</dd> <dd>

Largeur de la grille sur laquelle une police vectorielle a été numérisée. Pour les polices Raster, si le membre n’est pas égal à zéro, il représente la largeur de tous les caractères de l’image bitmap. Si le membre est égal à zéro, la police a des caractères de largeur variable.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Type : **Word**

</dd> <dd>

Hauteur de la bitmap de caractères pour les polices Raster ou la hauteur de la grille sur laquelle une police vectorielle a été numérisée.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Le pas et la famille de la police. Pour plus d’informations, consultez la description de la structure [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) .

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Type : **Word**

</dd> <dd>

Largeur moyenne des caractères de la police (généralement définie en tant que largeur de la lettre x). Cette valeur n’inclut pas le dépassement requis pour les caractères gras ou italiques.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Type : **Word**

</dd> <dd>

La largeur du caractère le plus large de la police.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Premier code de caractère défini dans la police.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Dernier code de caractère défini dans la police.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Caractère à substituer aux caractères ne figurant pas dans la police.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Type : **Byte**

</dd> <dd>

Caractère qui sera utilisé pour définir des césures de mots pour la justification du texte.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Type : **Word**

</dd> <dd>

Nombre d’octets dans chaque ligne de l’image bitmap. Cette valeur est toujours même afin que les lignes commencent sur les limites de mot. Pour les polices vectorielles, ce membre n’a aucune signification.

</dd> <dt>

**dfDevice**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Offset dans le fichier à une chaîne se terminant par un caractère null qui spécifie un nom de périphérique. Pour une police générique, cette valeur est égale à zéro.

</dd> <dt>

**dfFace**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Offset dans le fichier à une chaîne se terminant par un caractère null qui nomme le type de caractères.

</dd> <dt>

**dfReserved**
</dt> <dd>

Type : **DWORD**

</dd> <dd>

Ce membre est réservé.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Type : **char**

</dd> <dd>

Nom de l’appareil si ce fichier de police est désigné pour un périphérique spécifique.

</dd> <dt>

**szFaceName**
</dt> <dd>

Type : **char**

</dd> <dd>

Nom de police de la police.

</dd> </dl>

## <a name="remarks"></a>Remarques

Il existe une structure **FONTDIRENTRY** pour chaque police du fichier. res. Les applications qui génèrent des fichiers. res avec des ressources de police doivent également ajouter au fichier une structure **FONTDIRENTRY** pour chaque police.

Les déclarations de police peuvent être mélangées à d’autres déclarations de ressource dans le. Fichier RC, car les polices n’ont pas besoin d’être contiguës dans le fichier. res.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**Dilocataire**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Ressources](resources.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

