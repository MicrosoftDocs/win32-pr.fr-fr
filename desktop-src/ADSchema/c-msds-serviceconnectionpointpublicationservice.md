---
title: ms-DS-Service-Connection-point-publication-service (classe)
description: Stocke les options de configuration du service de publication de point de connexion de service dans ADAM.
ms.assetid: 30b4df70-a03b-4d42-b200-75bfa6cf8273
ms.tgt_platform: multiple
keywords:
- Schéma AD de la classe de service ms-DS-Service-Connection-point-publication-service
- Schéma AD de la classe msDS-ServiceConnectionPointPublicationService
topic_type:
- apiref
api_name:
- ms-DS-Service-Connection-Point-Publication-Service
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13b458a5d66d8d6fd90a58519ce57de03f625087be4123f2e51ca8c09534ed96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879839"
---
# <a name="ms-ds-service-connection-point-publication-service-class"></a>ms-DS-Service-Connection-point-publication-service (classe)

Stocke les options de configuration du service de publication de point de connexion de service dans ADAM.



| Entrée | Valeur |
|-------------------|----------------------------------------------------|
| CN                | ms-DS-Service-Connection-point-publication-service |
| LDAP-Display-Name | msDS-ServiceConnectionPointPublicationService      |
| Mettre à jour le privilège  | \-                                                 |
| Fréquence des mises à jour  | \-                                                 |
| Schema-ID-GUID    | d33f5da6-b009-7e48-8268-b2305529e933               |



## <a name="implementations"></a>Implémentations

-   [**ADAM**](#adam-attributes)

## <a name="adam"></a>ADAM

-   [Attributs](#adam-attributes)



| Entrée | Valeur |
|-----------------------------|----------------------------------------|
| System-Only                 | Vrai                                   |
| Object-Category             | 1                                      |
| Default-Object-catégorie     | \-                                     |
| Governs-Id                  | 1.2.840.113556.1.5.247                 |
| Valeur de masquage par défaut        | 1                                      |
| RDN-att-ID                  | [**Nom commun**](a-cn.md)<br/> |
| Sous-classe de                 | [**Retour au début**](c-top.md)<br/>        |
| Supérieurs possibles          | [**NTDS-service**](c-ntdsservice.md)  |
| Classes auxiliaires           | \-                                     |
| Descripteur de sécurité NT      | O :BAG : BAD : S :                           |
| Descripteur de sécurité par défaut | D:S:                                   |
| System-Flags                | 0x00000000                             |



## <a name="adam-attributes"></a>Attributs ADAM

Cette classe contient les attributs suivants pour ADAM :



| Attribut                                                                   | Obligatoire | Dérivé de                                           |
|-----------------------------------------------------------------------------|-----------|--------------------------------------------------------|
| [**Administrateur-Description**](a-admindescription.md)                             | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Admin-Display-Name**](a-admindisplayname.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Allowed-attributs**](a-allowedattributes.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Autorisé-attributs-effectif**](a-allowedattributeseffective.md)        | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Allowed-classes enfants**](a-allowedchildclasses.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Allowed-classes enfants-effectif**](a-allowedchildclasseseffective.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Tête de pont-serveur-liste-BL**](a-bridgeheadserverlistbl.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Nom canonique**](a-canonicalname.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Nom commun**](a-cn.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Date et heure de création**](a-createtimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Description**](a-description.md)                                        | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Nom complet**](a-displayname.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**DSA-signature**](a-dsasignature.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**DS-Core-propagation-données**](a-dscorepropagationdata.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Activé**](a-enabled.md)                                                | Faux     | **ms-DS-Service-Connection-point-publication-service** |
| [**Entrée de**](a-fromentry.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**FSMO-Role-owner**](a-fsmoroleowner.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Type d’instance**](a-instancetype.md)                                     | Vrai      | [**Retour au début**](c-top.md)<br/>                        |
| [**Is-Critical-System-Object**](a-iscriticalsystemobject.md)               | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Est supprimé**](a-isdeleted.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Is-Member-of-DL**](a-memberof.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Mot**](a-keywords.md)                                              | Faux     | **ms-DS-Service-Connection-point-publication-service** |
| [**Dernier-parent connu**](a-lastknownparent.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Objets managés**](a-managedobjects.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Masterisé-par**](a-masteredby.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Date et heure de modification**](a-modifytimestamp.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-approx-immed-subordonnés**](a-msds-approx-immed-subordinates.md) | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-enfant-nombre**](a-ms-ds-consistencychildcount.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**MS-DS-Consistency-Guid**](a-ms-ds-consistencyguid.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-Disable-for-instances**](a-msds-disableforinstances.md)           | Faux     | **ms-DS-Service-Connection-point-publication-service** |
| [**ms-DS-Disable-for-instances-BL**](a-msds-disableforinstancesbl.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-masterisé-by**](a-msds-masteredby.md)                              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-NC REPL-curseurs**](a-msds-ncreplcursors.md)                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-CN-REPL-trafic entrant-voisins**](a-msds-ncreplinboundneighbors.md)    | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-CN-REPL-sortant-voisins**](a-msds-ncreploutboundneighbors.md)  | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-REPL-attribute-méta-données**](a-msds-replattributemetadata.md)      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-REPL-value-Meta-Data**](a-msds-replvaluemetadata.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**ms-DS-SCP-Container**](a-msds-scpcontainer.md)                          | Faux     | **ms-DS-Service-Connection-point-publication-service** |
| [**ms-DS-service-account-BL**](a-msds-serviceaccountbl.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Descripteur de sécurité NT**](a-ntsecuritydescriptor.md)                    | Vrai      | [**Retour au début**](c-top.md)<br/>                        |
| [**Obj-Dist-Name**](a-distinguishedname.md)                                | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Catégorie d’objet**](a-objectcategory.md)                                 | Vrai      | [**Retour au début**](c-top.md)<br/>                        |
| [**Classe d’objet**](a-objectclass.md)                                       | Vrai      | [**Retour au début**](c-top.md)<br/>                        |
| [**GUID de l’objet**](a-objectguid.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Version de l’objet**](a-objectversion.md)                                   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Autres objets bien connus**](a-otherwellknownobjects.md)                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Partial-attribute-suppression-liste**](a-partialattributedeletionlist.md)   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Partial-attribute-set**](a-partialattributeset.md)                      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Possible-inférieur**](a-possibleinferiors.md)                           | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Proxyd-Object-Name**](a-proxiedobjectname.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Adresses proxy**](a-proxyaddresses.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Requête-stratégie-BL**](a-querypolicybl.md)                                  | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**UNIQUE**](a-name.md)                                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**REPL-Property-Meta-Data**](a-replpropertymetadata.md)                   | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**REPL-UpToDate-Vector**](a-repluptodatevector.md)                        | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Représentants-à partir de**](a-repsfrom.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Représentants-à**](a-repsto.md)                                                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Faisant**](a-revision.md)                                              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**SD-droits-effectifs**](a-sdrightseffective.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Serveur-référence-BL**](a-serverreferencebl.md)                          | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Afficher dans Advanced-View uniquement**](a-showinadvancedviewonly.md)              | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Site-objet-BL**](a-siteobjectbl.md)                                    | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Structural-Object-Class**](a-structuralobjectclass.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Sous-Références**](a-subrefs.md)                                               | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**SubSchemaSubEntry**](a-subschemasubentry.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Indicateurs système**](a-systemflags.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**USN-modifié**](a-usnchanged.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Créé par USN**](a-usncreated.md)                                         | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**USN-DSA-Last-obj-supprimé**](a-usndsalastobjremoved.md)                  | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**USN-intersite**](a-usnintersite.md)                                     | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**USN-Last-obj-REM**](a-usnlastobjrem.md)                                 | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**USN-source**](a-usnsource.md)                                           | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Chemin WBEM**](a-wbempath.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Objets bien connus**](a-wellknownobjects.md)                            | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**En cas de modification**](a-whenchanged.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**Lors de la création**](a-whencreated.md)                                       | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**WWW-page d’hébergement**](a-wwwhomepage.md)                                      | Faux     | [**Retour au début**](c-top.md)<br/>                        |
| [**WWW-page-autres**](a-url.md)                                             | Faux     | [**Retour au début**](c-top.md)<br/>                        |



 

 





