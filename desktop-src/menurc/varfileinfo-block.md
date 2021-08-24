---
title: VarFileInfo bloc (instruction)
description: Décrit la forme du bloc d’informations sur les variables.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menus de l’instruction de bloc VarFileInfo et autres ressources
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e15b4bf57a14d6bae6dd5b83c8ea86e38830113fbcfbbaa27b143bf02bb130e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119846969"
---
# <a name="varfileinfo-block-statement"></a>VarFileInfo bloc (instruction)

Définit un bloc d’informations de variable.

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Un des identificateurs de langue spécifiés dans la section Notes.

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Un des identificateurs de jeu de caractères spécifiés dans la section Notes.

</dd> </dl>

## <a name="remarks"></a>Remarques

Plusieurs paires d’identificateurs peuvent être fournies, mais chaque paire doit être séparée de la paire précédente par une virgule.

Le paramètre *LangID* spécifie l’un des codes de langue suivants.



| Code   | Langage            | Code   | Langage                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabe              | 0x0415 | Polonais                    |
| 0x0402 | Bulgare           | 0x0416 | Portugais (Brésil)       |
| 0x0403 | Catalan             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Chinois traditionnel | 0x0418 | Roumain                  |
| 0x0405 | Tchèque               | 0x0419 | Russe                   |
| 0x0406 | Danois              | 0x041A | Croato-Serbian (latin)    |
| 0x0407 | Allemand              | 0x041B | Slovaque                    |
| 0x0408 | Grec               | 0x041C | Albanais                  |
| 0x0409 | Anglais (États-Unis)        | 0x041D | Suédois                   |
| 0x040A | Espagnol castillan   | 0x041E | Thaï                      |
| 0x040B | Finnois             | 0x041F | Turc                   |
| 0x040C | Français              | 0x0420 | Ourdou                      |
| 0x040D | Hébreu              | 0x0421 | Bahasa                    |
| 0x040E | Hongrois           | 0x0804 | Chinois simplifié        |
| 0x040F | Islandais           | 0x0807 | Allemand Suisse              |
| 0x0410 | Italien             | 0x0809 | au Royaume-Uni Anglais              |
| 0x0411 | Japonais            | 0x080A | Espagnol (Mexique)          |
| 0x0412 | Coréen              | 0x080C | Français belge            |
| 0x0413 | Néerlandais               | 0x0C0C | Français (Canada)           |
| 0x0414 | Norvégien – bokmal  | 0x100C | Français Suisse              |
| 0x0810 | Italien Suisse       | 0x0816 | Portugais (Portugal)     |
| 0x0813 | Néerlandais (Belgique)       | 0x081A | Serbo-Croatian (cyrillique) |
| 0x0814 | Norvégien – nynorsk | ?      | ?                         |



 

Le paramètre *charsetID* spécifie l’un des identificateurs de jeu de caractères suivants :



| Identificateur | Jeu de caractères              |
|------------|----------------------------|
| 0          | ASCII 7 bits                |
| 932        | Japon (Shift-JIS X-0208) |
| 949        | Corée (Shift-KSC 5601)   |
| 950        | Taïwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Europe de l’est) |
| 1251       | Cyrillique                   |
| 1252       | Multilingue               |
| 1253       | Grec                      |
| 1254       | Turc                    |
| 1 255       | Hébreu                     |
| 1256       | Arabe                     |



 

 

 




