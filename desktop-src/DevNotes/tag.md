---
description: Identifie une entrée dans la base de données de shims.
ms.assetid: c092592d-a4f4-4b2f-9b03-c07951ed214a
title: TAG (Exposeenums2managed. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfc7e4df727245ead30ecefef0cd941148b8f4c76e2881ab19f41c3388934abd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075793"
---
# <a name="tag"></a>ÉTIQUETTE

Identifie une entrée dans la base de données de shims.

Les entrées suivantes sont de type **\_ \_ liste de types de balises** (0x7000).



| Constante/valeur                                                                                                                                                                                                                                                             | Description                                                               |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| <span id="TAG_DATABASE"></span><span id="tag_database"></span><dl> <dt>**Balise \_ Base de données**</dt> <dt>( \| **\_ \_ liste de types de balise** 0x1)</dt> </dl>                               | Entrée de base de données.<br/>                                                |
| <span id="TAG_LIBRARY"></span><span id="tag_library"></span><dl> <dt>**Balise \_ Bibliothèque**</dt> <dt>( \| **liste des \_ types \_ de balise** 0X2)</dt> </dl>                                  | Entrée de la bibliothèque.<br/>                                                 |
| <span id="TAG_INEXCLUDE"></span><span id="tag_inexclude"></span><dl> <dt>**Balise \_ Inexclude**</dt> <dt>( \| **\_ \_ liste de types de balises** 0x3)</dt> </dl>                            | Entrée include et Exclude.<br/>                                     |
| <span id="TAG_SHIM"></span><span id="tag_shim"></span><dl> <dt>**Balise \_ SHIM**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x4)</dt> </dl>                                           | Entrée de Shim qui contient le nom et les informations d’objectif.<br/>     |
| <span id="TAG_PATCH"></span><span id="tag_patch"></span><dl> <dt>**Balise \_ PATCH**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x5)</dt> </dl>                                        | Entrée de correctif qui contient les informations de mise à jour corrective en mémoire.<br/>  |
| <span id="TAG_APP"></span><span id="tag_app"></span><dl> <dt>**Balise \_ APPLICATION**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x6)</dt> </dl>                                              | Entrée de l’application.<br/>                                             |
| <span id="TAG_EXE"></span><span id="tag_exe"></span><dl> <dt>**Balise \_ EXE**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x7)</dt> </dl>                                              | Entrée exécutable.<br/>                                              |
| <span id="TAG_MATCHING_FILE"></span><span id="tag_matching_file"></span><dl> <dt>**Balise \_ \_Fichier correspondant**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x8)</dt> </dl>               | Entrée de fichier correspondante.<br/>                                           |
| <span id="TAG_SHIM_REF"></span><span id="tag_shim_ref"></span><dl> <dt>**Balise \_ SHIM \_ Réf**</dt> . <dt>( \| liste de types de balises 0x9 \_ \_ )</dt> </dl>                                   | Entrée de définition du shim.<br/>                                         |
| <span id="TAG_PATCH_REF"></span><span id="tag_patch_ref"></span><dl> <dt>**Balise \_ PATCH \_ Réf**</dt> <dt>( \| **liste de \_ types \_ de balises** 0xA)</dt> </dl>                           | Entrée de définition de correctif.<br/>                                        |
| <span id="TAG_LAYER"></span><span id="tag_layer"></span><dl> <dt>**Balise \_ COUCHE**</dt> <dt>( \| **\_ \_ liste type de balise** 0xB)</dt> </dl>                                        | Entrée de shim de couche.<br/>                                              |
| <span id="TAG_FILE"></span><span id="tag_file"></span><dl> <dt>**Balise \_ FICHIER**</dt> <dt>( \| **\_ \_ liste type de balise** 0xc)</dt> </dl>                                           | Attribut de fichier utilisé dans une entrée de shim.<br/>                           |
| <span id="TAG_APPHELP"></span><span id="tag_apphelp"></span><dl> <dt>**Balise \_ APPHELP**</dt> <dt>( \| **liste de \_ types \_ de balises** 0xD)</dt> </dl>                                  | Entrée d’informations AppHelp.<br/>                                     |
| <span id="TAG_LINK"></span><span id="tag_link"></span><dl> <dt>**Balise \_ LINK**</dt> <dt>( \| **liste de \_ types \_ de balise** 0xE)</dt> </dl>                                           | Entrée d’informations du lien AppHelp online.<br/>                         |
| <span id="TAG_DATA"></span><span id="tag_data"></span><dl> <dt>**Balise \_ DONNÉES**</dt> <dt>( \| **\_ \_ liste type de balise** 0xF)</dt> </dl>                                           | Entrée de mappage nom-valeur.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM"></span><span id="tag_msi_transform"></span><dl> <dt>**Balise \_ MSI \_ Transform**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x10)</dt> </dl>              | Entrée de transformation MSI.<br/>                                      |
| <span id="TAG_MSI_TRANSFORM_REF"></span><span id="tag_msi_transform_ref"></span><dl> <dt>**Balise \_ MSI \_ Transform \_ ref**</dt> <dt>( \| **liste de \_ types \_ de balise** 0x11)</dt> </dl> | Entrée de définition de transformation MSI.<br/>                           |
| <span id="TAG_MSI_PACKAGE"></span><span id="tag_msi_package"></span><dl> <dt>**Balise \_ \_Package MSI**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x12)</dt> </dl>                    | Entrée de package MSI.<br/>                                             |
| <span id="TAG_FLAG"></span><span id="tag_flag"></span><dl> <dt>**Balise \_ FLAG**</dt> <dt>( \| **liste de \_ types \_ de balises** 0x13)</dt> </dl>                                          | Entrée de l’indicateur.<br/>                                                    |
| <span id="TAG_MSI_CUSTOM_ACTION"></span><span id="tag_msi_custom_action"></span><dl> <dt>**Balise \_ MSI \_ Custom \_ action**</dt> <dt>(0x14 \| **\_ \_ liste type de balise**)</dt> </dl> | Entrée d’action personnalisée MSI.<br/>                                       |
| <span id="TAG_FLAG_REF"></span><span id="tag_flag_ref"></span><dl> <dt>**Balise \_ INDICATEUR \_ ref**</dt> <dt>( \| **liste de \_ types \_ de balise** 0x15)</dt> </dl>                             | Entrée de la définition de l’indicateur.<br/>                                         |
| <span id="TAG_ACTION"></span><span id="tag_action"></span><dl> <dt>**Balise \_ ACTION**</dt> <dt>( \| **liste de \_ types \_ de balise** 0x16)</dt> </dl>                                    | Inutilisé.<br/>                                                        |
| <span id="TAG_LOOKUP"></span><span id="tag_lookup"></span><dl> <dt>**Balise \_ LOOKUP**</dt> <dt>( \| **liste de \_ types \_ de balise** 0x17)</dt> </dl>                                    | Entrée de recherche utilisée pour la recherche dans une base de données de pilotes.<br/>             |
| <span id="TAG_STRINGTABLE"></span><span id="tag_stringtable"></span><dl> <dt>**Balise \_ STRINGTABLE**</dt> <dt>( \| **liste des \_ types \_ de balise** 0x801)</dt> </dl>                    | Entrée de la table de chaînes.<br/>                                            |
| <span id="TAG_INDEXES"></span><span id="tag_indexes"></span><dl> <dt>**Balise \_ INDEX**</dt> <dt>( \| **\_ \_ liste de types de balise** 0x802)</dt> </dl>                                | Indexe l’entrée qui définit tous les index d’une base de données de shims.<br/> |
| <span id="TAG_INDEX"></span><span id="tag_index"></span><dl> <dt>**Balise \_ INDEX**</dt> <dt>( \| **liste de \_ types \_ de balise** 0x803)</dt> </dl>                                      | Entrée d’index qui définit un index dans une base de données de shims.<br/>          |



Les entrées suivantes sont de type de **balise \_ \_ STRINGREF** (0x6000).



| Constante/valeur                                                                                                                                                                                                                                                                     | Description                                                                                   |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="TAG_NAME"></span><span id="tag_name"></span><dl> <dt>**Balise \_ NAME**</dt> <dt>(0x1 \| **, \_ type \_ de balise STRINGREF**)</dt> </dl>                                              | Attribut Name.<br/>                                                                    |
| <span id="TAG_DESCRIPTION"></span><span id="tag_description"></span><dl> <dt>**Balise \_ DESCRIPTION**</dt> <dt>(0X2 \| **, \_ type \_ de balise STRINGREF**)</dt> </dl>                         | Entrée de description.<br/>                                                                 |
| <span id="TAG_MODULE"></span><span id="tag_module"></span><dl> <dt>**Balise \_ MODULE**</dt> <dt>( \| **type de balise 0x3 \_ \_ STRINGREF**)</dt> </dl>                                        | Attribut de module.<br/>                                                                  |
| <span id="TAG_API"></span><span id="tag_api"></span><dl> <dt>**Balise \_ API**</dt> <dt>( \| **type de balise 0x4 \_ \_ STRINGREF**)</dt> </dl>                                                 | Entrée d’API.<br/>                                                                         |
| <span id="TAG_VENDOR"></span><span id="tag_vendor"></span><dl> <dt>**Balise \_ VENDOR**</dt> <dt>( \| **type de balise 0x5 \_ \_ STRINGREF**)</dt> </dl>                                        | Attribut de nom de fournisseur.<br/>                                                             |
| <span id="TAG_APP_NAME"></span><span id="tag_app_name"></span><dl> <dt>**Balise \_ \_Nom**</dt> de l’application <dt>( \| **type de balise 0x6 \_ \_ STRINGREF**)</dt> </dl>                                 | Attribut de nom d’application qui décrit une entrée d’application dans une base de données de shims.<br/> |
| <span id="TAG_COMMAND_LINE"></span><span id="tag_command_line"></span><dl> <dt>**Balise \_ \_Ligne de commande**</dt> <dt>( \| **type de balise 0x8 \_ \_ STRINGREF**)</dt> </dl>                     | Attribut de ligne de commande utilisé lors du passage des arguments à un shim, par exemple.<br/> |
| <span id="TAG_COMPANY_NAME"></span><span id="tag_company_name"></span><dl> <dt>**Balise \_ \_Nom**</dt> de la société <dt>( \| **type de balise 0x9 \_ \_ STRINGREF**)</dt> </dl>                     | Attribut de nom de la société.<br/>                                                            |
| <span id="TAG_DLLFILE"></span><span id="tag_dllfile"></span><dl> <dt>**Balise \_ DLLFILE**</dt> <dt>( \| **type de balise 0xA \_ \_ STRINGREF**)</dt> </dl>                                     | Attribut de fichier DLL pour une entrée de shim.<br/>                                               |
| <span id="TAG_WILDCARD_NAME"></span><span id="tag_wildcard_name"></span><dl> <dt>**Balise \_ \_Nom du caractère générique**</dt> <dt>( \| **type de balise 0xb \_ \_ STRINGREF**)</dt> </dl>                  | Attribut de nom générique pour une entrée exécutable avec un caractère générique comme nom de fichier.<br/>  |
| <span id="TAG_PRODUCT_NAME"></span><span id="tag_product_name"></span><dl> <dt>**Balise \_ \_Nom du produit**</dt> <dt>( \| **type de balise 0x10 \_ \_ STRINGREF**)</dt> </dl>                    | Attribut Product Name.<br/>                                                            |
| <span id="TAG_PRODUCT_VERSION"></span><span id="tag_product_version"></span><dl> <dt>**Balise \_ \_Version du produit**</dt> <dt>( \| **type de balise 0x11 \_ \_ STRINGREF**)</dt> </dl>           | Attribut de version du produit.<br/>                                                         |
| <span id="TAG_FILE_DESCRIPTION"></span><span id="tag_file_description"></span><dl> <dt>**Balise \_ \_Description du fichier**</dt> <dt>( \| **type de balise 0x12 \_ \_ STRINGREF**)</dt> </dl>        | Attribut de description de fichier.<br/>                                                        |
| <span id="TAG_FILE_VERSION"></span><span id="tag_file_version"></span><dl> <dt>**Balise \_ \_Version de fichier**</dt> <dt>( \| **type de balise 0x13 \_ \_ STRINGREF**)</dt> </dl>                    | Attribut de version de fichier.<br/>                                                            |
| <span id="TAG_ORIGINAL_FILENAME"></span><span id="tag_original_filename"></span><dl> <dt>**Balise \_ \_Nom du fichier d’origine**</dt> <dt>(0x14 \| , **type de balise \_ \_ STRINGREF**)</dt> </dl>     | Attribut de nom de fichier d’origine.<br/>                                                      |
| <span id="TAG_INTERNAL_NAME"></span><span id="tag_internal_name"></span><dl> <dt>**Balise \_ \_Nom interne**</dt> <dt>( \| **type de balise 0x15 \_ \_ STRINGREF**)</dt> </dl>                 | Attribut de nom de fichier interne.<br/>                                                      |
| <span id="TAG_LEGAL_COPYRIGHT"></span><span id="tag_legal_copyright"></span><dl> <dt>**Balise \_ \_Copyright légal**</dt> <dt>( \| **type de balise 0x16 \_ \_ STRINGREF**)</dt> </dl>           | Attribut de copyright.<br/>                                                               |
| <span id="TAG_16BIT_DESCRIPTION"></span><span id="tag_16bit_description"></span><dl> <dt>**Description de la balise \_ 16 \_ bits**</dt> <dt>( \| **type de balise 0x17 \_ \_ STRINGREF**)</dt> </dl>     | attribut de description 16 bits.<br/>                                                      |
| <span id="TAG_APPHELP_DETAILS"></span><span id="tag_apphelp_details"></span><dl> <dt>**Balise \_ \_Détails du APPHELP**</dt> <dt>( \| **type de balise 0x18 \_ \_ STRINGREF**)</dt> </dl>           | Attribut des informations du message AppHelp details.<br/>                                     |
| <span id="TAG_LINK_URL"></span><span id="tag_link_url"></span><dl> <dt>**Balise \_ \_URL du lien**</dt> <dt>( \| **type de balise 0x19 \_ \_ STRINGREF**)</dt> </dl>                                | Attribut d’URL du lien AppHelp online.<br/>                                                 |
| <span id="TAG_LINK_TEXT"></span><span id="tag_link_text"></span><dl> <dt>**Balise \_ \_Texte du lien**</dt> <dt>( \| **type de balise 0x1A \_ \_ STRINGREF**)</dt> </dl>                             | Attribut de texte du lien AppHelp online.<br/>                                                |
| <span id="TAG_APPHELP_TITLE"></span><span id="tag_apphelp_title"></span><dl> <dt>**Balise \_ \_Titre de APPHELP**</dt> <dt>( \| **type de balise 0x1B \_ \_ STRINGREF**)</dt> </dl>                 | Attribut de titre AppHelp.<br/>                                                           |
| <span id="TAG_APPHELP_CONTACT"></span><span id="tag_apphelp_contact"></span><dl> <dt>**Balise \_ \_**</dt> <dt>Numéro de série du point de contact (0x1C \| **\_ \_ STRINGREF**)</dt> </dl>           | Attribut de contact du fournisseur AppHelp.<br/>                                                  |
| <span id="TAG_SXS_MANIFEST"></span><span id="tag_sxs_manifest"></span><dl> <dt>**Balise \_ \_Manifeste SxS**</dt> <dt>( \| **type de balise 0x1d \_ \_ STRINGREF**)</dt> </dl>                    | Entrée de manifeste côte à côte.<br/>                                                       |
| <span id="TAG_DATA_STRING"></span><span id="tag_data_string"></span><dl> <dt>**Balise \_ \_Chaîne de données**</dt> <dt>( \| **type de balise 0x1E \_ \_ STRINGREF**)</dt> </dl>                       | Attribut de chaîne pour une entrée de données.<br/>                                                 |
| <span id="TAG_MSI_TRANSFORM_FILE"></span><span id="tag_msi_transform_file"></span><dl> <dt>**Balise \_ \_ \_ Fichier de transformation MSI**</dt> <dt>( \| **type de balise 0x1F \_ \_ STRINGREF**)</dt> </dl> | Attribut de nom de fichier d’une entrée de transformation MSI.<br/>                                |
| <span id="TAG_16BIT_MODULE_NAME"></span><span id="tag_16bit_module_name"></span><dl> <dt>**\_ Nom du \_ module \_ de balise 16 bits**</dt> <dt>( \| **type de balise 0x20 \_ \_ STRINGREF**)</dt> </dl>    | attribut de nom de module 16 bits.<br/>                                                      |
| <span id="TAG_LAYER_DISPLAYNAME"></span><span id="tag_layer_displayname"></span><dl> <dt>**Balise \_ \_DisplayName**</dt> de la couche <dt>( \| **type de balise 0x21 \_ \_ STRINGREF**)</dt> </dl>     | Inutilisé.<br/>                                                                            |
| <span id="TAG_COMPILER_VERSION"></span><span id="tag_compiler_version"></span><dl> <dt>**Balise \_ \_Version du compilateur**</dt> <dt>( \| **type de balise 0X22 \_ \_ STRINGREF**)</dt> </dl>        | Version du compilateur de base de données de shims.<br/>                                                    |
| <span id="TAG_ACTION_TYPE"></span><span id="tag_action_type"></span><dl> <dt>**Balise \_ \_Type d’action**</dt> <dt>( \| **type de balise 0x23 \_ \_ STRINGREF**)</dt> </dl>                       | Inutilisé.<br/>                                                                            |
| <span id="TAG_EXPORT_NAME"></span><span id="tag_export_name"></span><dl> <dt>**Balise \_ EXPORT \_ Name**</dt> <dt>( \| **type de balise 0x24 \_ \_ STRINGREF**)</dt> </dl>                       | Attribut de nom de fichier d’exportation.<br/>                                                        |



Les entrées suivantes sont de type de **balise \_ \_ DWORD** (0x4000).



| Constante/valeur                                                                                                                                                                                                                                                                    | Description                                                                                                      |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| <span id="TAG_SIZE"></span><span id="tag_size"></span><dl> <dt>**Balise \_ TAILLE**</dt> <dt>(0x1 \| **type de balise \_ \_ DWORD**)</dt> </dl>                                                 | Attribut de taille de fichier.<br/>                                                                                  |
| <span id="TAG_OFFSET"></span><span id="tag_offset"></span><dl> <dt>**Balise \_ OFFSET**</dt> <dt>(0X2 \| **type de balise \_ \_ DWORD**)</dt> </dl>                                           | Inutilisé.<br/>                                                                                               |
| <span id="TAG_CHECKSUM"></span><span id="tag_checksum"></span><dl> <dt>**Balise \_ CHECKSUM**</dt> <dt>( \| **type de balise 0x3 \_ \_ DWORD**)</dt> </dl>                                     | Attribut de somme de contrôle de fichier.<br/>                                                                              |
| <span id="TAG_SHIM_TAGID"></span><span id="tag_shim_tagid"></span><dl> <dt>**Balise \_ SHIM \_ TagId**</dt> <dt>( \| **type de balise 0x4 \_ \_ DWORD**)</dt> </dl>                              | Attribut shim **TagId** .<br/>                                                                             |
| <span id="TAG_PATCH_TAGID"></span><span id="tag_patch_tagid"></span><dl> <dt>**Balise \_ CORRECTIF \_ TagId**</dt> <dt>( \| **type de balise 0x5 \_ \_ DWORD**)</dt> </dl>                           | Attribut **TagId** de patch.<br/>                                                                            |
| <span id="TAG_MODULE_TYPE"></span><span id="tag_module_type"></span><dl> <dt>**Balise \_ \_Type de module**</dt> <dt>( \| **type de balise 0x6, \_ \_ DWORD**)</dt> </dl>                           | Attribut de type de module.<br/>                                                                                |
| <span id="TAG_VERDATEHI"></span><span id="tag_verdatehi"></span><dl> <dt>**Balise \_ VERDATEHI**</dt> <dt>( \| **type de balise 0x7 \_ \_ DWORD**)</dt> </dl>                                  | Partie ordre élevé de l’attribut date de la version du fichier.<br/>                                                |
| <span id="TAG_VERDATELO"></span><span id="tag_verdatelo"></span><dl> <dt>**Balise \_ VERDATELO**</dt> <dt>( \| **type de balise 0x8 \_ \_ DWORD**)</dt> </dl>                                  | Partie de l’ordre bas de l’attribut date de la version du fichier.<br/>                                                 |
| <span id="TAG_VERFILEOS"></span><span id="tag_verfileos"></span><dl> <dt>**Balise \_ VERFILEOS**</dt> <dt>( \| **type de balise 0x9 \_ \_ DWORD**)</dt> </dl>                                  | Attribut version du fichier du système d’exploitation.<br/>                                                              |
| <span id="TAG_VERFILETYPE"></span><span id="tag_verfiletype"></span><dl> <dt>**Balise \_ VERFILETYPE**</dt> <dt>( \| **type de balise 0xA- \_ \_ DWORD**)</dt> </dl>                            | Attribut de type de fichier.<br/>                                                                                  |
| <span id="TAG_PE_CHECKSUM"></span><span id="tag_pe_checksum"></span><dl> <dt>**Balise \_ \_Somme de contrôle PE**</dt> <dt>( \| **type de balise 0xb \_ \_ DWORD**)</dt> </dl>                           | Attribut de somme de contrôle de fichier PE.<br/>                                                                           |
| <span id="TAG_PREVOSMAJORVER"></span><span id="tag_prevosmajorver"></span><dl> <dt>**Balise \_ PREVOSMAJORVER**</dt> <dt>( \| **type de balise 0xc \_ \_ DWORD**)</dt> </dl>                   | Attribut de version du système d’exploitation principal.<br/>                                                             |
| <span id="TAG_PREVOSMINORVER"></span><span id="tag_prevosminorver"></span><dl> <dt>**Balise \_ PREVOSMINORVER**</dt> <dt>( \| **\_ type \_ de balise** 0xD</dt> </dl>                   | Attribut de version du système d’exploitation mineur.<br/>                                                             |
| <span id="TAG_PREVOSPLATFORMID"></span><span id="tag_prevosplatformid"></span><dl> <dt>**Balise \_ PREVOSPLATFORMID**</dt> <dt>( \| **type de balise 0xE \_ \_ DWORD**)</dt> </dl>             | Attribut d’identificateur de la plateforme du système d’exploitation.<br/>                                                       |
| <span id="TAG_PREVOSBUILDNO"></span><span id="tag_prevosbuildno"></span><dl> <dt>**Balise \_ PREVOSBUILDNO**</dt> <dt>( \| **type de balise 0xF \_ \_ DWORD**)</dt> </dl>                      | Attribut du numéro de build du système d’exploitation.<br/>                                                              |
| <span id="TAG_PROBLEMSEVERITY"></span><span id="tag_problemseverity"></span><dl> <dt>**Balise \_ PROBLEMSEVERITY**</dt> <dt>( \| **type de balise 0x10 \_ \_ DWORD**)</dt> </dl>               | Attribut block d’une entrée AppHelp. Cela détermine si l’application est bloquée en dur ou en douceur.<br/> |
| <span id="TAG_LANGID"></span><span id="tag_langid"></span><dl> <dt>**Balise \_ LANGID**</dt> <dt>( \| **type de balise 0x11 \_ \_ DWORD**)</dt> </dl>                                          | Identificateur de langue d’une entrée AppHelp.<br/>                                                              |
| <span id="TAG_VER_LANGUAGE"></span><span id="tag_ver_language"></span><dl> <dt>**Balise \_ Version \_ langue**</dt> <dt>( \| **type de balise 0x12 \_ \_ DWORD**)</dt> </dl>                       | Attribut de version de langage d’un fichier.<br/>                                                                 |
| <span id="TAG_ENGINE"></span><span id="tag_engine"></span><dl> <dt>**Balise \_ MOTEUR**</dt> <dt>(0x14 \| **type de balise \_ \_ DWORD**)</dt> </dl>                                          | Inutilisé.<br/>                                                                                               |
| <span id="TAG_HTMLHELPID"></span><span id="tag_htmlhelpid"></span><dl> <dt>**Balise \_ HTMLHELPID**</dt> <dt>( \| **type de balise 0x15 \_ \_ DWORD**)</dt> </dl>                              | Attribut d’identificateur d’aide pour une entrée AppHelp.<br/>                                                       |
| <span id="TAG_INDEX_FLAGS"></span><span id="tag_index_flags"></span><dl> <dt>**Balise \_ \_Indicateurs d’index**</dt> <dt>( \| **type de balise 0x16 \_ \_ DWORD**)</dt> </dl>                          | Attribut flags pour une entrée d’index.<br/>                                                                   |
| <span id="TAG_FLAGS"></span><span id="tag_flags"></span><dl> <dt>**Balise \_ FLAGs**</dt> <dt>( \| **type de balise 0x17 \_ \_ DWORD**)</dt> </dl>                                             | Attribut flags pour une entrée AppHelp.<br/>                                                                 |
| <span id="TAG_DATA_VALUETYPE"></span><span id="tag_data_valuetype"></span><dl> <dt>**Balise \_ \_ValueType de données**</dt> <dt>( \| **type de balise 0x18 \_ \_ DWORD**)</dt> </dl>                 | Attribut de type de données pour une entrée de données.<br/>                                                                 |
| <span id="TAG_DATA_DWORD"></span><span id="tag_data_dword"></span><dl> <dt>**Balise \_ DONNÉES \_ DWORD**</dt> <dt>( \| **type de balise 0x19 \_ \_ DWORD**)</dt> </dl>                             | Attribut de valeur **DWORD** pour une entrée de données.<br/>                                                           |
| <span id="TAG_LAYER_TAGID"></span><span id="tag_layer_tagid"></span><dl> <dt>**Balise \_ \_TagId de couche**</dt> <dt>( \| **type de balise 0x1A \_ \_ DWORD**)</dt> </dl>                          | Attribut **TagId** de la couche shim.<br/>                                                                       |
| <span id="TAG_MSI_TRANSFORM_TAGID"></span><span id="tag_msi_transform_tagid"></span><dl> <dt>**Balise \_ MSI \_ Transform \_ TagId**</dt> <dt>( \| **type de balise 0x1B \_ \_ DWORD**)</dt> </dl> | Attribut de transformation MSI **TagId** .<br/>                                                                    |
| <span id="TAG_LINKER_VERSION"></span><span id="tag_linker_version"></span><dl> <dt>**Balise \_ \_Version**</dt> de l’éditeur <dt>de liens ( \| **type de balise 0x1C \_ \_ DWORD**)</dt> </dl>                 | Attribut de version de l’éditeur de liens d’un fichier.<br/>                                                                   |
| <span id="TAG_LINK_DATE"></span><span id="tag_link_date"></span><dl> <dt>**Balise \_ \_Date de liaison**</dt> <dt>( \| **type de balise 0x1d \_ \_ DWORD**)</dt> </dl>                                | Attribut date de la liaison d’un fichier.<br/>                                                                        |
| <span id="TAG_UPTO_LINK_DATE"></span><span id="tag_upto_link_date"></span><dl> <dt>**Balise \_ \_Date du lien \_ jusqu’à la date**</dt> <dt>( \| **type de balise 0x1E \_ \_ DWORD**)</dt> </dl>                | Attribut date de la liaison d’un fichier. La correspondance est effectuée jusqu’à la date de la liaison, y compris.<br/>                   |
| <span id="TAG_OS_SERVICE_PACK"></span><span id="tag_os_service_pack"></span><dl> <dt>**Balise \_ \_Service \_ Pack du système d’exploitation**</dt> <dt>( \| **type de balise 0x1F \_ \_ DWORD**)</dt> </dl>             | Attribut de Service Pack du système d’exploitation pour une entrée exécutable.<br/>                                      |
| <span id="TAG_FLAG_TAGID"></span><span id="tag_flag_tagid"></span><dl> <dt>**Balise \_ FLAG \_ TagId**</dt> <dt>( \| **type de balise 0x20 \_ \_ DWORD**)</dt> </dl>                             | Attribut **TagId** Flags.<br/>                                                                            |
| <span id="TAG_RUNTIME_PLATFORM"></span><span id="tag_runtime_platform"></span><dl> <dt>**Balise \_ \_Plateforme d’exécution**</dt> <dt>( \| **type de balise 0x21 \_ \_ DWORD**)</dt> </dl>           | Attribut de plateforme Runtime d’un fichier.<br/>                                                                |
| <span id="TAG_OS_SKU"></span><span id="tag_os_sku"></span><dl> <dt>**Balise \_ \_Référence SKU du système d’exploitation**</dt> <dt>( \| **type de balise 0X22 \_ \_ DWORD**)</dt> </dl>                                         | Attribut SKU du système d’exploitation pour une entrée exécutable.<br/>                                               |
| <span id="TAG_OS_PLATFORM"></span><span id="tag_os_platform"></span><dl> <dt>**Balise \_ \_Plateforme du système d’exploitation**</dt> <dt>( \| **type de balise 0x23 \_ \_ DWORD**)</dt> </dl>                          | Attribut de plateforme du système d’exploitation.<br/>                                                                  |
| <span id="TAG_APP_NAME_RC_ID"></span><span id="tag_app_name_rc_id"></span><dl> <dt>**Balise \_ Nom de l’application \_ \_ \_ ID RC**</dt> <dt>( \| **type de balise 0x24 \_ \_ DWORD**)</dt> </dl>               | Attribut d’identificateur de ressource de nom d’application pour les entrées apphelp.<br/>                                   |
| <span id="TAG_VENDOR_NAME_RC_ID"></span><span id="tag_vendor_name_rc_id"></span><dl> <dt>**Balise \_ \_Nom du \_ fournisseur \_ ID RC**</dt> <dt>( \| **type de balise 0x25 \_ \_ DWORD**)</dt> </dl>      | Attribut d’identificateur de ressource de nom de fournisseur pour les entrées apphelp.<br/>                                        |
| <span id="TAG_SUMMARY_MSG_RC_ID"></span><span id="tag_summary_msg_rc_id"></span><dl> <dt>**Balise \_ RESUME \_ MSG \_ RC \_ ID**</dt> <dt>( \| **type de balise égale 0x26 \_ \_ DWORD**)</dt> </dl>      | Attribut d’identificateur de ressource de message résumé pour les entrées apphelp.<br/>                                    |
| <span id="TAG_VISTA_SKU"></span><span id="tag_vista_sku"></span><dl> <dt>**Balise \_ \_SKU Vista**</dt> <dt>( \| **type de balise 0x27 \_ \_ DWORD**)</dt> </dl>                                | Windows Attribut SKU Vista.<br/>                                                                          |
| <span id="TAG_DESCRIPTION_RC_ID"></span><span id="tag_description_rc_id"></span><dl> <dt>**Balise \_ DESCRIPTION \_ RC \_ ID**</dt> <dt>( \| **type de balise 0x28 + \_ \_ DWORD**)</dt> </dl>       | Attribut d’identificateur de ressource de description pour les entrées apphelp.<br/>                                        |
| <span id="TAG_PARAMETER1_RC_ID"></span><span id="tag_parameter1_rc_id"></span><dl> <dt>**Balise \_ PARAMÈTRE1 \_ RC \_ ID**</dt> <dt>( \| **type de balise 0x29 \_ \_ DWORD**)</dt> </dl>          | Attribut d’identificateur de ressource paramètre1 pour les entrées apphelp.<br/>                                         |
| <span id="TAG_TAGID"></span><span id="tag_tagid"></span><dl> <dt>**Balise \_ TAGID**</dt> <dt>( \| **type de balise 0x801 \_ \_ DWORD**)</dt> </dl>                                            | Attribut **TagId** .<br/>                                                                                  |



L’entrée suivante est de type **\_ \_ chaîne de type de balise** (0x8000).



| Constante/valeur                                                                                                                                                                                                                                                            | Description                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------|
| <span id="TAG_STRINGTABLE_ITEM"></span><span id="tag_stringtable_item"></span><dl> <dt>**Balise \_ \_Élément STRINGTABLE**</dt> <dt>( \| **chaîne de \_ type \_ de balise** 0x801)</dt> </dl> | Entrée d’élément de table de chaînes.<br/> |



Les entrées suivantes sont de type de **balise \_ \_ null** (0x1000).



| Constante/valeur                                                                                                                                                                                                                                                                            | Description                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| <span id="TAG_INCLUDE"></span><span id="tag_include"></span><dl> <dt>**Balise \_ INCLUDe**</dt> <dt>(0x1 \| , **type de balise \_ \_ null**)</dt> </dl>                                                 | Entrée de liste d’inclusion.<br/>                           |
| <span id="TAG_GENERAL"></span><span id="tag_general"></span><dl> <dt>**Balise \_ GÉNÉRAL**</dt> <dt>(0X2 \| **, \_ type \_ de balise null**)</dt> </dl>                                                 | Entrée de Shim à usage général.<br/>                   |
| <span id="TAG_MATCH_LOGIC_NOT"></span><span id="tag_match_logic_not"></span><dl> <dt>**Balise \_ Logique de correspondance \_ \_ not**</dt> <dt>( \| **type de balise 0x3 \_ \_ null**)</dt> </dl>                       | N’est pas une entrée de logique correspondante.<br/>                  |
| <span id="TAG_APPLY_ALL_SHIMS"></span><span id="tag_apply_all_shims"></span><dl> <dt>**Balise \_ APPLIQUER \_ tous les \_ shims**</dt> <dt>( \| **type de balise 0x4 \_ \_ null**)</dt> </dl>                       | Inutilisé.<br/>                                       |
| <span id="TAG_USE_SERVICE_PACK_FILES"></span><span id="tag_use_service_pack_files"></span><dl> <dt>**Balise \_ UTILISER \_ des \_ \_ fichiers de Service Pack**</dt> <dt>( \| **type de balise 0x5 \_ \_ null**)</dt> </dl> | Informations de Service Pack pour les entrées apphelp.<br/> |
| <span id="TAG_MITIGATION_OS"></span><span id="tag_mitigation_os"></span><dl> <dt>**Balise \_ \_Système d’exploitation d’atténuation**</dt> <dt>( \| **type de balise 0x6 \_ \_ null**)</dt> </dl>                              | Atténuation au niveau de l’entrée d’étendue du système d’exploitation.<br/>   |
| <span id="TAG_BLOCK_UPGRADE"></span><span id="tag_block_upgrade"></span><dl> <dt>**Balise \_ BLOQUER la \_ mise à niveau**</dt> <dt>( \| **type de balise 0x7 \_ \_ null**)</dt> </dl>                              | Mise à niveau de l’entrée de bloc.<br/>                          |
| <span id="TAG_INCLUDEEXCLUDEDLL"></span><span id="tag_includeexcludedll"></span><dl> <dt>**Balise \_ INCLUDEEXCLUDEDLL**</dt> <dt>( \| **type de balise 0x8 \_ \_ null**)</dt> </dl>                   | Entrée de DLL include/Exclude.<br/>                    |



Les entrées suivantes sont de type de **balise de type \_ \_ QWord** (0x5000).



| Constante/valeur                                                                                                                                                                                                                                                                                   | Description                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------|
| <span id="TAG_TIME"></span><span id="tag_time"></span><dl> <dt>**Balise \_ HEURE**</dt> <dt>(0x1 \| **type de balise \_ \_ QWord**)</dt> </dl>                                                                | Attribut d’heure.<br/>                                                                                     |
| <span id="TAG_BIN_FILE_VERSION"></span><span id="tag_bin_file_version"></span><dl> <dt>**Balise \_ \_ \_ Version du fichier bin**</dt> <dt>(0X2 \| **type de balise \_ \_ QWord**)</dt> </dl>                          | Attribut de version de fichier bin pour les entrées de fichier.<br/>                                                        |
| <span id="TAG_BIN_PRODUCT_VERSION"></span><span id="tag_bin_product_version"></span><dl> <dt>**Balise \_ \_ \_ Version du produit bin**</dt> <dt>( \| **type de balise 0x3 \_ \_ QWord**)</dt> </dl>                 | Attribut de version de produit bin pour les entrées de fichier.<br/>                                                     |
| <span id="TAG_MODTIME"></span><span id="tag_modtime"></span><dl> <dt>**Balise \_ MODTIME**</dt> <dt>( \| **type de balise 0x4 \_ \_ QWord**)</dt> </dl>                                                       | Inutilisé.<br/>                                                                                             |
| <span id="TAG_FLAG_MASK_KERNEL"></span><span id="tag_flag_mask_kernel"></span><dl> <dt>**Balise \_ \_ \_ Noyau du masque des indicateurs**</dt> <dt>( \| **type de balise 0x5 \_ \_ QWord**)</dt> </dl>                          | Attribut de masque de l’indicateur de noyau.<br/>                                                                         |
| <span id="TAG_UPTO_BIN_PRODUCT_VERSION"></span><span id="tag_upto_bin_product_version"></span><dl> <dt>**Balise \_ Jusqu’à la \_ \_ \_ version du produit bin**</dt> <dt>( \| **type de balise 0x6 \_ \_ QWord**)</dt> </dl> | Attribut de version de produit bin d’un fichier. La correspondance est effectuée jusqu’à cette version du produit, y compris.<br/> |
| <span id="TAG_DATA_QWORD"></span><span id="tag_data_qword"></span><dl> <dt>**Balise \_ DONNÉES \_ QWord**</dt> <dt>( \| **type de balise 0x7 \_ \_ QWord**)</dt> </dl>                                             | Attribut de valeur **ULONGLONG** pour une entrée de données.<br/>                                                     |
| <span id="TAG_FLAG_MASK_USER"></span><span id="tag_flag_mask_user"></span><dl> <dt>**Balise \_ \_ \_ Utilisateur de masque d’indicateur**</dt> <dt>(type de \| **balise 0x8 \_ \_ QWord**)</dt> </dl>                                | Attribut de masque de l’indicateur utilisateur.<br/>                                                                           |
| <span id="TAG_FLAGS_NTVDM1"></span><span id="tag_flags_ntvdm1"></span><dl> <dt>**Balise \_ FLAGs \_ NTVDM1**</dt> <dt>( \| **type de balise 0x9 \_ \_ QWord**)</dt> </dl>                                       | Attribut de masque de l’indicateur NTVDM1.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM2"></span><span id="tag_flags_ntvdm2"></span><dl> <dt>**Balise \_ FLAGs \_ NTVDM2**</dt> <dt>(0xA \| **type de balise \_ \_ QWord**)</dt> </dl>                                       | Attribut de masque de l’indicateur NTVDM2.<br/>                                                                         |
| <span id="TAG_FLAGS_NTVDM3"></span><span id="tag_flags_ntvdm3"></span><dl> <dt>**Balise \_ FLAGs \_ NTVDM3**</dt> <dt>( \| **type de balise 0xb \_ \_ QWord**)</dt> </dl>                                       | Attribut de masque de l’indicateur NTVDM3.<br/>                                                                         |
| <span id="TAG_FLAG_MASK_SHELL"></span><span id="tag_flag_mask_shell"></span><dl> <dt>**Balise \_ Indicateur \_ de \_ masque d’indicateur**</dt> <dt>( \| **type de balise 0xc \_ \_ QWord**)</dt> </dl>                             | Attribut de masque de l’indicateur de Shell.<br/>                                                                          |
| <span id="TAG_UPTO_BIN_FILE_VERSION"></span><span id="tag_upto_bin_file_version"></span><dl> <dt>**Balise \_ Jusqu’à la \_ \_ \_ version du fichier bin**</dt> <dt>( \| **type de balise 0xD- \_ \_ QWord**)</dt> </dl>          | Attribut de version de fichier bin d’un fichier. La correspondance est effectuée jusqu’à cette version de fichier, y compris.<br/>       |
| <span id="TAG_FLAG_MASK_FUSION"></span><span id="tag_flag_mask_fusion"></span><dl> <dt>**Balise \_ \_ \_ Fusion de masque d’indicateur**</dt> <dt>( \| **type de balise 0xE \_ \_ QWord**)</dt> </dl>                          | Attribut de masque de l’indicateur de fusion.<br/>                                                                         |
| <span id="TAG_FLAG_PROCESSPARAM"></span><span id="tag_flag_processparam"></span><dl> <dt>**Balise \_ FLAG \_ PROCESSPARAM**</dt> <dt>( \| **type de balise 0xF \_ \_ QWord**)</dt> </dl>                        | Attribut de l’indicateur du paramètre Process.<br/>                                                                       |
| <span id="TAG_FLAG_LUA"></span><span id="tag_flag_lua"></span><dl> <dt>**Balise \_ INDICATEUR \_ LUA**</dt> <dt>( \| **type de balise 0x10 \_ \_ QWord**)</dt> </dl>                                                  | Attribut de l’indicateur LUA.<br/>                                                                                 |
| <span id="TAG_FLAG_INSTALL"></span><span id="tag_flag_install"></span><dl> <dt>**Balise \_ INDICATEUR d' \_ installation**</dt> <dt>( \| **type de balise 0x11 \_ \_ QWord**)</dt> </dl>                                      | Attribut d’indicateur d’installation.<br/>                                                                             |



Les entrées suivantes sont de type de **balise \_ \_ Binary** (0x9000).



| Constante/valeur                                                                                                                                                                                                                                                     | Description                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| <span id="TAG_PATCH_BITS"></span><span id="tag_patch_bits"></span><dl> <dt>**Balise \_ PATCH \_ bits**</dt> <dt>(0X2 \| **type de balise \_ \_ binaire**)</dt> </dl>              | Attribut bits des fichiers correctifs.<br/>                          |
| <span id="TAG_FILE_BITS"></span><span id="tag_file_bits"></span><dl> <dt>**Balise \_ \_Bits de fichier**</dt> <dt>( \| **type de balise 0x3 \_ \_ binaire**)</dt> </dl>                 | Attribut bits de fichier.<br/>                                |
| <span id="TAG_EXE_ID"></span><span id="tag_exe_id"></span><dl> <dt>**Balise \_ \_ID exe**</dt> <dt>( \| **type de balise 0x4 \_ \_ binaire**)</dt> </dl>                          | Attribut **GUID** d’une entrée exécutable.<br/>          |
| <span id="TAG_DATA_BITS"></span><span id="tag_data_bits"></span><dl> <dt>**Balise \_ \_Bits de données**</dt> <dt>( \| **type de balise 0x5 \_ \_ binaire**)</dt> </dl>                 | Attribut de bits de données.<br/>                                |
| <span id="TAG_MSI_PACKAGE_ID"></span><span id="tag_msi_package_id"></span><dl> <dt>**Balise \_ \_ \_ ID de package MSI**</dt> <dt>( \| **type de balise 0x6, \_ \_ binaire**)</dt> </dl> | Attribut d’identificateur de package MSI d’un package MSI.<br/> |
| <span id="TAG_DATABASE_ID"></span><span id="tag_database_id"></span><dl> <dt>**Balise \_ \_ID de base de données**</dt> <dt>( \| **type de balise 0x7 \_ \_ binaire**)</dt> </dl>           | Attribut **GUID** d’une base de données.<br/>                   |
| <span id="TAG_INDEX_BITS"></span><span id="tag_index_bits"></span><dl> <dt>**Balise \_ \_Bits d’index**</dt> <dt>( \| **type de balise 0x801 \_ \_ binaire**)</dt> </dl>            | Attribut bits d’index.<br/>                               |



Les entrées suivantes sont de type **\_ \_ mot de type de balise** (0x3000).



| Constante/valeur                                                                                                                                                                                                                                      | Description                                        |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------|
| <span id="TAG_MATCH_MODE"></span><span id="tag_match_mode"></span><dl> <dt>**Balise \_ MATCH \_ mode**</dt> <dt>(0x1 \| **type de balise \_ \_ Word**)</dt> </dl> | Attribut de mode de correspondance.<br/>                   |
| <span id="TAG_TAG"></span><span id="tag_tag"></span><dl> <dt>**Balise \_ TAG**</dt> <dt>( \| **mot de \_ type \_ de balise** 0x801)</dt> </dl>                     | Entrée de BALIse.<br/>                              |
| <span id="TAG_INDEX_TAG"></span><span id="tag_index_tag"></span><dl> <dt>**Balise \_ \_Étiquette d’index**</dt> <dt>( \| **\_ \_ mot de type de balise** 0x802)</dt> </dl>  | Attribut de BALIse d’index pour une entrée d’index.<br/> |
| <span id="TAG_INDEX_KEY"></span><span id="tag_index_key"></span><dl> <dt>**Balise \_ \_Clé d’index**</dt> <dt>( \| **\_ \_ mot de type de balise** 0x803)</dt> </dl>  | Attribut de clé d’index pour une entrée d’index.<br/> |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|----------------------------------------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Exposeenums2managed. h (inclure Axextendenums. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Types de BALISes](tag-types.md)
</dt> <dt>

[**TAGID**](tagid.md)
</dt> <dt>

[**TAGREF**](tagref.md)
</dt> </dl>

 

 




