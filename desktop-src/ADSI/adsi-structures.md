---
title: Structures ADSI
description: Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les structures listées dans le tableau suivant.
ms.assetid: 3ee0e469-9932-4135-8798-27d318011786
ms.tgt_platform: multiple
keywords:
- ADSI ADSI, référence, structures
- structures ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c8c954f55ef53cc1607957a9251ec960908a981ce33e2166f45eef42251abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962178"
---
# <a name="adsi-structures"></a>Structures ADSI

Les interfaces ADSI (Active Directory Service Interfaces) définissent et utilisent les structures listées dans le tableau suivant.



| Structure                                                                      | Description                                                                                                    |
|--------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [**\_définition d’attr ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_attr_def)<br/>                              | Décrit un ensemble de définitions d’attribut d’un objet **attributeSchema** .<br/>                          |
| [**\_infos attr \_ ads**](/windows/desktop/api/Iads/ns-iads-ads_attr_info)<br/>                            | Contient la valeur d’un attribut nommé et spécifie les opérations de modification de l’attribut.<br/>              |
| [**\_lien secondaire ads**](/windows/win32/api/iads/ns-iads-ads_backlink)<br/>                               | Représente une représentation ADSI de l’attribut de **lien précédent** .<br/>                                   |
| [**\_liste des CASEIGNORE ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_caseignore_list)<br/>                | Représente une représentation ADSI de l’attribut de **liste de cas ignore** .<br/>                            |
| [**\_définition de classe ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_class_def)<br/>                            | Décrit les données de schéma pour un objet.<br/>                                                                |
| [**\_DN ADS \_ avec \_ binaire**](/windows/win32/api/iads/ns-iads-ads_dn_with_binary)<br/>                 | Structure définie par l’interface ADSI qui mappe un nom unique à un **GUID** d’objet.<br/>                     |
| [**\_DN ADS \_ avec \_ chaîne**](/windows/win32/api/iads/ns-iads-ads_dn_with_string)<br/>                 | Structure définie par l’interface ADSI qui mappe un nom unique d’un objet à une valeur de chaîne non différente.<br/> |
| [**\_E-mail ads**](/windows/win32/api/iads/ns-iads-ads_email)<br/>                                     | Représente une représentation ADSI de l’attribut de **messagerie** .<br/>                                       |
| [**\_FAXNUMBER ads**](/windows/win32/api/iads/ns-iads-ads_faxnumber)<br/>                             | Représente une représentation ADSI de l’attribut de **numéro de téléphone de télécopie** .<br/>                  |
| [**les annonces sont \_ conservées**](/windows/win32/api/iads/ns-iads-ads_hold)<br/>                                       | Représente une représentation ADSI de l’attribut **Hold** .<br/>                                        |
| [**ADRESSE de publicité ADS \_**](/windows/win32/api/iads/ns-iads-ads_netaddress)<br/>                           | Représente une représentation ADSI de l’attribut d' **adresse net** .<br/>                                 |
| [**\_descripteur de sécurité NT ADS \_ \_**](/windows/win32/api/iads/ns-iads-ads_nt_security_descriptor)<br/> | Décrit un descripteur de sécurité.<br/>                                                                    |
| [**\_infos objet \_ ads**](/windows/desktop/api/Iads/ns-iads-ads_object_info)<br/>                        | Décrit les données d’objet du service d’annuaire.<br/>                                                            |
| [**\_liste des octets ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_octet_list)<br/>                          | Représente une représentation ADSI de l’attribut de **liste d’octets** .<br/>                                  |
| [**\_chaîne d’octets ADS \_**](/windows/win32/api/iads/ns-iads-ads_octet_string)<br/>                      | Représente une représentation ADSI de l’attribut de **chaîne d’octets** .<br/>                                |
| [**\_chemin d’accès ads**](/windows/win32/api/iads/ns-iads-ads_path)<br/>                                       | Représente une représentation ADSI de l’attribut **path** .<br/>                                        |
| [**\_POSTALADDRESS ads**](/windows/win32/api/iads/ns-iads-ads_postaladdress)<br/>                     | Représente une représentation ADSI de l’attribut **adresse postale** .<br/>                              |
| [**PUBLICITÉS \_ \_ spécifiques**](/windows/win32/api/iads/ns-iads-ads_prov_specific)<br/>                    | Décrit un type de données spécifique au fournisseur.<br/>                                                            |
| [**\_REPLICAPOINTER ads**](/windows/win32/api/iads/ns-iads-ads_replicapointer)<br/>                   | Représente une représentation ADSI de l’attribut du pointeur de réplica.<br/>                                 |
| [**\_colonne de recherche ADS \_**](/windows/desktop/api/Iads/ns-iads-ads_search_column)<br/>                    | Représente une colonne résultant d’une requête de répertoire.<br/>                                               |
| [**\_info SEARCHPREF \_ ads**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info)<br/>                | Décrit les préférences de requête.<br/>                                                                        |
| [**\_SortKey ads**](/windows/desktop/api/Iads/ns-iads-ads_sortkey)<br/>                                 | Décrit la clé de tri utilisée pour trier une requête.<br/>                                                    |
| [**\_horodateur ads**](/windows/win32/api/iads/ns-iads-ads_timestamp)<br/>                             | Représente une représentation ADSI de l’attribut **timestamp** .<br/>                                   |
| [**\_TYPEDNAME ads**](/windows/win32/api/iads/ns-iads-ads_typedname)<br/>                             | Représente une représentation ADSI de l’attribut de **nom typé** .<br/>                                  |
| [**ADSVALUE**](/windows/desktop/api/Iads/ns-iads-adsvalue)<br/>                                        | Décrit la valeur d’un type de données ADSI.<br/>                                                           |
| [**\_VLV ads**](/windows/desktop/api/Iads/ns-iads-ads_vlv)<br/>                                         | Spécifie que l’affichage de liste virtuelle doit être utilisé lors du retour des résultats de recherche à partir du serveur.<br/>  |



 

 

 





