---
title: Énumérations ADSI
description: Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les énumérations listées dans le tableau suivant.
ms.assetid: f0ad5ce5-742d-40dc-ac5a-31d779e40bfd
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, référence, énumérations
- Énumérations ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c10d5aed5688e7128a64a32dee2f83efa22ab5bf292231517026299ccb592886
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119023907"
---
# <a name="adsi-enumerations"></a>Énumérations ADSI

Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les énumérations listées dans le tableau suivant.



| Énumération                                                           | Description                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ \_ énumération ACEFLAG ads**](/windows/win32/api/iads/ne-iads-ads_aceflag_enum)                        | Spécifie comment la sécurité se propage pour les entrées de contrôle d’accès (ACE) héritées et les types d’audit pour une entrée du contrôle d’accès système.                                                                                                                                             |
| [**\_ \_ énumération ACETYPE ads**](/windows/win32/api/iads/ne-iads-ads_acetype_enum)                        | Spécifie le type d’entrée du contrôle d’accès.                                                                                                                                                                                                                                           |
| [**\_énumération d’authentification ADS \_**](/windows/win32/api/iads/ne-iads-ads_authentication_enum)          | Spécifie le niveau de sécurité utilisé pour l’authentification d’un client.                                                                                                                                                                                                     |
| [**\_ \_ énumérations de références de Chase ADS \_**](/windows/win32/api/iads/ne-iads-ads_chase_referrals_enum)       | Spécifie le comportement du repérage de références.                                                                                                                                                                                                                       |
| [**\_DEREFENUM ads**](/windows/win32/api/iads/ne-iads-ads_derefenum)                               | Spécifie le comportement du déréférencement des alias.                                                                                                                                                                                                                    |
| [**\_énumération d’affichage ADS \_**](/windows/win32/api/iads/ne-iads-ads_display_enum)                        | Spécifie le mode d’affichage d’un tracé.                                                                                                                                                                                                                                |
| [**\_ \_ énumération du mode d’échappement ADS \_**](/windows/win32/api/iads/ne-iads-ads_escape_mode_enum)               | Spécifie si les caractères spéciaux sont placés dans une séquence d’échappement, sans séquence d’échappement ou sans toucher.                                                                                                                                                                                        |
| [**\_ \_ énumération FLAGTYPE ads**](/windows/win32/api/iads/ne-iads-ads_flagtype_enum)                      | Spécifie la présence des champs **ObjectType** ou **INHERITEDOBJECTTYPE** dans une entrée du contrôle d’accès.                                                                                                                                                                         |
| [**\_énumération de format ADS \_**](/windows/win32/api/iads/ne-iads-ads_format_enum)                          | Spécifie le type de valeurs dans un objet PathName.                                                                                                                                                                                                                |
| [**\_ \_ énumération de type de groupe ADS \_**](/windows/win32/api/iads/ne-iads-ads_group_type_enum)                 | Spécifie le type de groupe du membre.                                                                                                                                                                                                                           |
| [**\_nom ADS \_ INITTYPE \_ enum**](/windows/win32/api/iads/ne-iads-ads_name_inittype_enum)           | Spécifie le type d’initialisation à effectuer sur un objet translate de nom.                                                                                                                                                                                  |
| [**\_ \_ énumération de type de nom ADS \_**](/windows/win32/api/iads/ne-iads-ads_name_type_enum)                   | Spécifie le format utilisé pour représenter les noms uniques.                                                                                                                                                                                                       |
| [**\_énumération des options ADS \_**](/windows/win32/api/iads/ne-iads-ads_option_enum)                          | Spécifie les options disponibles que l’interface [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions) utilise pour manipuler les objets d’annuaire.                                                                                                                        |
| [**\_enum de \_ codage de mot de passe ADS \_**](/windows/win32/api/iads/ne-iads-ads_password_encoding_enum)   | Utilisé pour identifier le type d’encodage de mot de passe utilisé avec l’option de méthode de mot de passe de l' **\_ option \_ \_ ADS** dans les méthodes [**IADsObjectOptions :: GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) et [**IADsObjectOptions :: SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) . |
| [**\_ \_ énumération PATHTYPE ads**](/windows/win32/api/iads/ne-iads-ads_pathtype_enum)                      | Spécifie le type d’objet sur lequel le descripteur de sécurité est modifié.                                                                                                                                                                                        |
| [**\_énumération des préférences ADS \_**](/windows/win32/api/iads/ne-iads-ads_preferences_enum)                | Spécifie les préférences de requête de la OLE DB pour l’interface ADSI.                                                                                                                                                                                                           |
| [**ENUM de l' \_ opération de propriété ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_property_operation_enum) | Spécifie les façons de mettre à jour les valeurs de propriété dans le cache de propriétés.                                                                                                                                                                                               |
| [**\_énumération des droits ADS \_**](/windows/win32/api/iads/ne-iads-ads_rights_enum)                          | Spécifie les droits d’accès à un objet de service d’annuaire.                                                                                                                                                                                                        |
| [**\_SCOPEENUM ads**](/windows/win32/api/iads/ne-iads-ads_scopeenum)                               | Spécifie l’étendue d’une recherche dans les annuaires.                                                                                                                                                                                                                        |
| [**\_enum du \_ contrôle \_ SD ads**](/windows/win32/api/iads/ne-iads-ads_sd_control_enum)                 | Spécifie qu’une liste de contrôle d’accès (ACL) doit être protégée lorsque de nouvelles autorisations sont appliquées de manière récursive à une arborescence de répertoires.                                                                                                                                  |
| [**\_enum de \_ format \_ SD ads**](/windows/win32/api/iads/ne-iads-ads_sd_format_enum)                   | Spécifie le format de conversion du descripteur de sécurité.                                                                                                                                                                                                      |
| [**\_énumération de la révision SD ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_sd_revision_enum)               | Spécifie le numéro de révision d’une entrée de contrôle d’accès ou d’une liste ACL.                                                                                                                                                                                                                   |
| [**\_ \_ énumération SEARCHPREF ads**](/windows/win32/api/iads/ne-iads-ads_searchpref_enum)                  | Spécifie les préférences de la recherche.                                                                                                                                                                                                                              |
| [**\_ \_ énumération des informations de sécurité ADS \_**](/windows/win32/api/iads/ne-iads-ads_security_info_enum)           | Spécifie les options d’examen des données de sécurité.                                                                                                                                                                                                                |
| [**\_ \_ énumération SETTYPE ads**](/windows/win32/api/iads/ne-iads-ads_settype_enum)                        | Spécifie le format du chemin d’accès dans [**IADsPathname :: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set).                                                                                                                                                                                       |
| [**\_STATUSENUM ads**](/windows/win32/api/iads/ne-iads-ads_statusenum)                             | Spécifie l’état des préférences de recherche.                                                                                                                                                                                                                       |
| [**\_ \_ énumération systemFlags ads**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)                  | Spécifie les types d’attributs représentés par un objet **attributeSchema** .                                                                                                                                                                                   |
| [**ENUM de l' \_ indicateur utilisateur ADS \_ \_**](/windows/win32/api/iads/ne-iads-ads_user_flag_enum)                   | Spécifie les indicateurs utilisés pour manipuler les propriétés de l’utilisateur.                                                                                                                                                                                                            |
| [**\_énumération de dialecte ADSI \_**](/windows/win32/api/iads/ne-iads-adsi_dialect_enum)                      | Spécifie les dialectes de requête ADSI disponibles.                                                                                                                                                                                                                          |
| [**ADSTYPEENUM**](/windows/win32/api/iads/ne-iads-adstypeenum)                                    | Spécifie les types de données utilisés pour interpréter une chaîne de syntaxe étendue ADSI.                                                                                                                                                                                            |



 

## <a name="remarks"></a>Remarques

étant donné que les applications Visual Basic scripting Edition ne peuvent pas lire les données d’une bibliothèque de types, les applications VBScript ne peuvent pas reconnaître les constantes symboliques telles qu’elles sont définies dans ces énumérations. Utilisez plutôt les constantes numériques pour définir les indicateurs appropriés dans une application VBScript. Pour utiliser les constantes symboliques comme bonne pratique de programmation, écrivez des déclarations explicites de telles constantes, comme cela est fait ici dans les applications VBScript.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)
</dt> <dt>

[**IADsPathname :: Set**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)
</dt> </dl>

 

 




