---
title: Group (classe)
description: Stocke une liste de noms d’utilisateurs. Utilisé pour appliquer des principaux de sécurité sur les ressources.
ms.assetid: e8ce5c43-d0fb-4c67-a6ef-7094fb7e7669
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe de groupe
- Schéma AD de la classe de groupe
topic_type:
- apiref
api_name:
- Group
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eae33b53eff8305fee4698c5aed2bb072f3fa5b90a5922d0099e40e90f9b3fe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021907"
---
# <a name="group-class"></a>Group (classe)

Stocke une liste de noms d’utilisateurs. Utilisé pour appliquer des principaux de sécurité sur les ressources.



| Entrée | Valeur |
|-------------------|------------------------------------------------|
| CN                | Groupe                                          |
| LDAP-Display-Name | group                                          |
| Mettre à jour le privilège  | Cette valeur est définie par l’administrateur de domaine. |
| Fréquence des mises à jour  | \-                                             |
| Schema-ID-GUID    | bf967a9c-0de6-11d0-a285-00aa003049e2           |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributs](#windows-2000-server-attributes)
-   [Droits étendus](#windows-2000-server-extended-rights)
-   [Écritures validées](#windows-2000-server-validated-writes)
-   [Jeux de propriétés](#windows-2000-server-property-sets)



| Entrée | Valeur |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                               |
| Object-Category             | 1                                                                                                                                                                                                   |
| Default-Object-catégorie     | \-                                                                                                                                                                                                  |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                   |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                              |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                     |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**conteneur**](c-container.md) [**d’unité d’organisation**](c-organizationalunit.md)DNS [**BuiltIn-domaine**](c-builtindomain.md)                                       |
| Classes auxiliaires           | [**Sécurité-**](c-securityprincipal.md) destinataire (système)[**e-mail-destinataire**](c-mailrecipient.md) (système)                                                                                        |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                        |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; UA |
| System-Flags                | 0x00000010                                                                                                                                                                                          |



## <a name="windows-2000-server-attributes"></a>attributs de serveur Windows 2000

cette classe contient les attributs suivants pour Windows serveur 2000 :



| Attribut                                                                    | Obligatoire | Dérivé de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Nombre d’administrateurs**](a-admincount.md)                                          | Faux     | **Groupe**                                                                                    |
| [**Administrateur-Description**](a-admindescription.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-attributs**](a-allowedattributes.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                   | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom canonique**](a-canonicalname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Commentaire**](a-info.md)                                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Nom commun**](a-cn.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>         |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                       | Faux     | **Groupe**                                                                                    |
| [**Date et heure de création**](a-createtimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Description**](a-description.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Bureau-profil**](a-desktopprofile.md)                                  | Faux     | **Groupe**                                                                                    |
| [**Nom complet**](a-displayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DSA-signature**](a-dsasignature.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses de messagerie**](a-mail.md)                                           | Faux     | **Groupe**                                                                                    |
| [**Nom de l’extension**](a-extensionname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Indicateurs**](a-flags.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Entrée de**](a-fromentry.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Groupe-attributs**](a-groupattributes.md)                                | Faux     | **Groupe**                                                                                    |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                         | Faux     | **Groupe**                                                                                    |
| [**Type de groupe**](a-grouptype.md)                                            | Vrai      | **Groupe**                                                                                    |
| [**Type d’instance**](a-instancetype.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est supprimé**](a-isdeleted.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Géré par**](a-managedby.md)                                            | Faux     | **Groupe**                                                                                    |
| [**Objets managés**](a-managedobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Masterisé-par**](a-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Membre**](a-member.md)                                                   | Faux     | **Groupe**                                                                                    |
| [**Date et heure de modification**](a-modifytimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                           | Faux     | **Groupe**                                                                                    |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**NT-Group-members**](a-ntgroupmembers.md)                                 | Faux     | **Groupe**                                                                                    |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                     | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Classe d’objet**](a-objectclass.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**GUID de l’objet**](a-objectguid.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID de l’objet**](a-objectsid.md)                                            | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Version de l’objet**](a-objectversion.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Opérateur-nombre**](a-operatorcount.md)                                    | Faux     | **Groupe**                                                                                    |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Possible-inférieur**](a-possibleinferiors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Faux     | **Groupe**                                                                                    |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**UNIQUE**](a-name.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Rapports**](a-directreports.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à**](a-repsto.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Faisant**](a-revision.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**RID**](a-rid.md)                                                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Nom de compte SAM**](a-samaccountname.md)                                 | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Type de compte SAM**](a-samaccounttype.md)                                 | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Identificateur de sécurité**](a-securityidentifier.md)                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID-historique**](a-sidhistory.md)                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Site-objet-BL**](a-siteobjectbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Sous-Références**](a-subrefs.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Indicateurs système**](a-systemflags.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Numéro de téléphone**](a-telephonenumber.md)                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Jetons-groupes**](a-tokengroups.md)                                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md) | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Utilisateur-certificat**](a-usercert.md)                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**USN-modifié**](a-usnchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Créé par USN**](a-usncreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-intersite**](a-usnintersite.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-source**](a-usnsource.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Chemin WBEM**](a-wbempath.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Objets bien connus**](a-wellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**En cas de modification**](a-whenchanged.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Lors de la création**](a-whencreated.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page-autres**](a-url.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-2000-server-extended-rights"></a>droits étendus du serveur Windows 2000

cette classe contient les droits étendus suivants pour Windows serveur 2000 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-2000-server-validated-writes"></a>écritures validées par le serveur Windows 2000

cette classe contient les écritures validées suivantes pour Windows serveur 2000 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-2000-server-property-sets"></a>jeux de propriétés de serveur Windows 2000

cette classe contient les jeux de propriétés suivants pour Windows serveur 2000 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)
-   [Droits étendus](#windows-server-2003-extended-rights)
-   [Écritures validées](#windows-server-2003-validated-writes)
-   [Jeux de propriétés](#windows-server-2003-property-sets)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-catégorie     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Supérieurs possibles          | [**Domaine-Domain DNS**](c-domaindns.md)[](c-organizationalunit.md)[**BuiltIn-domaine**](c-builtindomain.md)[**conteneur**](c-container.md)[**ms-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes auxiliaires           | [**Sécurité-**](c-securityprincipal.md) destinataire (système)[**e-mail-destinataire**](c-mailrecipient.md) (système)                                                                                                                                                                                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                     |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; AU) (OA ;; RP ; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2 ;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-attributes"></a>Windows Attributs du serveur 2003

cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                    | Obligatoire | Dérivé de                                                                                 |
|------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Nombre d’administrateurs**](a-admincount.md)                                          | Faux     | **Groupe**                                                                                    |
| [**Administrateur-Description**](a-admindescription.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-attributs**](a-allowedattributes.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                   | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom canonique**](a-canonicalname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Commentaire**](a-info.md)                                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Nom commun**](a-cn.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>         |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                       | Faux     | **Groupe**                                                                                    |
| [**Date et heure de création**](a-createtimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Description**](a-description.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Bureau-profil**](a-desktopprofile.md)                                  | Faux     | **Groupe**                                                                                    |
| [**Nom complet**](a-displayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DSA-signature**](a-dsasignature.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses de messagerie**](a-mail.md)                                           | Faux     | **Groupe**                                                                                    |
| [**Nom de l’extension**](a-extensionname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Indicateurs**](a-flags.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Entrée de**](a-fromentry.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Groupe-attributs**](a-groupattributes.md)                                | Faux     | **Groupe**                                                                                    |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                         | Faux     | **Groupe**                                                                                    |
| [**Type de groupe**](a-grouptype.md)                                            | Vrai      | **Groupe**                                                                                    |
| [**Type d’instance**](a-instancetype.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est supprimé**](a-isdeleted.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**labeledURI**](a-labeleduri.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Dernier-parent connu**](a-lastknownparent.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Géré par**](a-managedby.md)                                            | Faux     | **Groupe**                                                                                    |
| [**Objets managés**](a-managedobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Masterisé-par**](a-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Membre**](a-member.md)                                                   | Faux     | **Groupe**                                                                                    |
| [**Date et heure de modification**](a-modifytimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-AZ-LDAP-requête**](a-msds-azldapquery.md)                            | Faux     | **Groupe**                                                                                    |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-non-membres**](a-msds-nonmembers.md)                               | Faux     | **Groupe**                                                                                    |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                           | Faux     | **Groupe**                                                                                    |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**NT-Group-members**](a-ntgroupmembers.md)                                 | Faux     | **Groupe**                                                                                    |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                     | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Classe d’objet**](a-objectclass.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**GUID de l’objet**](a-objectguid.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID de l’objet**](a-objectsid.md)                                            | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Version de l’objet**](a-objectversion.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Opérateur-nombre**](a-operatorcount.md)                                    | Faux     | **Groupe**                                                                                    |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Possible-inférieur**](a-possibleinferiors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Faux     | **Groupe**                                                                                    |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**UNIQUE**](a-name.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Rapports**](a-directreports.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à**](a-repsto.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Faisant**](a-revision.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**RID**](a-rid.md)                                                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Nom de compte SAM**](a-samaccountname.md)                                 | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Type de compte SAM**](a-samaccounttype.md)                                 | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**secretary**](a-secretary.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Identificateur de sécurité**](a-securityidentifier.md)                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID-historique**](a-sidhistory.md)                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Site-objet-BL**](a-siteobjectbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Sous-Références**](a-subrefs.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Indicateurs système**](a-systemflags.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Numéro de téléphone**](a-telephonenumber.md)                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**Jetons-groupes**](a-tokengroups.md)                                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md) | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Utilisateur-certificat**](a-usercert.md)                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |
| [**USN-modifié**](a-usnchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Créé par USN**](a-usncreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-intersite**](a-usnintersite.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-source**](a-usnsource.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Chemin WBEM**](a-wbempath.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Objets bien connus**](a-wellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**En cas de modification**](a-whenchanged.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Lors de la création**](a-whencreated.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page-autres**](a-url.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**X509-CERT**](a-usercertificate.md)                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                         |



## <a name="windows-server-2003-extended-rights"></a>Windows Droits étendus du serveur 2003

cette classe contient les droits étendus suivants pour Windows Server 2003 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-server-2003-validated-writes"></a>Windows Serveur 2003 écritures validées

cette classe contient les écritures validées suivantes pour Windows Server 2003 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-server-2003-property-sets"></a>Windows Jeux de propriétés du serveur 2003

cette classe contient les jeux de propriétés suivants pour Windows Server 2003 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)
-   [Écritures validées](#adam-validated-writes)
-   [Jeux de propriétés](#adam-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                |
| Object-Category             | 1                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                 |
| Valeur de masquage par défaut        | 0                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                               |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                      |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**conteneur**](c-container.md) [**d’unité d’organisation**](c-organizationalunit.md)DNS |
| Classes auxiliaires           | [**Sécurité principale**](c-securityprincipal.md) (système)                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                         |
| Descripteur de sécurité par défaut | D:S:                                                                                                                 |
| System-Flags                | 0x00000010                                                                                                           |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                   | Obligatoire | Dérivé de                                                                                 |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Bureau-profil**](a-desktopprofile.md)                                 | Faux     | **Groupe**                                                                                    |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Type de groupe**](a-grouptype.md)                                           | Vrai      | **Groupe**                                                                                    |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Géré par**](a-managedby.md)                                           | Faux     | **Groupe**                                                                                    |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Membre**](a-member.md)                                                  | Faux     | **Groupe**                                                                                    |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                              |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SID de l’objet**](a-objectsid.md)                                           | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                          | Faux     | **Groupe**                                                                                    |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)               | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Jetons-groupes**](a-tokengroups.md)                                       | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                 |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                              |



## <a name="adam-validated-writes"></a>Écritures validées par ADAM

Cette classe contient les écritures validées suivantes pour ADAM :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="adam-property-sets"></a>Jeux de propriétés ADAM

Cette classe contient les jeux de propriétés suivants pour ADAM :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)
-   [Droits étendus](#windows-server-2003-r2-extended-rights)
-   [Écritures validées](#windows-server-2003-r2-validated-writes)
-   [Jeux de propriétés](#windows-server-2003-r2-property-sets)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-catégorie     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Supérieurs possibles          | [**Domaine-Domain DNS**](c-domaindns.md)[](c-organizationalunit.md)[**BuiltIn-domaine**](c-builtindomain.md)[**conteneur**](c-container.md)[**ms-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes auxiliaires           | [**posixgroup**](c-posixgroup.md)[**sécurité-principal**](c-securityprincipal.md) (système)[**messagerie-destinataire**](c-mailrecipient.md) (système)                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                     |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; AU) (OA ;; RP ; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2 ;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributs du serveur 2003 R2

cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                    | Obligatoire | Dérivé de                                                                                                                       |
|------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre d’administrateurs**](a-admincount.md)                                          | Faux     | **Groupe**                                                                                                                          |
| [**Administrateur-Description**](a-admindescription.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-attributs**](a-allowedattributes.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                   | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom canonique**](a-canonicalname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Commentaire**](a-info.md)                                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Nom commun**](a-cn.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                       | Faux     | **Groupe**                                                                                                                          |
| [**Date et heure de création**](a-createtimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Description**](a-description.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Bureau-profil**](a-desktopprofile.md)                                  | Faux     | **Groupe**                                                                                                                          |
| [**Nom complet**](a-displayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DSA-signature**](a-dsasignature.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses de messagerie**](a-mail.md)                                           | Faux     | **Groupe**                                                                                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Indicateurs**](a-flags.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Entrée de**](a-fromentry.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                             | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Groupe-attributs**](a-groupattributes.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                         | Faux     | **Groupe**                                                                                                                          |
| [**Type de groupe**](a-grouptype.md)                                            | Vrai      | **Groupe**                                                                                                                          |
| [**Type d’instance**](a-instancetype.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est supprimé**](a-isdeleted.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Dernier-parent connu**](a-lastknownparent.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Géré par**](a-managedby.md)                                            | Faux     | **Groupe**                                                                                                                          |
| [**Objets managés**](a-managedobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Masterisé-par**](a-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre**](a-member.md)                                                   | Faux     | **Groupe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                             | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-LDAP-requête**](a-msds-azldapquery.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                    | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non-membres**](a-msds-nonmembers.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nom**](a-mssfu30name.md)                                       | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-NIS-domaine**](a-mssfu30nisdomain.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                        | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                           | Faux     | **Groupe**                                                                                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-members**](a-ntgroupmembers.md)                                 | Faux     | **Groupe**                                                                                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                     | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Catégorie d’objet**](a-objectcategory.md)                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Classe d’objet**](a-objectclass.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**GUID de l’objet**](a-objectguid.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID de l’objet**](a-objectsid.md)                                            | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Version de l’objet**](a-objectversion.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Opérateur-nombre**](a-operatorcount.md)                                    | Faux     | **Groupe**                                                                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-set**](a-partialattributeset.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Possible-inférieur**](a-possibleinferiors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                           | Faux     | **Groupe**                                                                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses proxy**](a-proxyaddresses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**UNIQUE**](a-name.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Rapports**](a-directreports.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à partir de**](a-repsfrom.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à**](a-repsto.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Faisant**](a-revision.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**RID**](a-rid.md)                                                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nom de compte SAM**](a-samaccountname.md)                                 | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Type de compte SAM**](a-samaccounttype.md)                                 | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificateur de sécurité**](a-securityidentifier.md)                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID-historique**](a-sidhistory.md)                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-objet-BL**](a-siteobjectbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Sous-Références**](a-subrefs.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Indicateurs système**](a-systemflags.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Numéro de téléphone**](a-telephonenumber.md)                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Jetons-groupes**](a-tokengroups.md)                                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md) | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                               | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Utilisateur-certificat**](a-usercert.md)                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                      | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modifié**](a-usnchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Créé par USN**](a-usncreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-intersite**](a-usnintersite.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-source**](a-usnsource.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Chemin WBEM**](a-wbempath.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Objets bien connus**](a-wellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**En cas de modification**](a-whenchanged.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Lors de la création**](a-whencreated.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page-autres**](a-url.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Droits étendus du serveur 2003 R2

cette classe contient les droits étendus suivants pour Windows Server 2003 R2 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-server-2003-r2-validated-writes"></a>Windows Écritures validées du serveur 2003 R2

cette classe contient les écritures validées suivantes pour Windows Server 2003 R2 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Jeux de propriétés de Server 2003 R2

cette classe contient les jeux de propriétés suivants pour Windows Server 2003 R2 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)
-   [Droits étendus](#windows-server-2008-extended-rights)
-   [Écritures validées](#windows-server-2008-validated-writes)
-   [Jeux de propriétés](#windows-server-2008-property-sets)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-catégorie     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Supérieurs possibles          | [**Domaine-Domain DNS**](c-domaindns.md)[](c-organizationalunit.md)[**BuiltIn-domaine**](c-builtindomain.md)[**conteneur**](c-container.md)[**ms-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes auxiliaires           | [**posixgroup**](c-posixgroup.md)[**sécurité-principal**](c-securityprincipal.md) (système)[**messagerie-destinataire**](c-mailrecipient.md) (système)                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                     |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; AU) (OA ;; RP ; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2 ;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-attributes"></a>Windows Attributs du serveur 2008

cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                        | Obligatoire | Dérivé de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre d’administrateurs**](a-admincount.md)                                              | Faux     | **Groupe**                                                                                                                          |
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                       | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Commentaire**](a-info.md)                                                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Nom commun**](a-cn.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                           | Faux     | **Groupe**                                                                                                                          |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Bureau-profil**](a-desktopprofile.md)                                      | Faux     | **Groupe**                                                                                                                          |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses de messagerie**](a-mail.md)                                               | Faux     | **Groupe**                                                                                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Indicateurs**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Groupe-attributs**](a-groupattributes.md)                                    | Faux     | **Groupe**                                                                                                                          |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                             | Faux     | **Groupe**                                                                                                                          |
| [**Type de groupe**](a-grouptype.md)                                                | Vrai      | **Groupe**                                                                                                                          |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Géré par**](a-managedby.md)                                                | Faux     | **Groupe**                                                                                                                          |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre**](a-member.md)                                                       | Faux     | **Groupe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Last-importée-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-LDAP-requête**](a-msds-azldapquery.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Faux     | **Groupe**                                                                                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non-membres**](a-msds-nonmembers.md)                                   | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nom**](a-mssfu30name.md)                                           | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-NIS-domaine**](a-mssfu30nisdomain.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-members**](a-ntgroupmembers.md)                                     | Faux     | **Groupe**                                                                                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID de l’objet**](a-objectsid.md)                                                | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Opérateur-nombre**](a-operatorcount.md)                                        | Faux     | **Groupe**                                                                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**RID**](a-rid.md)                                                             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nom de compte SAM**](a-samaccountname.md)                                     | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Type de compte SAM**](a-samaccounttype.md)                                     | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificateur de sécurité**](a-securityidentifier.md)                              | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID-historique**](a-sidhistory.md)                                              | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                    | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Numéro de téléphone**](a-telephonenumber.md)                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Jetons-groupes**](a-tokengroups.md)                                            | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md)     | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Utilisateur-certificat**](a-usercert.md)                                                  | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                          | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-extended-rights"></a>Windows Droits étendus du serveur 2008

cette classe contient les droits étendus suivants pour Windows Server 2008 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-server-2008-validated-writes"></a>Windows Serveur 2008 écritures validées

cette classe contient les écritures validées suivantes pour Windows Server 2008 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-server-2008-property-sets"></a>Windows Jeux de propriétés du serveur 2008

cette classe contient les jeux de propriétés suivants pour Windows Server 2008 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)
-   [Droits étendus](#windows-server-2008-r2-extended-rights)
-   [Écritures validées](#windows-server-2008-r2-validated-writes)
-   [Jeux de propriétés](#windows-server-2008-r2-property-sets)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-catégorie     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Supérieurs possibles          | [**Domaine-Domain DNS**](c-domaindns.md)[](c-organizationalunit.md)[**BuiltIn-domaine**](c-builtindomain.md)[**conteneur**](c-container.md)[**ms-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes auxiliaires           | [**posixgroup**](c-posixgroup.md)[**sécurité-principal**](c-securityprincipal.md) (système)[**messagerie-destinataire**](c-mailrecipient.md) (système)                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                     |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; AU) (OA ;; RP ; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2 ;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributs du serveur 2008 R2

cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de                                                                                                                       |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre d’administrateurs**](a-admincount.md)                                              | Faux     | **Groupe**                                                                                                                          |
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                       | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Commentaire**](a-info.md)                                                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Nom commun**](a-cn.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                           | Faux     | **Groupe**                                                                                                                          |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Bureau-profil**](a-desktopprofile.md)                                      | Faux     | **Groupe**                                                                                                                          |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses de messagerie**](a-mail.md)                                               | Faux     | **Groupe**                                                                                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Indicateurs**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                 | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Groupe-attributs**](a-groupattributes.md)                                    | Faux     | **Groupe**                                                                                                                          |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                             | Faux     | **Groupe**                                                                                                                          |
| [**Type de groupe**](a-grouptype.md)                                                | Vrai      | **Groupe**                                                                                                                          |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Géré par**](a-managedby.md)                                                | Faux     | **Groupe**                                                                                                                          |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre**](a-member.md)                                                       | Faux     | **Groupe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                 | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                    | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                    | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                   | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Last-importée-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md) | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-LDAP-requête**](a-msds-azldapquery.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                              | Faux     | **Groupe**                                                                                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non-membres**](a-msds-nonmembers.md)                                   | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nom**](a-mssfu30name.md)                                           | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-NIS-domaine**](a-mssfu30nisdomain.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                            | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-members**](a-ntgroupmembers.md)                                     | Faux     | **Groupe**                                                                                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID de l’objet**](a-objectsid.md)                                                | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Opérateur-nombre**](a-operatorcount.md)                                        | Faux     | **Groupe**                                                                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**RID**](a-rid.md)                                                             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nom de compte SAM**](a-samaccountname.md)                                     | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Type de compte SAM**](a-samaccounttype.md)                                     | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificateur de sécurité**](a-securityidentifier.md)                              | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID-historique**](a-sidhistory.md)                                              | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                    | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Numéro de téléphone**](a-telephonenumber.md)                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Jetons-groupes**](a-tokengroups.md)                                            | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md)     | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)             | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                   | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Utilisateur-certificat**](a-usercert.md)                                                  | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                          | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Droits étendus du serveur 2008 R2

cette classe contient les droits étendus suivants pour Windows Server 2008 R2 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-server-2008-r2-validated-writes"></a>Windows Écritures validées du serveur 2008 R2

cette classe contient les écritures validées suivantes pour Windows Server 2008 R2 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Jeux de propriétés de Server 2008 R2

cette classe contient les jeux de propriétés suivants pour Windows Server 2008 R2 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)
-   [Droits étendus](#windows-server-2012-extended-rights)
-   [Écritures validées](#windows-server-2012-validated-writes)
-   [Jeux de propriétés](#windows-server-2012-property-sets)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                                                                                                                                                            |
| Object-Category             | 1                                                                                                                                                                                                                                                                                                                |
| Default-Object-catégorie     | \-                                                                                                                                                                                                                                                                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.8                                                                                                                                                                                                                                                                                             |
| Valeur de masquage par défaut        | 0                                                                                                                                                                                                                                                                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                                                                                                                                                                           |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                                                                                                                                                                                                                                                  |
| Supérieurs possibles          | [**Domaine-Domain DNS**](c-domaindns.md)[](c-organizationalunit.md)[**BuiltIn-domaine**](c-builtindomain.md)[**conteneur**](c-container.md)[**ms-DS-AZ-admin-Manager**](c-msds-azadminmanager.md)[**ms-DS-AZ-application**](c-msds-azapplication.md)[**ms-DS-AZ-Scope**](c-msds-azscope.md) |
| Classes auxiliaires           | [**posixgroup**](c-posixgroup.md)[**sécurité-principal**](c-securityprincipal.md) (système)[**messagerie-destinataire**](c-mailrecipient.md) (système)                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                                                                                                                                                                     |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; AU) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; AO) (A ;; RPLCLORC;;; PS) (OA ;; CR ; ab721a55-1e2f-11D0-9819-00aa0040529b ;; AU) (OA ;; RP ; 46a9b11d-60ae-405a-b7e8-ff8a58d456d2 ;; S-1-5-32-560)                                                   |
| System-Flags                | 0x00000010                                                                                                                                                                                                                                                                                                       |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributs

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de                                                                                                                       |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------------------------------------------------|
| [**Nom-compte-historique**](a-accountnamehistory.md)                                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nombre d’administrateurs**](a-admincount.md)                                                          | Faux     | **Groupe**                                                                                                                          |
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Alt-sécurité-identités**](a-altsecurityidentities.md)                                   | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Commentaire**](a-info.md)                                                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Nom commun**](a-cn.md)                                                                  | Vrai      | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> |
| [**Droits de contrôle-accès**](a-controlaccessrights.md)                                       | Faux     | **Groupe**                                                                                                                          |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Description**](a-description.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/> [**posixGroup**](c-posixgroup.md)<br/>                                                      |
| [**Bureau-profil**](a-desktopprofile.md)                                                  | Faux     | **Groupe**                                                                                                                          |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses de messagerie**](a-mail.md)                                                           | Faux     | **Groupe**                                                                                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Indicateurs**](a-flags.md)                                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**gidNumber**](a-gidnumber.md)                                                             | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Groupe-attributs**](a-groupattributes.md)                                                | Faux     | **Groupe**                                                                                                                          |
| [**Groupe-appartenance-SAM**](a-groupmembershipsam.md)                                         | Faux     | **Groupe**                                                                                                                          |
| [**Type de groupe**](a-grouptype.md)                                                            | Vrai      | **Groupe**                                                                                                                          |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**labeledURI**](a-labeleduri.md)                                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Géré par**](a-managedby.md)                                                            | Faux     | **Groupe**                                                                                                                          |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre**](a-member.md)                                                                   | Faux     | **Groupe**                                                                                                                          |
| [**memberUid**](a-memberuid.md)                                                             | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-AZ-Application-Data**](a-msds-azapplicationdata.md)                                | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule**](a-msds-azbizrule.md)                                                | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-biz-Rule-Language**](a-msds-azbizrulelanguage.md)                               | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Generic-Data**](a-msds-azgenericdata.md)                                        | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Last-importée-biz-Rule-Path**](a-msds-azlastimportedbizrulepath.md)             | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-LDAP-requête**](a-msds-azldapquery.md)                                            | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-AZ-Object-GUID**](a-msds-azobjectguid.md)                                          | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-coordonnées-altitude**](a-msds-geocoordinatesaltitude.md)                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-géocoordinations-Latitude**](a-msds-geocoordinateslatitude.md)                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-géocoordinations-Longitude**](a-msds-geocoordinateslongitude.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-KeyVersionNumber**](a-msds-keyversionnumber.md)                                    | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-non-membres**](a-msds-nonmembers.md)                                               | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-DS-principal-ordinateur**](a-msds-primarycomputer.md)                                     | Faux     | **Groupe**                                                                                                                          |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**msSFU-30-nom**](a-mssfu30name.md)                                                       | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-NIS-domaine**](a-mssfu30nisdomain.md)                                            | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member**](a-mssfu30posixmember.md)                                        | Faux     | **Groupe**                                                                                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Membre non de sécurité**](a-nonsecuritymember.md)                                           | Faux     | **Groupe**                                                                                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**NT-Group-members**](a-ntgroupmembers.md)                                                 | Faux     | **Groupe**                                                                                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/> [**Sécurité-principal**](c-securityprincipal.md)<br/>                                       |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID de l’objet**](a-objectsid.md)                                                            | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Opérateur-nombre**](a-operatorcount.md)                                                    | Faux     | **Groupe**                                                                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Primary-Group-Token**](a-primarygrouptoken.md)                                           | Faux     | **Groupe**                                                                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Rapports**](a-directreports.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Faisant**](a-revision.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**RID**](a-rid.md)                                                                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Nom de compte SAM**](a-samaccountname.md)                                                 | Vrai      | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Type de compte SAM**](a-samaccounttype.md)                                                 | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**secretary**](a-secretary.md)                                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Identificateur de sécurité**](a-securityidentifier.md)                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SID-historique**](a-sidhistory.md)                                                          | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Informations d’identification supplémentaires**](a-supplementalcredentials.md)                                | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Numéro de téléphone**](a-telephonenumber.md)                                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Jetons-groupes**](a-tokengroups.md)                                                        | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-global-et-Universal**](a-tokengroupsglobalanduniversal.md)                 | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**Token-Groups-non-GC-acceptable**](a-tokengroupsnogcacceptable.md)                         | Faux     | [**Sécurité-principal**](c-securityprincipal.md)<br/>                                                                       |
| [**unixUserPassword**](a-unixuserpassword.md)                                               | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**Utilisateur-certificat**](a-usercert.md)                                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                                      | Faux     | [**posixGroup**](c-posixgroup.md)<br/>                                                                                      |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                    |
| [**X509-CERT**](a-usercertificate.md)                                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                               |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Droits étendus

Cette classe contient les droits étendus suivants pour Windows Server 2012 :



| Nom commun                  |
|------------------------------|
| [**Envoyer vers**](r-send-to.md) |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Écritures validées

Cette classe contient les écritures validées suivantes pour Windows Server 2012 :



| Nom commun                                  |
|----------------------------------------------|
| [**Auto-appartenance**](r-self-membership.md) |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Jeux de propriétés

Cette classe contient les jeux de propriétés suivants pour Windows Server 2012 :



| Nom commun                                      |
|--------------------------------------------------|
| [**E-mail-informations**](r-email-information.md) |



 

 





