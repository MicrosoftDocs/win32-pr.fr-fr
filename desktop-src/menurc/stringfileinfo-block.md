---
title: StringFileInfo bloc (instruction)
description: Décrit la forme du bloc d’informations de chaîne.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Menus de l’instruction de bloc StringFileInfo et autres ressources
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468257d0b8b8b53f3168e8e11e2f649b8354d50a76d3c2a010b98d245472aad0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886762"
---
# <a name="stringfileinfo-block-statement"></a>StringFileInfo bloc (instruction)

Définit un bloc d’informations de type chaîne.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Paire d’identificateurs de langue et de jeu de caractères. Il s’agit d’une chaîne hexadécimale qui se compose de la concaténation des identificateurs de langue et de jeu de caractères spécifiés dans la section Notes.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nom de chaîne*
</dt> <dd>

Nom d’une valeur dans le bloc et peut être l’un des noms prédéfinis spécifiés dans la section Notes.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*ajoutée*
</dt> <dd>

Chaîne de caractères qui spécifie la valeur du nom de chaîne correspondant. Plusieurs instructions de **valeur** peuvent être fournies.

</dd> </dl>

## <a name="remarks"></a>Remarques

Le paramètre *lang-charset* spécifie l’un des codes de langue suivants.



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



 

Le paramètre *lang-charset* spécifie également l’un des identificateurs de jeu de caractères suivants.



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



 

Le paramètre *String-name* spécifie l’un des noms prédéfinis suivants.



| Nom                 | Description                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commentaires**         | Informations supplémentaires à afficher à des fins de diagnostic.                                                                                                                                                                                                                                    |
| **CompanyName**      | Société qui a produit le fichier, par exemple « Microsoft Corporation » ou « Standard Microsystems Corporation, Inc. » Cette chaîne est requise.                                                                                                                                                                   |
| **FileDescription**  | Description du fichier à présenter aux utilisateurs. Cette chaîne peut être affichée dans une zone de liste lorsque l’utilisateur choisit les fichiers à installer, par exemple « pilote de clavier pour AT-Style claviers ». Cette chaîne est requise.                                                                                            |
| **FileVersion**      | Numéro de version du fichier, par exemple « 3,10 » ou « 5,00. RC2 ». Cette chaîne est requise.                                                                                                                                                                                                                      |
| **InternalName**     | Nom interne du fichier, s’il en existe un, par exemple, un nom de module s’il s’agit d’une bibliothèque de liens dynamiques. Si le fichier n’a pas de nom interne, cette chaîne doit être le nom de fichier d’origine, sans extension. Cette chaîne est requise.                                                                       |
| **LegalCopyright**   | Mentions de droits d’auteur s’appliquant au fichier. Cela doit inclure le texte intégral de toutes les mentions, symboles légaux, dates de copyright, etc. Cette chaîne est facultative.                                                                                                                                             |
| **LegalTrademarks**  | Marques et marques déposées qui s’appliquent au fichier. Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, numéros de marques, etc. Cette chaîne est facultative.                                                                                                                        |
| **OriginalFilename** | Nom d’origine du fichier, à l’exclusion du chemin d’accès. Ces informations permettent à une application de déterminer si un fichier a été renommé par un utilisateur. Le format du nom dépend du système de fichiers pour lequel le fichier a été créé. Cette chaîne est requise.                                                 |
| **PrivateBuild**     | Informations sur une version privée du fichier, par exemple, « créé par TESTER1 sur \\ Testbed ». Cette chaîne doit être présente uniquement si **vs \_ FF \_ PRIVATEBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine.                                                                                   |
| **ProductName**      | Nom du produit avec lequel le fichier est distribué. Cette chaîne est requise.                                                                                                                                                                                                                            |
| **ProductVersion**   | Version du produit avec lequel le fichier est distribué, par exemple « 3,10 » ou « 5,00. RC2 ». Cette chaîne est requise.                                                                                                                                                                                       |
| **SpecialBuild**     | Texte qui spécifie la différence entre cette version du fichier et la version standard, par exemple « build privée pour TESTER1 résolution des problèmes de souris sur les ordinateurs M250 et M250E ». Cette chaîne doit être présente uniquement si **vs \_ FF \_ SPECIALBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine. |



 

 

 




