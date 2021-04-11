---
title: Top (classe)
description: Classe de niveau supérieur à partir de laquelle toutes les classes sont dérivées.
ms.assetid: 025aff6c-1804-4141-accf-d50cfd50e90e
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe la plus haute
- Schéma AD de la classe la plus haute
topic_type:
- apiref
api_name:
- Top
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01cd6a72dfba6a80687081d503864c88fd1c5122
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104106732"
---
# <a name="top-class"></a>Top (classe)

Classe de niveau supérieur à partir de laquelle toutes les classes sont dérivées.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Haut                                  |
| LDAP-Display-Name | top                                  |
| Mettre à jour le privilège  | Administrateur de schéma                 |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | bf967ab7-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam-attributes)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributs](#windows-2000-server-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-2000-server-attributes"></a>Attributs du serveur Windows 2000

Cette classe contient les attributs suivants pour le serveur Windows 2000 :



| Attribut                                                                 | Obligatoire | Dérivé de |
|---------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                           | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                         | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)      | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                    | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md) | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)             | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                 | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                               | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                            | Faux     | **Top**      |
| [**Description**](a-description.md)                                      | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                     | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                  | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                   | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)               | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                 | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                  | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                         | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                   | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                         | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                        | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                            | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                               | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                       | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                            | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)    | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                   | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                  | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                               | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                     | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                       | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                 | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)               | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md) | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                    | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                         | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                        | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                               | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                     | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                        | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                           | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                               | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                            | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                        | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                        | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)            | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                  | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                             | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                     | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                       | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                       | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                   | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                         | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                           | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                          | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                     | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                     | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                    | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                           | Faux     | **Top**      |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-attributes"></a>Attributs Windows Server 2003

Cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                   | Obligatoire | Dérivé de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                 | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | **Top**      |
| [**Description**](a-description.md)                                        | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                       | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                    | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | **Top**      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | **Top**      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | **Top**      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | **Top**      |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | **Top**      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | **Top**      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                       | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                          | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                              | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                           | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | **Top**      |



## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)



| Entrée | Valeur |
|-----------------------------|------------------------------------------|
| System-Only                 | Vrai                                     |
| Object-Category             | 2                                        |
| Default-Object-catégorie     | \-                                       |
| Governs-Id                  | 2.5.6.0                                  |
| Valeur de masquage par défaut        | 1                                        |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>   |
| Sous-classe de                 | **Top**<br/>                       |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md) |
| Classes auxiliaires           | \-                                       |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                             |
| Descripteur de sécurité par défaut | D:S:                                     |
| System-Flags                | 0x00000010                               |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                   | Obligatoire | Dérivé de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                 | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | **Top**      |
| [**Description**](a-description.md)                                        | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                       | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | **Top**      |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | **Top**      |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                       | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                              | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                           | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | **Top**      |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2003-r2-attributes"></a>Attributs Windows Server 2003 R2

Cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                   | Obligatoire | Dérivé de |
|-----------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                 | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | **Top**      |
| [**Description**](a-description.md)                                        | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                       | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                    | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Faux     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | **Top**      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | **Top**      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | **Top**      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | **Top**      |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | **Top**      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | **Top**      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                       | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                          | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                              | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                           | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | **Top**      |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-attributes"></a>Attributs Windows Server 2008

Cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                      | Obligatoire | Dérivé de |
|--------------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                                | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                              | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                      | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                    | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                                 | Faux     | **Top**      |
| [**Description**](a-description.md)                                           | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                          | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                        | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                      | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                       | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                              | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                        | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                              | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                    | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                            | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | Faux     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Faux     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Faux     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Faux     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | Faux     | **Top**      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Faux     | **Top**      |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | Faux     | **Top**      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | Faux     | **Top**      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | Faux     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | Faux     | **Top**      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | Faux     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Faux     | **Top**      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | Faux     | **Top**      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | Faux     | **Top**      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Faux     | **Top**      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | Faux     | **Top**      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Faux     | **Top**      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | Faux     | **Top**      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | Faux     | **Top**      |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Faux     | **Top**      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Faux     | **Top**      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | Faux     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                          | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                            | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                      | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                          | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                             | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                    | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                                 | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                                  | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                          | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                            | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                            | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                        | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                              | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                                | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                               | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                          | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                          | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                                | Faux     | **Top**      |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2008-r2-attributes"></a>Attributs Windows Server 2008 R2

Cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de |
|----------------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                      | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | **Top**      |
| [**Description**](a-description.md)                                             | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                            | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                         | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | **Top**      |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | **Top**      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | **Top**      |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | **Top**      |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | **Top**      |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | **Top**      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | **Top**      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | **Top**      |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | **Top**      |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | **Top**      |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | **Top**      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | **Top**      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | **Top**      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | **Top**      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | **Top**      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | **Top**      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | **Top**      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | **Top**      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | **Top**      |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | **Top**      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | **Top**      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                            | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                               | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                                   | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                                | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | **Top**      |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | Vrai                                                                                         |
| Object-Category             | 2                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 2.5.6.0                                                                                      |
| Valeur de masquage par défaut        | 1                                                                                            |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                       |
| Sous-classe de                 | **Top**<br/>                                                                           |
| Supérieurs possibles          | [**Perdu-et-trouvé**](c-lostandfound.md)                                                     |
| Classes auxiliaires           | \-                                                                                           |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                 |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                   |



## <a name="windows-server-2012-attributes"></a>Attributs Windows Server 2012

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de |
|----------------------------------------------------------------------------------------------|-----------|--------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | **Top**      |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | **Top**      |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | **Top**      |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | **Top**      |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | **Top**      |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | **Top**      |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | **Top**      |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | **Top**      |
| [**Nom commun**](a-cn.md)                                                                  | Faux     | **Top**      |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | **Top**      |
| [**Description**](a-description.md)                                                         | Faux     | **Top**      |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | **Top**      |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | **Top**      |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | **Top**      |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | **Top**      |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | **Top**      |
| [**Père**](a-flags.md)                                                                     | Faux     | **Top**      |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | **Top**      |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | **Top**      |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | **Top**      |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | **Top**      |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | **Top**      |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | **Top**      |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | **Top**      |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | **Top**      |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | **Top**      |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | **Top**      |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | **Top**      |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | **Top**      |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | **Top**      |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | **Top**      |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | **Top**      |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | **Top**      |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | **Top**      |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | **Top**      |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | **Top**      |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | **Top**      |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | **Top**      |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | **Top**      |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | **Top**      |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | **Top**      |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | **Top**      |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | **Top**      |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | **Top**      |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | **Top**      |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | **Top**      |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | **Top**      |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | **Top**      |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | **Top**      |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | **Top**      |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | **Top**      |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | **Top**      |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | **Top**      |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | **Top**      |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | **Top**      |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | **Top**      |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | **Top**      |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | **Top**      |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | **Top**      |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | **Top**      |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | **Top**      |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | **Top**      |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | **Top**      |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | **Top**      |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | **Top**      |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | **Top**      |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | **Top**      |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | **Top**      |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | **Top**      |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | **Top**      |
| [**ms-DS-TDO-sortie-BL**](a-msds-tdoegressbl.md)                                            | Faux     | **Top**      |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | **Top**      |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | **Top**      |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | **Top**      |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | **Top**      |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | **Top**      |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | **Top**      |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | **Top**      |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | **Top**      |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | **Top**      |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | **Top**      |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | **Top**      |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | **Top**      |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | **Top**      |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | **Top**      |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | **Top**      |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | **Top**      |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | **Top**      |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | **Top**      |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | **Top**      |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | **Top**      |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | **Top**      |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | **Top**      |
| [**Rapports**](a-directreports.md)                                                           | Faux     | **Top**      |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | **Top**      |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | **Top**      |
| [**Faisant**](a-revision.md)                                                               | Faux     | **Top**      |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | **Top**      |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | **Top**      |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | **Top**      |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | **Top**      |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | **Top**      |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | **Top**      |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | **Top**      |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | **Top**      |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | **Top**      |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | **Top**      |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | **Top**      |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | **Top**      |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | **Top**      |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | **Top**      |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | **Top**      |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | **Top**      |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | **Top**      |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | **Top**      |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | **Top**      |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | **Top**      |



 

 





