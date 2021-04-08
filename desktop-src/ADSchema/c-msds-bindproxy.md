---
title: classe ms-DS-bind-proxy
description: Classe auxiliaire pour représenter un proxy de liaison dans AD/AM.
ms.assetid: de837926-9d40-41f6-8c56-c4e436fd66b6
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe ms-DS-bind-proxy
- Schéma AD de la classe msDS-BindProxy
topic_type:
- apiref
api_name:
- ms-DS-Bind-Proxy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db4fbb48080c83c3ea82b72c598e2a5a06037562
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744100"
---
# <a name="ms-ds-bind-proxy-class"></a>classe ms-DS-bind-proxy

Classe auxiliaire pour représenter un proxy de liaison dans AD/AM. Le proxy de liaison fait référence à un principal de sécurité Windows via son attribut objectSid. Lorsqu’un utilisateur effectue une liaison simple avec un objet de proxy de liaison, la liaison est redirigée vers le principal Windows correspondant.



| Entrée | Valeur |
|-------------------|--------------------------------------|
| CN                | ms-DS-bind-proxy                     |
| LDAP-Display-Name | msDS-BindProxy                       |
| Mettre à jour le privilège  | \-                                   |
| Fréquence des mises à jour  | \-                                   |
| Schema-ID-GUID    | 717532ab-66e9-684d-a62b-8af1e3985e2f |



## <a name="implementations"></a>Implémentations

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)



| Entrée | Valeur |
|-----------------------------|---------------------------------|
| System-Only                 | Faux                           |
| Object-Category             | 3                               |
| Default-Object-catégorie     | \-                              |
| Governs-Id                  | 1.2.840.113556.1.5.245          |
| Valeur de masquage par défaut        | 1                               |
| RDN-att-ID                  | \-                              |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/> |
| Supérieurs possibles          | \-                              |
| Classes auxiliaires           | \-                              |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                    |
| Descripteur de sécurité par défaut | \-                              |
| System-Flags                | 0x00000010                      |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                   | Obligatoire | Dérivé de                    |
|-----------------------------------------------------------------------------|-----------|---------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/> |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-principal-name**](a-msds-principalname.md)                        | Faux     | **ms-DS-bind-proxy**            |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/> |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/> |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/> |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**SID de l’objet**](a-objectsid.md)                                           | Vrai      | **ms-DS-bind-proxy**            |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/> |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/> |



 

 





