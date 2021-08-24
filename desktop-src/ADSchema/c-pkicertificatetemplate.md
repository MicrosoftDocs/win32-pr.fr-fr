---
title: Classe de modèle PKI-Certificate
description: Contient des informations sur les certificats émis par le serveur de certificats.
ms.assetid: 9b6ca989-058c-461b-ba3d-5b29ea15cbbc
ms.tgt_platform: multiple
keywords:
- PKI-schéma AD de la classe de modèle de certificat
- Schéma AD de la classe pKICertificateTemplate
topic_type:
- apiref
api_name:
- PKI-Certificate-Template
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e45c19969a09770e8b37b5bf9a45c4ff4d87806fc8e77b02e1a7e109981110c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753089"
---
# <a name="pki-certificate-template-class"></a>Classe de modèle PKI-Certificate

Contient des informations sur les certificats émis par le serveur de certificats.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | PKI-Certificate-modèle             |
| LDAP-Display-Name | pKICertificateTemplate               |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | e5209ca2-3bba-11d2-90cc-00c04fd91ab1 |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributs](#windows-2000-server-attributes)
-   [Droits étendus](#windows-2000-server-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>attributs de serveur Windows 2000

cette classe contient les attributs suivants pour Windows serveur 2000 :



| Attribut                                                                 | Obligatoire | Dérivé de                                                 |
|---------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md) | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                     | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                  | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                  | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                               | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                          | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-2000-server-extended-rights"></a>droits étendus du serveur Windows 2000

cette classe contient les droits étendus suivants pour Windows serveur 2000 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)
-   [Droits étendus](#windows-server-2003-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Attributs du serveur 2003

cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                               | Obligatoire | Dérivé de                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                                   | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                                | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-application-stratégie**](a-mspki-certificate-application-policy.md) | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-certificat-stratégie**](a-mspki-certificate-policy.md)                         | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-cert-template-OID**](a-mspki-cert-template-oid.md)                           | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-inscription-indicateur**](a-mspki-enrollment-flag.md)                               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-minimum-Key-Size**](a-mspki-minimal-key-size.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-privé-clé-indicateur**](a-mspki-private-key-flag.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-application-stratégies**](a-mspki-ra-application-policies.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-stratégies**](a-mspki-ra-policies.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-signature**](a-mspki-ra-signature.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-remplace-templates**](a-mspki-supersede-templates.md)                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-mineur-révision**](a-mspki-template-minor-revision.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-Schema-Version**](a-mspki-template-schema-version.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                             | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                                 | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-server-2003-extended-rights"></a>Windows Droits étendus du serveur 2003

cette classe contient les droits étendus suivants pour Windows Server 2003 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)
-   [Droits étendus](#windows-server-2003-r2-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributs du serveur 2003 R2

cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                               | Obligatoire | Dérivé de                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                                   | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                                | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-application-stratégie**](a-mspki-certificate-application-policy.md) | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-certificat-stratégie**](a-mspki-certificate-policy.md)                         | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-cert-template-OID**](a-mspki-cert-template-oid.md)                           | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-inscription-indicateur**](a-mspki-enrollment-flag.md)                               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-minimum-Key-Size**](a-mspki-minimal-key-size.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-privé-clé-indicateur**](a-mspki-private-key-flag.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-application-stratégies**](a-mspki-ra-application-policies.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-stratégies**](a-mspki-ra-policies.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-signature**](a-mspki-ra-signature.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-remplace-templates**](a-mspki-supersede-templates.md)                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-mineur-révision**](a-mspki-template-minor-revision.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-Schema-Version**](a-mspki-template-schema-version.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                             | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                                 | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Droits étendus du serveur 2003 R2

cette classe contient les droits étendus suivants pour Windows Server 2003 R2 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)
-   [Droits étendus](#windows-server-2008-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Attributs du serveur 2008

cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                               | Obligatoire | Dérivé de                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                                   | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                                | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-application-stratégie**](a-mspki-certificate-application-policy.md) | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-certificat-stratégie**](a-mspki-certificate-policy.md)                         | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-cert-template-OID**](a-mspki-cert-template-oid.md)                           | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-inscription-indicateur**](a-mspki-enrollment-flag.md)                               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-minimum-Key-Size**](a-mspki-minimal-key-size.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-privé-clé-indicateur**](a-mspki-private-key-flag.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-application-stratégies**](a-mspki-ra-application-policies.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-stratégies**](a-mspki-ra-policies.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-signature**](a-mspki-ra-signature.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-remplace-templates**](a-mspki-supersede-templates.md)                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-mineur-révision**](a-mspki-template-minor-revision.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-Schema-Version**](a-mspki-template-schema-version.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                             | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                                 | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-server-2008-extended-rights"></a>Windows Droits étendus du serveur 2008

cette classe contient les droits étendus suivants pour Windows Server 2008 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)
-   [Droits étendus](#windows-server-2008-r2-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributs du serveur 2008 R2

cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                               | Obligatoire | Dérivé de                                                 |
|-----------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                                   | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                                | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-recyclé**](a-isrecycled.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-application-stratégie**](a-mspki-certificate-application-policy.md) | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-certificat-stratégie**](a-mspki-certificate-policy.md)                         | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-cert-template-OID**](a-mspki-cert-template-oid.md)                           | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-inscription-indicateur**](a-mspki-enrollment-flag.md)                               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-minimum-Key-Size**](a-mspki-minimal-key-size.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-privé-clé-indicateur**](a-mspki-private-key-flag.md)                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-application-stratégies**](a-mspki-ra-application-policies.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-stratégies**](a-mspki-ra-policies.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-signature**](a-mspki-ra-signature.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-remplace-templates**](a-mspki-supersede-templates.md)                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-mineur-révision**](a-mspki-template-minor-revision.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-Schema-Version**](a-mspki-template-schema-version.md)               | Faux     | **PKI-Certificate-modèle**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                             | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                                     | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                                 | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Droits étendus du serveur 2008 R2

cette classe contient les droits étendus suivants pour Windows Server 2008 R2 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)
-   [Droits étendus](#windows-server-2012-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.177                                                                       |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>                                                              |
| Supérieurs possibles          | [**Conteneur**](c-container.md)                                                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributs

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de                                                 |
|----------------------------------------------------------------------------------------------|-----------|--------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom commun**](a-cn.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Description**](a-description.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs**](a-flags.md)                                                                     | Faux     | **PKI-Certificate-modèle** [ **Top**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**MS-PKI-Certificate-application-stratégie**](a-mspki-certificate-application-policy.md)      | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-Certificate-Name-Flag**](a-mspki-certificate-name-flag.md)                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-certificat-stratégie**](a-mspki-certificate-policy.md)                              | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-cert-template-OID**](a-mspki-cert-template-oid.md)                                | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-inscription-indicateur**](a-mspki-enrollment-flag.md)                                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-minimum-Key-Size**](a-mspki-minimal-key-size.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-privé-clé-indicateur**](a-mspki-private-key-flag.md)                                  | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-application-stratégies**](a-mspki-ra-application-policies.md)                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-stratégies**](a-mspki-ra-policies.md)                                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-RA-signature**](a-mspki-ra-signature.md)                                          | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-remplace-templates**](a-mspki-supersede-templates.md)                            | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-mineur-révision**](a-mspki-template-minor-revision.md)                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**MS-PKI-template-Schema-Version**](a-mspki-template-schema-version.md)                    | Faux     | **PKI-Certificate-modèle**                                 |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                              |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**PKI-Critical-extensions**](a-pkicriticalextensions.md)                                   | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-default-CSP**](a-pkidefaultcsps.md)                                                 | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-clé-valeur par défaut**](a-pkidefaultkeyspec.md)                                          | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-inscription-accès**](a-pkienrollmentaccess.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-expiration-période**](a-pkiexpirationperiod.md)                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-étendue-utilisation**](a-pkiextendedkeyusage.md)                                      | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Key-usage**](a-pkikeyusage.md)                                                       | Faux     | **PKI-Certificate-modèle**                                 |
| [**PKI-Max-Emission-Depth**](a-pkimaxissuingdepth.md)                                        | Faux     | **PKI-Certificate-modèle**                                 |
| [**Infrastructure à clé publique-chevauchement-période**](a-pkioverlapperiod.md)                                             | Faux     | **PKI-Certificate-modèle**                                 |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Rapports**](a-directreports.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Faisant**](a-revision.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                              |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                              |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Droits étendus

Cette classe contient les droits étendus suivants pour Windows Server 2012 :



| Nom commun                                                |
|------------------------------------------------------------|
| [**Inscription de certificats**](r-certificate-enrollment.md) |



 

 





