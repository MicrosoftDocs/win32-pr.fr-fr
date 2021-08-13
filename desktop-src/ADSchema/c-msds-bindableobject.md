---
title: ms-DS-Bindable-classe d’objets
description: Classe auxiliaire pour représenter un objet pouvant être lié. Toute classe définie par l’utilisateur qui représente une entité qui peut être utilisée pour établir une liaison avec le répertoire (c’est-à-dire un utilisateur) doit inclure cette classe auxiliaire.
ms.assetid: 181b3e2b-9442-4f11-9af7-4697491115f3
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe d’objets pouvant être liée par ms-DS
- Schéma AD de la classe msDS-BindableObject
topic_type:
- apiref
api_name:
- ms-DS-Bindable-Object
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b702a26c61920f5a3868ccc479b1f8578a3075907b5dc5bc2eb9d070321c91d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118680779"
---
# <a name="ms-ds-bindable-object-class"></a>ms-DS-Bindable-classe d’objets

Classe auxiliaire pour représenter un objet pouvant être lié. Toute classe définie par l’utilisateur qui représente une entité qui peut être utilisée pour établir une liaison avec le répertoire (c’est-à-dire un utilisateur) doit inclure cette classe auxiliaire.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-Bindable-objet                |
| LDAP-Display-Name | msDS-BindableObject                  |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | 89f4a69f-4416-6b49-821d-6e3c4a0ff802 |



## <a name="implementations"></a>Implémentations

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)



| Entrée | Valeur |
|-----------------------------|--------------------------------------------------------------|
| System-Only                 | False                                                        |
| Object-Category             | 3                                                            |
| Default-Object-catégorie     | \-                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.244                                       |
| Valeur de masquage par défaut        | 1                                                            |
| RDN-att-ID                  | \-                                                           |
| Sous-classe de                 | [**Sécurité-principal**](c-securityprincipal.md)<br/> |
| Supérieurs possibles          | \-                                                           |
| Classes auxiliaires           | \-                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                 |
| Descripteur de sécurité par défaut | \-                                                           |
| System-Flags                | 0x00000010                                                   |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                                      | Obligatoire | Dérivé de                                                                                 |
|------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Compte-expire**](a-accountexpires.md)                                                    | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Administrateur-Description**](a-admindescription.md)                                                | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                              | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                           | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Mot de passe incorrect**](a-badpasswordtime.md)                                                 | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Nombre de mot de passe incorrect**](a-badpwdcount.md)                                                         | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                  | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom canonique**](a-canonicalname.md)                                                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom commun**](a-cn.md)                                                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Date et heure de création**](a-createtimestamp.md)                                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Description**](a-description.md)                                                           | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom complet**](a-displayname.md)                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DSA-signature**](a-dsasignature.md)                                                        | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Entrée de**](a-fromentry.md)                                                              | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                     | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Type d’instance**](a-instancetype.md)                                                        | True      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est supprimé**](a-isdeleted.md)                                                              | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Last-Logon-timestamp**](a-lastlogontimestamp.md)                                           | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Temps de verrouillage**](a-lockouttime.md)                                                          | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Objets managés**](a-managedobjects.md)                                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Masterisé-par**](a-masteredby.md)                                                            | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                       | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                     | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-auto-verrouillé**](a-ms-ds-useraccountautolocked.md)                        | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)            | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-Account-désactivé**](a-msds-useraccountdisabled.md)                              | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-no-expire-Password**](a-msds-userdontexpirepassword.md)                       | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-mot de passe-expiré**](a-msds-userpasswordexpired.md)                              | False     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-mot de passe-non-requis**](a-ms-ds-userpasswordnotrequired.md)                    | False     | **ms-DS-Bindable-objet**                                                                    |
| [**NT-pwd-historique**](a-ntpwdhistory.md)                                                       | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                       | True      | [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                                    | True      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Classe d’objet**](a-objectclass.md)                                                          | True      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**GUID de l’objet**](a-objectguid.md)                                                            | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID de l’objet**](a-objectsid.md)                                                              | True      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Version de l’objet**](a-objectversion.md)                                                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Possible-inférieur**](a-possibleinferiors.md)                                              | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                             | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Pwd-dernier jeu**](a-pwdlastset.md)                                                           | False     | **ms-DS-Bindable-objet**                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                     | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**UNIQUE**](a-name.md)                                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                      | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                           | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                                | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à**](a-repsto.md)                                                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Faisant**](a-revision.md)                                                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                             | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                             | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                                 | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                       | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                     | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Sous-Références**](a-subrefs.md)                                                                  | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                                  | False     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Indicateurs système**](a-systemflags.md)                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Jetons-groupes**](a-tokengroups.md)                                                          | False     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-pwd**](a-unicodepwd.md)                                                            | False     | **ms-DS-Bindable-objet**                                                                    |
| [**USN-modifié**](a-usnchanged.md)                                                            | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Créé par USN**](a-usncreated.md)                                                            | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                     | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-intersite**](a-usnintersite.md)                                                        | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                    | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-source**](a-usnsource.md)                                                              | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Chemin WBEM**](a-wbempath.md)                                                                | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                               | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**En cas de modification**](a-whenchanged.md)                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Lors de la création**](a-whencreated.md)                                                          | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                         | False     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page-autres**](a-url.md)                                                                | False     | [**Retour au début**](c-top.md)<br/>                                                              |



 

 





