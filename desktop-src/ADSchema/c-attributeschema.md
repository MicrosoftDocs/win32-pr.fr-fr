---
title: Classe Attribute-Schema
description: Définit un objet d’attribut dans le schéma.
ms.assetid: 2338d0ca-b090-4c76-be39-3f54ecb9932d
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe Attribute-Schema
- Schéma d’AD de la classe attributeSchema
topic_type:
- apiref
api_name:
- Attribute-Schema
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a75225aa034503a2f08beb827f00cb44ccb656b387a1edb601b7ea430f05c0d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119703889"
---
# <a name="attribute-schema-class"></a>Classe Attribute-Schema

Définit un objet d’attribut dans le schéma.



| Entrée | Valeur |
|-------------------|-----------------------------------------------|
| CN                | Attribute-Schema                              |
| LDAP-Display-Name | attributeSchema                               |
| Mettre à jour le privilège  | Cette valeur est définie par l’administrateur de schéma. |
| Fréquence des mises à jour  | \-                                            |
| Schema-ID-GUID    | bf967a80-0de6-11d0-a285-00aa003049e2          |



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



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-2000-server-attributes"></a>attributs de serveur Windows 2000

cette classe contient les attributs suivants pour Windows serveur 2000 :



| Attribut                                                                     | Obligatoire | Dérivé de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                         | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                 | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                   | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                      | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                             | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md) | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                  | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                         | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                               | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-attributes"></a>Windows Attributs du serveur 2003

cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                     | Obligatoire | Dérivé de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                         | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                 | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                   | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                      | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                             | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md) | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                  | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                   | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                         | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                               | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                     | Obligatoire | Dérivé de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                         | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                 | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                   | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                      | Faux     | **Attribut-schéma**                                 |
| [**Entrée de**](a-fromentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                             | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md) | Faux     | **Attribut-schéma**                                 |
| [**Est de valeur unique**](a-issinglevalued.md)                                  | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Masterisé-par**](a-masteredby.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                   | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                         | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                               | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributs du serveur 2003 R2

cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                     | Obligatoire | Dérivé de                                         |
|-------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                         | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                    | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                 | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                              | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                   | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                      | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                             | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md) | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                  | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                   | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                         | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                               | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                    | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                      | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                         | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                           | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-attributes"></a>Windows Attributs du serveur 2008

cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                      | Obligatoire | Dérivé de                                         |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                          | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                     | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                  | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                               | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                    | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                       | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                              | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                          | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md)  | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                   | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                 | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                    | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                    | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                    | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                     | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                                | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                     | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                       | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                          | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributs du serveur 2008 R2

cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de                                         |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                            | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                       | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                    | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                 | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                      | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                         | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                                | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md)    | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                     | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                   | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                      | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                      | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                              | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                      | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                       | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                                  | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                              | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                              | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                       | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                         | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                            | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                              | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Faux                                  |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.3.14                  |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**DMD**](c-dmd.md)                   |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x08000010                             |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributs

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de                                         |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID d’attribut**](a-attributeid.md)                                                        | Vrai      | **Attribut-schéma**                                 |
| [**Attribute-Security-GUID**](a-attributesecurityguid.md)                                   | Faux     | **Attribut-schéma**                                 |
| [**Syntaxe d’attribut**](a-attributesyntax.md)                                                | Vrai      | **Attribut-schéma**                                 |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Class-Display-Name**](a-classdisplayname.md)                                             | Faux     | **Attribut-schéma**                                 |
| [**Nom commun**](a-cn.md)                                                                  | Vrai      | **Attribut-Schema** [ **Top**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Description**](a-description.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Caractères étendus-autorisés**](a-extendedcharsallowed.md)                                     | Faux     | **Attribut-schéma**                                 |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs**](a-flags.md)                                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-défunt**](a-isdefunct.md)                                                            | Faux     | **Attribut-schéma**                                 |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Is-éphémère**](a-isephemeral.md)                                                        | Faux     | **Attribut-schéma**                                 |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est un membre de-partial-attribute-set**](a-ismemberofpartialattributeset.md)                | Faux     | **Attribut-schéma**                                 |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Est de valeur unique**](a-issinglevalued.md)                                                 | Vrai      | **Attribut-schéma**                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**LDAP-Display-Name**](a-ldapdisplayname.md)                                               | Vrai      | **Attribut-schéma**                                 |
| [**ID de lien**](a-linkid.md)                                                                  | Faux     | **Attribut-schéma**                                 |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ID MAPI**](a-mapiid.md)                                                                  | Faux     | **Attribut-schéma**                                 |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-IntId**](a-msds-intid.md)                                                          | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-Schema-extensions**](a-msds-schema-extensions.md)                                  | Faux     | **Attribut-schéma**                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                      |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**OM-Object-Class**](a-omobjectclass.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**OM-syntaxe**](a-omsyntax.md)                                                              | Vrai      | **Attribut-schéma**                                 |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Plage inférieure**](a-rangelower.md)                                                          | Faux     | **Attribut-schéma**                                 |
| [**Plage supérieure**](a-rangeupper.md)                                                          | Faux     | **Attribut-schéma**                                 |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Rapports**](a-directreports.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Faisant**](a-revision.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de schéma-ex**](a-schemaflagsex.md)                                                   | Faux     | **Attribut-schéma**                                 |
| [**Schema-ID-GUID**](a-schemaidguid.md)                                                     | Vrai      | **Attribut-schéma**                                 |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs de recherche**](a-searchflags.md)                                                        | Faux     | **Attribut-schéma**                                 |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Système uniquement**](a-systemonly.md)                                                          | Faux     | **Attribut-schéma**                                 |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                      |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                      |



 

 





