---
title: classe ms-WMI-ObjectEncoding
description: Contient des données d’encodage pour une classe WMI ou un objet d’instance, ainsi que des informations supplémentaires concernant l’objet.
ms.assetid: 8f2830f0-c427-431e-bcd2-6d7f8951792a
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe ms-WMI-ObjectEncoding
- Schéma AD de la classe msWMI-ObjectEncoding
topic_type:
- apiref
api_name:
- ms-WMI-ObjectEncoding
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 791833306da64ff677f9c0d419ec0c6a97d0a688e11d1248e79ec9933052b2c4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440289"
---
# <a name="ms-wmi-objectencoding-class"></a>classe ms-WMI-ObjectEncoding

Contient des données d’encodage pour une classe WMI ou un objet d’instance, ainsi que des informations supplémentaires concernant l’objet.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | MS-WMI-ObjectEncoding                |
| LDAP-Display-Name | msWMI-ObjectEncoding                 |
| Mettre à jour le privilège  | Administrateur de domaine                 |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | 55dd81c9-c312-41f9-a84d-c6adbdf1e8e1 |



## <a name="implementations"></a>Implémentations

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.217                                                                       |
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



| Attribut                                                                   | Obligatoire | Dérivé de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom de l’extension**](a-extensionname.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs**](a-flags.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                     | True      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-WMI-classe**](a-mswmi-class.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-genre**](a-mswmi-genus.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ID**](a-mswmi-id.md)                                             | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags1**](a-mswmi-intflags1.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags2**](a-mswmi-intflags2.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags3**](a-mswmi-intflags3.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags4**](a-mswmi-intflags4.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-parm1**](a-mswmi-parm1.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm2**](a-mswmi-parm2.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm3**](a-mswmi-parm3.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm4**](a-mswmi-parm4.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ScopeGuid**](a-mswmi-scopeguid.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-TargetObject**](a-mswmi-targetobject.md)                         | True      | **MS-WMI-ObjectEncoding**       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | True      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | True      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                       | True      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Version de l’objet**](a-objectversion.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Rapports**](a-directreports.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.217                                                                       |
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



| Attribut                                                                   | Obligatoire | Dérivé de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom de l’extension**](a-extensionname.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs**](a-flags.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                     | True      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-WMI-classe**](a-mswmi-class.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-genre**](a-mswmi-genus.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ID**](a-mswmi-id.md)                                             | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags1**](a-mswmi-intflags1.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags2**](a-mswmi-intflags2.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags3**](a-mswmi-intflags3.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags4**](a-mswmi-intflags4.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-parm1**](a-mswmi-parm1.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm2**](a-mswmi-parm2.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm3**](a-mswmi-parm3.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm4**](a-mswmi-parm4.md)                                       | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ScopeGuid**](a-mswmi-scopeguid.md)                               | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-TargetObject**](a-mswmi-targetobject.md)                         | True      | **MS-WMI-ObjectEncoding**       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | True      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | True      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                       | True      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Version de l’objet**](a-objectversion.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Rapports**](a-directreports.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.217                                                                       |
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



| Attribut                                                                      | Obligatoire | Dérivé de                    |
|--------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom de l’extension**](a-extensionname.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs**](a-flags.md)                                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                        | True      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-WMI-classe**](a-mswmi-class.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-genre**](a-mswmi-genus.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ID**](a-mswmi-id.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags1**](a-mswmi-intflags1.md)                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags2**](a-mswmi-intflags2.md)                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags3**](a-mswmi-intflags3.md)                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags4**](a-mswmi-intflags4.md)                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-parm1**](a-mswmi-parm1.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm2**](a-mswmi-parm2.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm3**](a-mswmi-parm3.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm4**](a-mswmi-parm4.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ScopeGuid**](a-mswmi-scopeguid.md)                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-TargetObject**](a-mswmi-targetobject.md)                            | True      | **MS-WMI-ObjectEncoding**       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | True      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | True      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                          | True      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Version de l’objet**](a-objectversion.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Rapports**](a-directreports.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.217                                                                       |
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



| Attribut                                                                        | Obligatoire | Dérivé de                    |
|----------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom de l’extension**](a-extensionname.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs**](a-flags.md)                                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                          | True      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-recyclé**](a-isrecycled.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-WMI-classe**](a-mswmi-class.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-genre**](a-mswmi-genus.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ID**](a-mswmi-id.md)                                                  | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags1**](a-mswmi-intflags1.md)                                    | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags2**](a-mswmi-intflags2.md)                                    | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags3**](a-mswmi-intflags3.md)                                    | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags4**](a-mswmi-intflags4.md)                                    | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-parm1**](a-mswmi-parm1.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm2**](a-mswmi-parm2.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm3**](a-mswmi-parm3.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm4**](a-mswmi-parm4.md)                                            | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ScopeGuid**](a-mswmi-scopeguid.md)                                    | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-TargetObject**](a-mswmi-targetobject.md)                              | True      | **MS-WMI-ObjectEncoding**       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | True      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | True      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                            | True      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Version de l’objet**](a-objectversion.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Rapports**](a-directreports.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------|
| System-Only                 | False                                                                                        |
| Object-Category             | 1                                                                                            |
| Default-Object-catégorie     | \-                                                                                           |
| Governs-Id                  | 1.2.840.113556.1.5.217                                                                       |
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



| Attribut                                                                                    | Obligatoire | Dérivé de                    |
|----------------------------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Nom de l’extension**](a-extensionname.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs**](a-flags.md)                                                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                                      | True      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Est-recyclé**](a-isrecycled.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-TDO-Egress-BL**](a-msds-tdoegressbl.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**MS-WMI-classe**](a-mswmi-class.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-genre**](a-mswmi-genus.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ID**](a-mswmi-id.md)                                                              | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags1**](a-mswmi-intflags1.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags2**](a-mswmi-intflags2.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags3**](a-mswmi-intflags3.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-intFlags4**](a-mswmi-intflags4.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-parm1**](a-mswmi-parm1.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm2**](a-mswmi-parm2.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm3**](a-mswmi-parm3.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-Parm4**](a-mswmi-parm4.md)                                                        | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-ScopeGuid**](a-mswmi-scopeguid.md)                                                | True      | **MS-WMI-ObjectEncoding**       |
| [**MS-WMI-TargetObject**](a-mswmi-targetobject.md)                                          | True      | **MS-WMI-ObjectEncoding**       |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | True      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | False     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | True      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                                        | True      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Version de l’objet**](a-objectversion.md)                                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | False     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | False     | [**Retour au début**](c-top.md)<br/> |
| [**Rapports**](a-directreports.md)                                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | False     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | False     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | False     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                                                | False     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                                          | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                                      | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | False     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                                            | False     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                                              | False     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | False     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                                        | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | False     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                                              | False     | [**Retour au début**](c-top.md)<br/> |



 

 





