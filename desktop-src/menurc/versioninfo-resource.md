---
title: Ressource VERSIONINFO
description: Définit une ressource d’informations sur la version. La ressource contient des informations sur le fichier en tant que son numéro de version, son système d’exploitation prévu et son nom de fichier d’origine. La ressource est destinée à être utilisée avec les fonctions d’informations de version.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menus de la ressource VERSIONINFO et autres ressources
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6708b4fefc564685a9989140e5f07dd20714e8bbcb60c53710f43cbfee4aa7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971868"
---
# <a name="versioninfo-resource"></a>Ressource VERSIONINFO

Définit une ressource d’informations sur la version. La ressource contient des informations sur le fichier en tant que son numéro de version, son système d’exploitation prévu et son nom de fichier d’origine. La ressource est destinée à être utilisée avec les fonctions d' [informations de version](./version-information.md) .

Il existe deux façons de mettre en forme une instruction **VERSIONINFO** :

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- ou -

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

Identificateur de ressource des informations de version. Cette valeur doit être 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*informations fixes*
</dt> <dd>

Les informations de version, telles que la version du fichier et le système d’exploitation prévu. Ce paramètre est constitué des instructions suivantes.



| .                         | Description                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  *Version* de FileVersion         | Numéro de version binaire du fichier. La *version* se compose d’entiers 2 32 bits, définis par des entiers 4 16 bits. Par exemple, « FILEVERSION 3, 10, 0, 61 » est traduit en deux mots doubles : 0x0003000a et 0x0000003d, dans cet ordre. Par conséquent, si la *version* est définie par les valeurs **DWORD** *DW1* et *DW2*, elles doivent apparaître dans l’instruction **FileVersion** comme suit : `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` . |
|  *Version* de PRODUCTVERSION      | Numéro de version binaire du produit avec lequel le fichier est distribué. Le paramètre de *version* est un entier 2 32 bits, défini par des entiers 4 16 bits. Pour plus d’informations sur la *version*, consultez la description de **FileVersion** .                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *FILEFLAGSMASK* | Indique les bits de l’instruction **FileFlags** qui sont valides. pour les Windows 16 bits, cette valeur est 0x3f.                                                                                                                                                                                                                                                                                                                                          |
| **FileFlags FileFlags**          | Attributs du fichier.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Fichieros**                | Système d’exploitation pour lequel ce fichier a été conçu. Le paramètre *fileos* peut être l’une des valeurs de système d’exploitation spécifiées dans la section Notes.                                                                                                                                                                                                                                                                                               |
| **Filetype type_fichier**            | Type général de fichier. Le paramètre *filetype* peut être l’une des valeurs de type de fichier listées dans la section Notes.                                                                                                                                                                                                                                                                                                                                |
|  *Sous-type* FILESUBTYPE         | Fonction du fichier. Le paramètre *SubType* est égal à zéro, sauf si le paramètre *filetype* de l’instruction **FILETYPE** est VFT \_ DRV, VFT \_ font ou VFT \_ vxd. Pour obtenir la liste des valeurs de sous-type de fichier, consultez la section Notes.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*bloc-instruction*
</dt> <dd>

Spécifie un ou plusieurs blocs d’informations sur la version. Un bloc peut contenir des informations de chaîne ou des informations sur les variables. Pour plus d’informations, consultez bloc [**StringFileInfo**](stringfileinfo-block.md) ou [**bloc VarFileInfo**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Remarques

pour utiliser les constantes spécifiées avec l’instruction **VERSIONINFO** , vous devez inclure le fichier d’en-tête Winver. h ou Windows. h dans le fichier de définition de ressource.

La liste suivante décrit les paramètres utilisés dans l’instruction **VERSIONINFO** :

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*
</dt> <dd>

Combinaison des valeurs suivantes.



| Valeur                      | Description                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **débogage VS \_ FF \_**          | Le fichier contient des informations de débogage ou est compilé avec les fonctionnalités de débogage activées.                                                                                                                                                                                         |
| **VS \_ FF \_ corrigé**        | Le fichier a été modifié et n’est pas identique au fichier d’envoi d’origine portant le même numéro de version.                                                                                                                                                                       |
| **\_ \_ version préliminaire de vs FF**     | Le fichier est une version de développement, et non un produit commercialisé.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | Le fichier n’a pas été créé à l’aide de procédures de version standard. Si cette valeur est donnée, le [**bloc StringFileInfo**](stringfileinfo-block.md) doit contenir une chaîne **PrivateBuild** .                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | Le fichier a été généré par la société d’origine à l’aide de procédures de version standard, mais il s’agit d’une variante du fichier standard du même numéro de version. Si cette valeur est donnée, le bloc de [bloc **StringFileInfo**](stringfileinfo-block.md) doit contenir une chaîne **SpecialBuild** . |
| **VS \_ FFI \_ FILEFLAGSMASK** | Combinaison de toutes les valeurs précédentes.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fichieros*
</dt> <dd>

Une des valeurs suivantes.



| Valeur                   | Description                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ inconnu**        | Le système d’exploitation pour lequel le fichier a été conçu est inconnu. |
| **VOS \_ dos**            | Le fichier a été conçu pour MS-DOS.                                    |
| **VOS \_ NT**             | Le fichier a été conçu pour une Windows de 32 bits.                            |
| **VOS \_ \_ WINDOWS16**    | Le fichier a été conçu pour une Windows 16 bits.                            |
| **VOS \_ \_ WINDOWS32**    | Le fichier a été conçu pour une Windows de 32 bits.                            |
| **VOS \_ dos \_ WINDOWS16** | le fichier a été conçu pour une Windows de 16 bits s’exécutant avec MS-DOS.        |
| **VOS \_ dos \_ WINDOWS32** | le fichier a été conçu pour une Windows de 32 bits s’exécutant avec MS-DOS.        |
| **VOS \_ NT \_ WINDOWS32**  | Le fichier a été conçu pour une Windows de 32 bits.                            |



 

Les valeurs 0x00002L, 0x00003L, 0x20000L et 0x30000L sont réservées.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*filetype*
</dt> <dd>

Une des valeurs suivantes.



| Valeur                | Description                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ inconnu**     | Le type de fichier est inconnu.                                                                                                       |
| **\_application VFT**         | Le fichier contient une application.                                                                                               |
| **\_dll VFT**         | Le fichier contient une bibliothèque de liens dynamiques (DLL).                                                                                 |
| **VFT \_ DRV**         | Le fichier contient un pilote de périphérique. Si *filetype* est **VFT \_ DRV**, *SubType* contient une description plus spécifique du pilote. |
| **\_police VFT**        | Le fichier contient une police. Si *filetype* est \_ la police VFT *, SubType* contient une description plus spécifique de la police.               |
| **VFT \_ vxd**         | Le fichier contient un appareil virtuel.                                                                                             |
| **VFT \_ static \_ lib** | Le fichier contient une bibliothèque de liens statiques.                                                                                        |



 

Toutes les autres valeurs sont réservées à une utilisation par Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*sous-type*
</dt> <dd>

Informations supplémentaires sur le type de fichier.

Si *filetype* spécifie **VFT \_ DRV**, ce paramètre peut avoir l’une des valeurs suivantes.



| Valeur                             | Description                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ inconnu**                 | Le type de pilote est inconnu.                   |
| **VFT2 \_ DRV \_ comm**               | Le fichier contient un pilote de communication.    |
| **\_Imprimante VFT2 DRV \_**            | Le fichier contient un pilote d’imprimante.           |
| **\_Clavier VFT2 DRV \_**           | Le fichier contient un pilote de clavier.          |
| **\_Langage VFT2 DRV \_**           | Le fichier contient un pilote de langage.          |
| **\_Affichage du DRV VFT2 \_**            | Le fichier contient un pilote d’affichage.           |
| **\_Souris VFT2 DRV \_**              | Le fichier contient un pilote de souris.             |
| **\_Réseau VFT2 DRV \_**            | Le fichier contient un pilote réseau.           |
| **\_Système VFT2 DRV \_**             | Le fichier contient un pilote système.            |
| **VFT2 \_ DRV \_ installable**        | Le fichier contient un pilote installable.      |
| **VFT2 \_ DRV \_**              | Le fichier contient un pilote audio.             |
| **Imprimante avec version de VFT2 \_ DRV \_ \_** | Le fichier contient un pilote d’imprimante avec version. |



 

Si *filetype* spécifie la **\_ police VFT**, ce paramètre peut avoir l’une des valeurs suivantes.



| Valeur                    | Description                    |
|--------------------------|--------------------------------|
| **VFT2 \_ inconnu**        | Le type de police est inconnu.          |
| **VFT2 de \_ police \_ Raster**   | Le fichier contient une police raster.   |
| **\_Vecteur de police VFT2 \_**   | Le fichier contient une police vectorielle.   |
| **VFT2 \_ police \_ TrueType** | Le fichier contient une police TrueType. |



 

Si *filetype* spécifie VFT \_ vxd, ce paramètre doit être l’identificateur de l’appareil virtuel inclus dans le bloc de contrôle de l’appareil virtuel.

Toutes les valeurs de *sous-type* non répertoriées ici sont réservées à une utilisation par Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

L’un des codes de langue suivants.



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
| 0x0414 | Norvégien? Bokmal  | 0x100C | Français Suisse              |
| 0x0810 | Italien Suisse       | 0x0816 | Portugais (Portugal)     |
| 0x0813 | Néerlandais (Belgique)       | 0x081A | Serbo-Croatian (cyrillique) |
| 0x0814 | Norvégien? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Un des identificateurs de jeu de caractères suivants.



| Decimal | Valeur hexadécimale | Jeu de caractères              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII 7 bits                |
| 932     | 03A4        | Le Japon (Maj ? JIS X-0208) |
| 949     | 03B5        | Corée (Maj ? KSC 5601)   |
| 950     | 03B6        | Taïwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latin-2 (Europe de l’est) |
| 1251    | 04E3        | Cyrillique                   |
| 1252    | 04E4        | Multilingue               |
| 1253    | 04E5        | Grec                      |
| 1254    | 04E6        | Turc                    |
| 1 255    | 04E7        | Hébreu                     |
| 1256    | 04E8        | Arabe                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nom de chaîne*
</dt> <dd>

L’un des noms prédéfinis suivants.



| Nom                 | Description                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commentaires**         | Informations supplémentaires à afficher à des fins de diagnostic.                                                                                                                                                                                                                                    |
| **CompanyName**      | Société qui a produit le fichier ? par exemple, « Microsoft Corporation » ou « Standard Microsystems Corporation, Inc. » Cette chaîne est requise.                                                                                                                                                                   |
| **FileDescription**  | Description du fichier à présenter aux utilisateurs. Cette chaîne peut être affichée dans une zone de liste lorsque l’utilisateur choisit les fichiers à installer ? par exemple, « pilote de clavier pour AT-Style claviers ». Cette chaîne est requise.                                                                                            |
| **FileVersion**      | Numéro de version du fichier, par exemple « 3,10 » ou « 5,00. RC2 ». Cette chaîne est requise.                                                                                                                                                                                                                      |
| **InternalName**     | Nom interne du fichier, s’il en existe un, par exemple, un nom de module s’il s’agit d’une bibliothèque de liens dynamiques. Si le fichier n’a pas de nom interne, cette chaîne doit être le nom de fichier d’origine, sans extension. Cette chaîne est requise.                                                                       |
| **LegalCopyright**   | Mentions de droits d’auteur s’appliquant au fichier. Cela doit inclure le texte intégral de toutes les mentions, symboles légaux, dates de copyright, etc. Cette chaîne est facultative.                                                                                                                                             |
| **LegalTrademarks**  | Marques et marques déposées qui s’appliquent au fichier. Cela doit inclure le texte intégral de la totalité des mentions, symboles légaux, numéros de marques, etc. Cette chaîne est facultative.                                                                                                                        |
| **OriginalFilename** | Nom d’origine du fichier, à l’exclusion du chemin d’accès. Ces informations permettent à une application de déterminer si un fichier a été renommé par un utilisateur. Le format du nom dépend du système de fichiers pour lequel le fichier a été créé. Cette chaîne est requise.                                                 |
| **PrivateBuild**     | Informations sur une version privée du fichier, par exemple, « créé par TESTER1 sur \\ Testbed ». Cette chaîne doit être présente uniquement si **vs \_ FF \_ PRIVATEBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine.                                                                                   |
| **ProductName**      | Nom du produit avec lequel le fichier est distribué. Cette chaîne est requise.                                                                                                                                                                                                                            |
| **ProductVersion**   | Version du produit avec lequel le fichier est distribué, par exemple « 3,10 » ou « 5,00. RC2 ». Cette chaîne est requise.                                                                                                                                                                                       |
| **SpecialBuild**     | Texte qui indique la différence entre cette version du fichier et la version standard, par exemple « build privée pour TESTER1 résolution des problèmes de souris sur les ordinateurs M250 et M250E ». Cette chaîne doit être présente uniquement si **vs \_ FF \_ SPECIALBUILD** est spécifié dans le paramètre *FileFlags* du bloc racine. |



 

</dd> </dl>

Certains attributs sont également pris en charge pour la compatibilité descendante. Pour plus d’informations, consultez [attributs de ressource communs](common-resource-attributes.md).

## <a name="examples"></a>Exemples

L’exemple suivant définit une ressource **VERSIONINFO** :

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des informations de version](./using-version-information.md)
</dt> <dt>

[Informations sur la version](./version-information.md)
</dt> </dl>

 

 