---
title: Classe Contact
description: Cette classe contient des informations sur une personne ou une société que vous devrez peut-être contacter régulièrement.
ms.assetid: 2372ea2b-1ac3-4173-950f-4ee00138fe22
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe de contact
- Schéma AD de la classe de contact
topic_type:
- apiref
api_name:
- Contact
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4b54d5929e11382c1680090adf376f670d8610fd767a193e349a31f54c1f2cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021887"
---
# <a name="contact-class"></a>Classe Contact

Cette classe contient des informations sur une personne ou une société que vous devrez peut-être contacter régulièrement.



| Entrée | Valeur |
|-------------------|------------------------------------------------|
| CN                | Contact                                        |
| LDAP-Display-Name | contact                                        |
| Mettre à jour le privilège  | Cette valeur est définie par l’administrateur de domaine. |
| Fréquence des mises à jour  | \-                                             |
| Schema-ID-GUID    | 5cb41ed0-0e4c-11d0-a286-00aa003049e2           |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributs](#windows-2000-server-attributes)
-   [Jeux de propriétés](#windows-2000-server-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>attributs de serveur Windows 2000

cette classe contient les attributs suivants pour Windows serveur 2000 :



| Attribut                                                                 | Obligatoire | Dérivé de                                                                                                                           |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                 | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                               | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Dernier-parent connu**](a-lastknownparent.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                               | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Voir aussi**](a-seealso.md)                                             | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Sous-Références**](a-subrefs.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                   | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                             | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                   | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                  | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-2000-server-property-sets"></a>jeux de propriétés de serveur Windows 2000

cette classe contient les jeux de propriétés suivants pour Windows serveur 2000 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)
-   [Jeux de propriétés](#windows-server-2003-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Attributs du serveur 2003

cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                   | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                   | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                                 | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-autorisé-à-déléguer-à**](a-msds-allowedtodelegateto.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-identifier**](a-msexchhouseidentifier.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Voir aussi**](a-seealso.md)                                               | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Numéro de série**](a-serialnumber.md)                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                               | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                   | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-property-sets"></a>Windows Jeux de propriétés du serveur 2003

cette classe contient les jeux de propriétés suivants pour Windows Server 2003 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)
-   [Jeux de propriétés](#windows-server-2003-r2-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributs du serveur 2003 R2

cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                                                                                           |
|-----------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                   | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)    | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                   | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                                 | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-autorisé-à-déléguer-à**](a-msds-allowedtodelegateto.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-source-objet-DN**](a-msds-sourceobjectdn.md)                     | Faux     | **Contact**                                                                                                                            |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-identifier**](a-msexchhouseidentifier.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Voir aussi**](a-seealso.md)                                               | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Numéro de série**](a-serialnumber.md)                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                               | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                   | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                     | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2003-r2-property-sets"></a>Windows Jeux de propriétés de Server 2003 R2

cette classe contient les jeux de propriétés suivants pour Windows Server 2003 R2 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)
-   [Jeux de propriétés](#windows-server-2008-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Attributs du serveur 2008

cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                      | Obligatoire | Dérivé de                                                                                                                           |
|--------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                      | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)       | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                                    | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                             | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-autorisé-à-déléguer-à**](a-msds-allowedtodelegateto.md)             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-phonétique-nom de la société**](a-msds-phoneticcompanyname.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-service**](a-msds-phoneticdepartment.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                |
| [**ms-DS-phonétique-prénom**](a-msds-phoneticfirstname.md)                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Last-Name**](a-msds-phoneticlastname.md)                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-source-objet-DN**](a-msds-sourceobjectdn.md)                        | Faux     | **Contact**                                                                                                                            |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-identifier**](a-msexchhouseidentifier.md)                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Voir aussi**](a-seealso.md)                                                  | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Numéro de série**](a-serialnumber.md)                                        | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                            | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Sous-Références**](a-subrefs.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                        | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                                  | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                      | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                        | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-property-sets"></a>Windows Jeux de propriétés du serveur 2008

cette classe contient les jeux de propriétés suivants pour Windows Server 2008 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)
-   [Jeux de propriétés](#windows-server-2008-r2-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributs du serveur 2008 R2

cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de                                                                                                                           |
|----------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                        | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)         | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                                      | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-autorisé-à-déléguer-à**](a-msds-allowedtodelegateto.md)               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-phonétique-nom de la société**](a-msds-phoneticcompanyname.md)                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-service**](a-msds-phoneticdepartment.md)                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                |
| [**ms-DS-phonétique-prénom**](a-msds-phoneticfirstname.md)                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Last-Name**](a-msds-phoneticlastname.md)                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-source-objet-DN**](a-msds-sourceobjectdn.md)                          | Faux     | **Contact**                                                                                                                            |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                          | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-identifier**](a-msexchhouseidentifier.md)                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)                   | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Voir aussi**](a-seealso.md)                                                    | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Numéro de série**](a-serialnumber.md)                                          | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                          | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                                    | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                                  | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                          | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                         | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                           | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2008-r2-property-sets"></a>Windows Jeux de propriétés de Server 2008 R2

cette classe contient les jeux de propriétés suivants pour Windows Server 2008 R2 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)
-   [Jeux de propriétés](#windows-server-2012-property-sets)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | [**Personne**](c-person.md)<br/>                                                        |
| Governs-Id                  | 1.2.840.113556.1.5.15                                                                        |
| Valeur de masquage par défaut        | 0                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Organizational-Person**](c-organizationalperson.md)<br/>                           |
| Supérieurs possibles          | [**Domaine-**](c-domaindns.md)[**unité d’organisation** DNS](c-organizationalunit.md)         |
| Classes auxiliaires           | [**E-mail-destinataire**](c-mailrecipient.md) (système)                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributs

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                              | Obligatoire | Dérivé de                                                                                                                           |
|--------------------------------------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------|
| [**Informations supplémentaires**](a-notes.md)                                                              | Faux     | **Contact**                                                                                                                            |
| [**Adresse**](a-streetaddress.md)                                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Adresse-personnelle**](a-homepostaladdress.md)                                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Administrateur-Description**](a-admindescription.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-attributs**](a-allowedattributes.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Conseiller**](a-assistant.md)                                                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**attributeCertificateAttribute**](a-attributecertificateattribute.md)                               | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom canonique**](a-canonicalname.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Commentaire**](a-info.md)                                                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Nom commun**](a-cn.md)                                                                            | Vrai      |  [ **Personne** à contacter](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Company**](a-company.md)                                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Pays-code**](a-countrycode.md)                                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Country-Name**](a-c.md)                                                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de création**](a-createtimestamp.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Service**](a-department.md)                                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Description**](a-description.md)                                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Destination-indicateur**](a-destinationindicator.md)                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom complet**](a-displayname.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Division**](a-division.md)                                                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**DSA-signature**](a-dsasignature.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses de messagerie**](a-mail.md)                                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ID d’employé**](a-employeeid.md)                                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’extension**](a-extensionname.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Télécopie-numéro de téléphone**](a-facsimiletelephonenumber.md)                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Indicateurs**](a-flags.md)                                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Entrée de**](a-fromentry.md)                                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Garbage-coll-period**](a-garbagecollperiod.md)                                                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Qualificateur de génération**](a-generationqualifier.md)                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom donné**](a-givenname.md)                                                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**houseIdentifier**](a-houseidentifier.md)                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Initiales**](a-initials.md)                                                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Type d’instance**](a-instancetype.md)                                                                | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**International-RNIS-numéro**](a-internationalisdnnumber.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est supprimé**](a-isdeleted.md)                                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Is-Member-of-DL**](a-memberof.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Est-recyclé**](a-isrecycled.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**labeledURI**](a-labeleduri.md)                                                                     | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Dernier-parent connu**](a-lastknownparent.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Legacy-Exchange-DN**](a-legacyexchangedn.md)                                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Localité-Name**](a-l.md)                                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Logo**](a-thumbnaillogo.md)                                                                        | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Objets managés**](a-managedobjects.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Gestion**](a-manager.md)                                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Masterisé-par**](a-masteredby.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MHS-ou-adresse**](a-mhsoraddress.md)                                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Date et heure de modification**](a-modifytimestamp.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-allowed-to-Act-on-on-of-other-Identity**](a-msds-allowedtoactonbehalfofotheridentity.md) | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-autorisé-à-déléguer-à**](a-msds-allowedtodelegateto.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-coordonnées-altitude**](a-msds-geocoordinatesaltitude.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-géocoordinations-Latitude**](a-msds-geocoordinateslatitude.md)                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-géocoordinations-Longitude**](a-msds-geocoordinateslongitude.md)                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-DS-HAB-Senior-index**](a-msds-habseniorityindex.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-phonétique-nom de la société**](a-msds-phoneticcompanyname.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-service**](a-msds-phoneticdepartment.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Display-Name**](a-msds-phoneticdisplayname.md)                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                |
| [**ms-DS-phonétique-prénom**](a-msds-phoneticfirstname.md)                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-phonétique-Last-Name**](a-msds-phoneticlastname.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-source-objet-DN**](a-msds-sourceobjectdn.md)                                                | Faux     | **Contact**                                                                                                                            |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**ms-Exch-Assistant-nom**](a-msexchassistantname.md)                                                | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-House-identifier**](a-msexchhouseidentifier.md)                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**ms-Exch-LabeledURI**](a-msexchlabeleduri.md)                                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                               | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Classe d’objet**](a-objectclass.md)                                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**GUID de l’objet**](a-objectguid.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Version de l’objet**](a-objectversion.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’unité d’organisation**](a-ou.md)                                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Nom de l’Organisation**](a-o.md)                                                                       | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre-boîte aux lettres**](a-othermailbox.md)                                                                | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autre nom**](a-middlename.md)                                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Personnel-titre**](a-personaltitle.md)                                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-télécopie-autre**](a-otherfacsimiletelephonenumber.md)                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-à-soi-autre**](a-otherhomephone.md)                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page d’hébergement principal**](a-homephone.md)                                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-autre**](a-otheripphone.md)                                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Ip-principal**](a-ipphone.md)                                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-rnis-principal**](a-primaryinternationalisdnnumber.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-autres**](a-othermobile.md)                                                            | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Mobile-principal**](a-mobile.md)                                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-Office-autre**](a-othertelephone.md)                                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-téléavertisseur-autre**](a-otherpager.md)                                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Téléphone-page de récepteur-principal**](a-pager.md)                                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Physical-delivery-Office-Name**](a-physicaldeliveryofficename.md)                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Aperçu**](a-thumbnailphoto.md)                                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Possible-inférieur**](a-possibleinferiors.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse postale**](a-postaladdress.md)                                                              | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Code postal**](a-postalcode.md)                                                                    | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**boîte de Office**](a-postofficebox.md)                                                             | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Méthode de remise par défaut**](a-preferreddeliverymethod.md)                                         | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**UNIQUE**](a-name.md)                                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Adresse inscrite**](a-registeredaddress.md)                                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Rapports**](a-directreports.md)                                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Représentants-à**](a-repsto.md)                                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Faisant**](a-revision.md)                                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**secretary**](a-secretary.md)                                                                       | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Voir aussi**](a-seealso.md)                                                                          | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Numéro de série**](a-serialnumber.md)                                                                | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Afficher dans l’adresse-livre**](a-showinaddressbook.md)                                                    | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Nom de l’État ou de la province**](a-st.md)                                                                 | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Rue-adresse**](a-street.md)                                                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Sous-Références**](a-subrefs.md)                                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Famille**](a-sn.md)                                                                                | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**Indicateurs système**](a-systemflags.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Numéro de téléphone**](a-telephonenumber.md)                                                          | Faux     | [**Personne**](c-person.md)<br/> [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                             |
| [**TELETEX-identificateur de terminal**](a-teletexterminalidentifier.md)                                     | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Numéro de télex**](a-telexnumber.md)                                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Télex-principal**](a-primarytelexnumber.md)                                                          | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-pays**](a-co.md)                                                                           | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Texte-ou-adresse**](a-textencodedoraddress.md)                                              | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Titre**](a-title.md)                                                                               | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-certificat**](a-usercert.md)                                                                        | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**Utilisateur-commentaire**](a-comment.md)                                                                      | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**Utilisateur-mot de passe**](a-userpassword.md)                                                                | Faux     | [**Personne**](c-person.md)<br/>                                                                                                  |
| [**User-SMIME-Certificate**](a-usersmimecertificate.md)                                               | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |
| [**USN-modifié**](a-usnchanged.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Créé par USN**](a-usncreated.md)                                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-intersite**](a-usnintersite.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**USN-source**](a-usnsource.md)                                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Chemin WBEM**](a-wbempath.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Objets bien connus**](a-wellknownobjects.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**En cas de modification**](a-whenchanged.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**Lors de la création**](a-whencreated.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**WWW-page-autres**](a-url.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                                                                        |
| [**X121-adresse**](a-x121address.md)                                                                  | Faux     | [**Organizational-Person**](c-organizationalperson.md)<br/>                                                                     |
| [**X509-CERT**](a-usercertificate.md)                                                                 | Faux     | [**E-mail-destinataire**](c-mailrecipient.md)<br/>                                                                                   |



## <a name="windows-server-2012-property-sets"></a>Windows Server 2012 Jeux de propriétés

Cette classe contient les jeux de propriétés suivants pour Windows Server 2012 :



| Nom commun                                            |
|--------------------------------------------------------|
| [**Informations personnelles**](r-personal-information.md) |
| [**Informations Web**](r-web-information.md)           |



 

 





