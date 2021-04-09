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
ms.openlocfilehash: feb69036ad9cd33b8f0a60f5356192acbea8dd71
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103844841"
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
| System-Only                 | Faux                                                        |
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
| [**Compte-expire**](a-accountexpires.md)                                                    | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Administrateur-Description**](a-admindescription.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Mot de passe incorrect**](a-badpasswordtime.md)                                                 | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Nombre de mot de passe incorrect**](a-badpwdcount.md)                                                         | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom canonique**](a-canonicalname.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom commun**](a-cn.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Date et heure de création**](a-createtimestamp.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Description**](a-description.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom complet**](a-displayname.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DSA-signature**](a-dsasignature.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Entrée de**](a-fromentry.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Type d’instance**](a-instancetype.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est supprimé**](a-isdeleted.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Last-Logon-timestamp**](a-lastlogontimestamp.md)                                           | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Temps de verrouillage**](a-lockouttime.md)                                                          | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Objets managés**](a-managedobjects.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Masterisé-par**](a-masteredby.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-User-Account-auto-verrouillé**](a-ms-ds-useraccountautolocked.md)                        | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-compte-contrôle-calculé**](a-msds-user-account-control-computed.md)            | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-Account-désactivé**](a-msds-useraccountdisabled.md)                              | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-no-expire-Password**](a-msds-userdontexpirepassword.md)                       | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-User-Encrypted-Text-Password-allowed**](a-ms-ds-userencryptedtextpasswordallowed.md) | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-mot de passe-expiré**](a-msds-userpasswordexpired.md)                              | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**ms-DS-utilisateur-mot de passe-non-requis**](a-ms-ds-userpasswordnotrequired.md)                    | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**NT-pwd-historique**](a-ntpwdhistory.md)                                                       | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                       | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Classe d’objet**](a-objectclass.md)                                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**GUID de l’objet**](a-objectguid.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID de l’objet**](a-objectsid.md)                                                              | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Version de l’objet**](a-objectversion.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Possible-inférieur**](a-possibleinferiors.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Pwd-dernier jeu**](a-pwdlastset.md)                                                           | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**UNIQUE**](a-name.md)                                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à**](a-repsto.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Faisant**](a-revision.md)                                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Sous-Références**](a-subrefs.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                                  | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Indicateurs système**](a-systemflags.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Jetons-groupes**](a-tokengroups.md)                                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Unicode-pwd**](a-unicodepwd.md)                                                            | Faux     | **ms-DS-Bindable-objet**                                                                    |
| [**USN-modifié**](a-usnchanged.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Créé par USN**](a-usncreated.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-intersite**](a-usnintersite.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-source**](a-usnsource.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Chemin WBEM**](a-wbempath.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**En cas de modification**](a-whenchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Lors de la création**](a-whencreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page-autres**](a-url.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |



 

 





