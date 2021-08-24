---
title: Classe NTDS-DSA
description: Représente le Active Directory processus DSA sur le serveur.
ms.assetid: f4369122-d74a-45d2-9dc0-46894a9f99cc
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe NTDS-DSA
- Schéma Active Directory de la classe nTDSDSA
topic_type:
- apiref
api_name:
- NTDS-DSA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 284b04027b97be0a8808f45ff61707d6b56b054786272e8d46d32f92d43c5448
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119753439"
---
# <a name="ntds-dsa-class"></a>Classe NTDS-DSA

Représente le Active Directory processus DSA sur le serveur.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | NTDS-DSA                             |
| LDAP-Display-Name | nTDSDSA                              |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | f0f8ffab-1191-11d0-a060-00aa006c33ed |



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



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>attributs de serveur Windows 2000

cette classe contient les attributs suivants pour Windows serveur 2000 :



| Attribut                                                                 | Obligatoire | Dérivé de                                                     |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                             | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                     | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                  | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                 | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                   | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)       | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                         | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                           | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                               | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                              | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                        | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)         | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                             | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-2000-server-extended-rights"></a>droits étendus du serveur Windows 2000

cette classe contient les droits étendus suivants pour Windows serveur 2000 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Abandon-réplication**](r-abandon-replication.md)                           |
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)
-   [Droits étendus](#windows-server-2003-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Windows Attributs du serveur 2003

cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                               | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                       | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                      | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                     | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)         | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                           | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)             | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                   | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                                 | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                             | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                          | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)           | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-extended-rights"></a>Windows Droits étendus du serveur 2003

cette classe contient les droits étendus suivants pour Windows Server 2003 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |
| [**Actualiser-groupe-cache**](r-refresh-group-cache.md)                           |



## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)
-   [Droits étendus](#adam-extended-rights)



| Entrée | Valeur |
|-----------------------------|------------------------------------------------------------------|
| System-Only                 | Vrai                                                             |
| Object-Category             | 1                                                                |
| Default-Object-catégorie     | \-                                                               |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                       |
| Valeur de masquage par défaut        | 1                                                                |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                           |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md) |
| Classes auxiliaires           | \-                                                               |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                     |
| Descripteur de sécurité par défaut | D:S:                                                             |
| System-Flags                | 0x00000010                                                       |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                   | Obligatoire | Dérivé de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                       | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                     | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)         | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                           | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)             | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-port-LDAP**](a-msds-portldap.md)                                  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-port-SSL**](a-msds-portssl.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-service-account**](a-msds-serviceaccount.md)                      | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-service-account-DNS-Domain**](a-msds-serviceaccountdnsdomain.md)  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                   | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Adresse réseau**](a-networkaddress.md)                                 | Faux     | **NTDS-DSA**                                                     |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                          | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)           | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="adam-extended-rights"></a>Droits étendus ADAM

Cette classe contient les droits étendus suivants pour ADAM :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)
-   [Droits étendus](#windows-server-2003-r2-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Windows Attributs du serveur 2003 R2

cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                     |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                               | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                       | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                      | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                     | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)         | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                           | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)             | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                   | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                                 | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                             | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                          | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)           | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-server-2003-r2-extended-rights"></a>Windows Droits étendus du serveur 2003 R2

cette classe contient les droits étendus suivants pour Windows Server 2003 R2 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |
| [**Actualiser-groupe-cache**](r-refresh-group-cache.md)                           |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)
-   [Droits étendus](#windows-server-2008-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Windows Attributs du serveur 2008

cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                      | Obligatoire | Dérivé de                                                     |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                                  | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                          | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                         | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                       | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                      | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                        | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)            | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                              | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                      | Faux     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-full-Replica-NC**](a-msds-hasfullreplicancs.md)                 | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)                | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                              | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                          | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-cachable-at-RODC**](a-msds-isusercachableatrodc.md)          | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-jamais-Reveal-Group**](a-msds-neverrevealgroup.md)                    | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                      | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)     | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-utilisateurs**](a-msds-revealedusers.md)                           | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)              | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                      | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                      | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                                | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                   | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                             | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)              | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                                  | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-extended-rights"></a>Windows Droits étendus du serveur 2008

cette classe contient les droits étendus suivants pour Windows Server 2008 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |
| [**Actualiser-groupe-cache**](r-refresh-group-cache.md)                           |
| [**Recharger-SSL-certificat**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)
-   [Droits étendus](#windows-server-2008-r2-extended-rights)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Windows Attributs du serveur 2008 R2

cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de                                                     |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                                    | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                            | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                           | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                         | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                        | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                          | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)              | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                        | Faux     | **NTDS-DSA**                                                     |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Fonctionnalité ms-DS-Enabled**](a-msds-enabledfeature.md)                           | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                              | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-full-Replica-NC**](a-msds-hasfullreplicancs.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)                  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                              | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-cachable-at-RODC**](a-msds-isusercachableatrodc.md)            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-jamais-Reveal-Group**](a-msds-neverrevealgroup.md)                      | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                        | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)       | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-utilisateurs**](a-msds-revealedusers.md)                             | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                        | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                        | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                                      | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                                  | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                     | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)                | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-server-2008-r2-extended-rights"></a>Windows Droits étendus du serveur 2008 R2

cette classe contient les droits étendus suivants pour Windows Server 2008 R2 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |
| [**Actualiser-groupe-cache**](r-refresh-group-cache.md)                           |
| [**Recharger-SSL-certificat**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)
-   [Droits étendus](#windows-server-2012-extended-rights)
-   [Écritures validées](#windows-server-2012-validated-writes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.7000.47                                                                   |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | [**Paramètres de l’Application**](c-applicationsettings.md)<br/>                             |
| Supérieurs possibles          | [](c-server.md)[**Organisation** du serveur](c-organization.md)                             |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Windows Server 2012 Attributs

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de                                                     |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’application**](a-applicationname.md)                                                | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom commun**](a-cn.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Description**](a-description.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DMD-emplacement**](a-dmdlocation.md)                                                        | Faux     | **NTDS-DSA**                                                     |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs**](a-flags.md)                                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**FRS-root-Path**](a-frsrootpath.md)                                                       | Faux     | **NTDS-DSA**                                                     |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**A-maître-NC**](a-hasmasterncs.md)                                                     | Faux     | **NTDS-DSA**                                                     |
| [**Contient-partiel-conplica-NC**](a-haspartialreplicancs.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**ID d’appel**](a-invocationid.md)                                                      | Faux     | **NTDS-DSA**                                                     |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Dernière-sauvegarde-restauration-heure**](a-lastbackuprestorationtime.md)                          | Faux     | **NTDS-DSA**                                                     |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Géré par**](a-managedby.md)                                                            | Faux     | **NTDS-DSA**                                                     |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Behavior-Version**](a-msds-behavior-version.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Fonctionnalité ms-DS-Enabled**](a-msds-enabledfeature.md)                                       | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-a-Domain-NC**](a-msds-hasdomainncs.md)                                          | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-full-Replica-NC**](a-msds-hasfullreplicancs.md)                               | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-instancié-NC**](a-msds-hasinstantiatedncs.md)                              | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-a-Master-NC**](a-msds-hasmasterncs.md)                                          | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isGC**](a-msds-isgc.md)                                                            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-isRODC**](a-msds-isrodc.md)                                                        | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-is-User-cachable-at-RODC**](a-msds-isusercachableatrodc.md)                        | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-jamais-Reveal-Group**](a-msds-neverrevealgroup.md)                                  | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-ReplicationEpoch**](a-msds-replicationepoch.md)                                    | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-retirée-REPL-NC-signatures**](a-msds-retiredreplncsignatures.md)                   | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-dévoilé-utilisateurs**](a-msds-revealedusers.md)                                         | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Reveal-OnDemand-Group**](a-msds-revealondemandgroup.md)                            | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-Paramètres**](a-msds-settings.md)                                                    | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**ms-DS-SiteName**](a-msds-sitename.md)                                                    | Faux     | **NTDS-DSA**                                                     |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresse réseau**](a-networkaddress.md)                                                  | Faux     | **NTDS-DSA**                                                     |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Notification-liste**](a-notificationlist.md)                                              | Faux     | [**Paramètres de l’Application**](c-applicationsettings.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                  |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Options**](a-options.md)                                                                 | Faux     | **NTDS-DSA**                                                     |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objet de stratégie de requête**](a-querypolicyobject.md)                                           | Faux     | **NTDS-DSA**                                                     |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Rapports**](a-directreports.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Retirée-REPL-DSA-signatures**](a-retiredrepldsasignatures.md)                            | Faux     | **NTDS-DSA**                                                     |
| [**Faisant**](a-revision.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Référence serveur**](a-serverreference.md)                                                | Faux     | **NTDS-DSA**                                                     |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                  |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                  |



## <a name="windows-server-2012-extended-rights"></a>Windows Server 2012 Droits étendus

Cette classe contient les droits étendus suivants pour Windows Server 2012 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Do-garbage collection**](r-do-garbage-collection.md)                       |
| [**Recalculer-hiérarchie**](r-recalculate-hierarchy.md)                       |
| [**Allocate-RID**](r-allocate-rids.md)                                       |
| [**Recalculer-sécurité-héritage**](r-recalculate-security-inheritance.md) |
| [**DS-Check-périmé-fantômes**](r-ds-check-stale-phantoms.md)                   |
| [**Actualiser-groupe-cache**](r-refresh-group-cache.md)                           |
| [**Recharger-SSL-certificat**](r-reload-ssl-certificate.md)                     |



## <a name="windows-server-2012-validated-writes"></a>Windows Server 2012 Écritures validées

Cette classe contient les écritures validées suivantes pour Windows Server 2012 :



| Nom commun                                                                    |
|--------------------------------------------------------------------------------|
| [**Validé-MS-DS-Behavior-Version**](r-validated-ms-ds-behavior-version.md) |



 

 





