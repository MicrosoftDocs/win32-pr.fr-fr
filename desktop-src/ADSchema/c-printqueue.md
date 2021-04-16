---
title: Classe Print-Queue
description: Contient des informations sur une file d’attente à l’impression.
ms.assetid: 779eb37c-f94e-472a-9551-8a0f72fe0e2b
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe Print-Queue
- Schéma AD de la classe printQueue
topic_type:
- apiref
api_name:
- Print-Queue
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7995598603af4cab7b4b9d6f150e92964f0ee616
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "104479509"
---
# <a name="print-queue-class"></a>Classe Print-Queue

Contient des informations sur une file d’attente à l’impression.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | Print-Queue                          |
| LDAP-Display-Name | printQueue                           |
| Mettre à jour le privilège  | Tout le monde peut mettre à jour cet objet.       |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | bf967aa8-0de6-11d0-a285-00aa003049e2 |



## <a name="implementations"></a>Implémentations

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server

-   [Attributs](#windows-2000-server-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-2000-server-attributes"></a>Attributs du serveur Windows 2000

Cette classe contient les attributs suivants pour le serveur Windows 2000 :



| Attribut                                                                 | Obligatoire | Dérivé de                                                                             |
|---------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                               | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                   | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                            | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                         | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                               | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)     | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)              | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)              | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                     | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)   | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)      | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                       | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                            | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                             | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                 | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003"></a>Windows Server 2003

-   [Attributs](#windows-server-2003-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-attributes"></a>Attributs Windows Server 2003

Cette classe contient les attributs suivants pour Windows Server 2003 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                                 | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                              | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                           | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-paramètres**](a-msds-settings.md)                                   | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)       | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                       | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)     | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)        | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                         | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                              | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                               | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                   | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2

-   [Attributs](#windows-server-2003-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2003-r2-attributes"></a>Attributs Windows Server 2003 R2

Cette classe contient les attributs suivants pour Windows Server 2003 R2 :



| Attribut                                                                   | Obligatoire | Dérivé de                                                                             |
|-----------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                                 | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                              | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                           | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-paramètres**](a-msds-settings.md)                                   | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)       | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                       | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)     | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)        | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                         | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                              | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                               | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                   | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008"></a>Windows Server 2008

-   [Attributs](#windows-server-2008-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-attributes"></a>Attributs Windows Server 2008

Cette classe contient les attributs suivants pour Windows Server 2008 :



| Attribut                                                                      | Obligatoire | Dérivé de                                                                             |
|--------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                                    | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                      | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                                 | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                              | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-principal-name**](a-msds-principalname.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-paramètres**](a-msds-settings.md)                                      | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                       | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                                    | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)          | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                          | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)        | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)           | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                            | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                                 | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                                  | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                      | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2

-   [Attributs](#windows-server-2008-r2-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2008-r2-attributes"></a>Attributs Windows Server 2008 R2

Cette classe contient les attributs suivants pour Windows Server 2008 R2 :



| Attribut                                                                        | Obligatoire | Dérivé de                                                                             |
|----------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                                      | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                          | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-recyclé**](a-isrecycled.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                                   | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                                | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-principal-name**](a-msds-principalname.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-paramètres**](a-msds-settings.md)                                        | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                         | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                            | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)            | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                            | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)          | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                                  | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                           | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)             | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                             | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                              | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                                   | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                                    | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                        | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



## <a name="windows-server-2012"></a>Windows Server 2012

-   [Attributs](#windows-server-2012-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System-Only                 | Faux                                                                                                                                                                |
| Object-Category             | 1                                                                                                                                                                    |
| Default-Object-catégorie     | \-                                                                                                                                                                   |
| Governs-Id                  | 1.2.840.113556.1.5.23                                                                                                                                                |
| Valeur de masquage par défaut        | 0                                                                                                                                                                    |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/>                                                                                                                               |
| Sous-classe de                 | [**Point de connexion**](c-connectionpoint.md)<br/>                                                                                                             |
| Supérieurs possibles          | [**Domaine de**](c-domaindns.md)[**conteneur**](c-container.md)d' [**ordinateur**](c-computer.md)-[**unité d’organisation**](c-organizationalunit.md) DNS                   |
| Classes auxiliaires           | \-                                                                                                                                                                   |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                                                                                                                                                         |
| Descripteur de sécurité par défaut | D : (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW ;;;D A) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; SY) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; PO) (A ;; RPWPCRCCDCLCLORCWOWDSDDTSW;;; CO) (A ;; RPLCLORC;;; UA |
| System-Flags                | 0x00000010                                                                                                                                                           |



## <a name="windows-server-2012-attributes"></a>Attributs Windows Server 2012

Cette classe contient les attributs suivants pour Windows Server 2012 :



| Attribut                                                                                    | Obligatoire | Dérivé de                                                                             |
|----------------------------------------------------------------------------------------------|-----------|------------------------------------------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Admin-Display-Name**](a-admindisplayname.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-attributs**](a-allowedattributes.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de l’élément multimédia**](a-assetnumber.md)                                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Octets par minute**](a-bytesperminute.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom canonique**](a-canonicalname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom commun**](a-cn.md)                                                                  | Vrai      | [**Point de connexion**](c-connectionpoint.md)<br/> [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Priorité par défaut**](a-defaultpriority.md)                                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Description**](a-description.md)                                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet**](a-displayname.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom complet-imprimable**](a-displaynameprintable.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du pilote**](a-drivername.md)                                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du pilote**](a-driverversion.md)                                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**DSA-signature**](a-dsasignature.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom de l’extension**](a-extensionname.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Père**](a-flags.md)                                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Entrée de**](a-fromentry.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Computer-Reference-BL**](a-frscomputerreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FRS-Member-Reference-BL**](a-frsmemberreferencebl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Type d’instance**](a-instancetype.md)                                                      | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est supprimé**](a-isdeleted.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Is-Member-of-DL**](a-memberof.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-titulaire de privilège**](a-isprivilegeholder.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Est-recyclé**](a-isrecycled.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Mots clés**](a-keywords.md)                                                               | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Dernier-parent connu**](a-lastknownparent.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lieu**](a-location.md)                                                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Géré par**](a-managedby.md)                                                            | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**Objets managés**](a-managedobjects.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Masterisé-par**](a-masteredby.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Date et heure de modification**](a-modifytimestamp.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-PartitionSetLink**](a-mscom-partitionsetlink.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-COM-UserLink**](a-mscom-userlink.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-ComputerReferenceBL**](a-msdfsr-computerreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DFSR-MemberReferenceBL**](a-msdfsr-memberreferencebl.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-AuthenticatedTo-accountlist**](a-msds-authenticatedtoaccountlist.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-claim-shares-possibles-values-with-BL**](a-msds-claimsharespossiblevalueswithbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-fonctionnalité-BL**](a-msds-enabledfeaturebl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Host-service-account-BL**](a-msds-hostserviceaccountbl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-domain-pour**](a-msds-isdomainfor.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-Full-Replica-pour**](a-msds-isfullreplicafor.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-partiel-réplica-pour**](a-msds-ispartialreplicafor.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-est-Primary-Computer-for**](a-msds-isprimarycomputerfor.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-KrbTgt-Link-BL**](a-msds-krbtgtlinkbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dernier-connu-RDN**](a-msds-lastknownrdn.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effectif-suppression-heure**](a-msds-localeffectivedeletiontime.md)             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-local-effectif-temps de recyclage**](a-msds-localeffectiverecycletime.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Members-for-AZ-Role-BL**](a-msds-membersforazrolebl.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-members-of-Resource-Property-List-BL**](a-msds-membersofresourcepropertylistbl.md) | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-RO-Replica-Locations-BL**](a-msds-nc-ro-replica-locations-bl.md)                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-NC-type**](a-msds-nctype.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-non-membres-BL**](a-msds-nonmembersbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-objet-référence-BL**](a-msds-objectreferencebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-OIDToGroup-Link-BL**](a-msds-oidtogrouplinkbl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Role-BL**](a-msds-operationsforazrolebl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-Operations-for-AZ-Task-BL**](a-msds-operationsforaztaskbl.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-principal-name**](a-msds-principalname.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-PSO-appliqué**](a-msds-psoapplied.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-DSA**](a-msds-revealeddsas.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-dévoilé-List-BL**](a-msds-revealedlistbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-paramètres**](a-msds-settings.md)                                                    | Faux     | [**Point de connexion**](c-connectionpoint.md)<br/>                                 |
| [**ms-DS-tâches-for-AZ-Role-BL**](a-msds-tasksforazrolebl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-tâches-pour-AZ-Task-BL**](a-msds-tasksforaztaskbl.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-sortie-BL**](a-msds-tdoegressbl.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-TDO-entrée-BL**](a-msds-tdoingressbl.md)                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-DS-value-type-référence-BL**](a-msds-valuetypereferencebl.md)                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**ms-Exch-owner-BL**](a-ownerbl.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**msSFU-30-POSIX-Member-of**](a-mssfu30posixmemberof.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**netboot-SCP-BL**](a-netbootscpbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Non-sécurité-membre-BL**](a-nonsecuritymemberbl.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Catégorie d’objet**](a-objectcategory.md)                                                  | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Classe d’objet**](a-objectclass.md)                                                        | Vrai      | [**Retour au début**](c-top.md)<br/>                                                          |
| [**GUID de l’objet**](a-objectguid.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Version de l’objet**](a-objectversion.md)                                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Système d’exploitation**](a-operatingsystem.md)                                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-correctif logiciel**](a-operatingsystemhotfix.md)                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Système d’exploitation-Service-Pack**](a-operatingsystemservicepack.md)                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Version du système d’exploitation**](a-operatingsystemversion.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Partial-attribute-set**](a-partialattributeset.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Physical-location-Object**](a-physicallocationobject.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Nom du port**](a-portname.md)                                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Possible-inférieur**](a-possibleinferiors.md)                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Attributs d’impression**](a-printattributes.md)                                                | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-bin-Names**](a-printbinnames.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-assembler**](a-printcollate.md)                                                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Couleur d’impression**](a-printcolor.md)                                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-duplex-pris en charge**](a-printduplexsupported.md)                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Heure de fin d’impression**](a-printendtime.md)                                                     | Faux     | **File d’attente d’impression**                                                                          |
| [**Printer-nom**](a-printername.md)                                                        | Vrai      | **File d’attente d’impression**                                                                          |
| [**Nom du formulaire d’impression**](a-printformname.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-conserver-imprimé-tâches**](a-printkeepprintedjobs.md)                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Langue d’impression**](a-printlanguage.md)                                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-MAC-Address**](a-printmacaddress.md)                                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-nombre maximal de copies**](a-printmaxcopies.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Resolution-pris en charge**](a-printmaxresolutionsupported.md)                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-X-étendue**](a-printmaxxextent.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Max-Y-étendue**](a-printmaxyextent.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-prêt pour le média**](a-printmediaready.md)                                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Support-pris en charge**](a-printmediasupported.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-mémoire**](a-printmemory.md)                                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-min-X-étendue**](a-printminxextent.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-min-Y-étendue**](a-printminyextent.md)                                              | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-adresse réseau**](a-printnetworkaddress.md)                                       | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-notifier**](a-printnotify.md)                                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Numéro d’impression**](a-printnumberup.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-orientations-pris en charge**](a-printorientationssupported.md)                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Propriétaire de l’impression**](a-printowner.md)                                                          | Faux     | **File d’attente d’impression**                                                                          |
| [**Imprimer-pages par minute**](a-printpagesperminute.md)                                      | Faux     | **File d’attente d’impression**                                                                          |
| [**Taux d’impression**](a-printrate.md)                                                            | Faux     | **File d’attente d’impression**                                                                          |
| [**Unité de taux d’impression**](a-printrateunit.md)                                                   | Faux     | **File d’attente d’impression**                                                                          |
| [**Fichier séparateur d’impression**](a-printseparatorfile.md)                                         | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Share-Name**](a-printsharename.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Spouleur d’impression**](a-printspooling.md)                                                    | Faux     | **File d’attente d’impression**                                                                          |
| [**Impression-agrafage-pris en charge**](a-printstaplingsupported.md)                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**Print-Start-Time**](a-printstarttime.md)                                                 | Faux     | **File d’attente d’impression**                                                                          |
| [**État d’impression**](a-printstatus.md)                                                        | Faux     | **File d’attente d’impression**                                                                          |
| [**Priorité**](a-priority.md)                                                               | Faux     | **File d’attente d’impression**                                                                          |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Adresses proxy**](a-proxyaddresses.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**UNIQUE**](a-name.md)                                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Rapports**](a-directreports.md)                                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à partir de**](a-repsfrom.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Représentants-à**](a-repsto.md)                                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Faisant**](a-revision.md)                                                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom du serveur**](a-servername.md)                                                          | Vrai      | **File d’attente d’impression**                                                                          |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Short-nom-serveur**](a-shortservername.md)                                               | Vrai      | **File d’attente d’impression**                                                                          |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)                               | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Site-objet-BL**](a-siteobjectbl.md)                                                     | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Sous-Références**](a-subrefs.md)                                                                | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Indicateurs système**](a-systemflags.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Nom UNC**](a-uncname.md)                                                                | Vrai      | **File d’attente d’impression**                                                                          |
| [**USN-modifié**](a-usnchanged.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Créé par USN**](a-usncreated.md)                                                          | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-intersite**](a-usnintersite.md)                                                      | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                                  | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**USN-source**](a-usnsource.md)                                                            | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Numéro de version**](a-versionnumber.md)                                                    | Vrai      | **File d’attente d’impression**                                                                          |
| [**Chemin WBEM**](a-wbempath.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Objets bien connus**](a-wellknownobjects.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**En cas de modification**](a-whenchanged.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**Lors de la création**](a-whencreated.md)                                                        | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |
| [**WWW-page-autres**](a-url.md)                                                              | Faux     | [**Retour au début**](c-top.md)<br/>                                                          |



 

 





