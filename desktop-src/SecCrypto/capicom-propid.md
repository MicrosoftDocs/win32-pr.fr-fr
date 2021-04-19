---
description: Définit les identificateurs de propriété CAPICOM.
ms.assetid: faf10018-3ed8-4de6-9838-c553626f6dd7
title: Énumération CAPICOM_PROPID (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROPID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: d817262b869ef694c2cf9ff5b1e577840c3168a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106532219"
---
# <a name="capicom_propid-enumeration"></a>CAPICOM \_ propId, énumération

L’énumération **\_ propid propid** définit les identificateurs de propriété CAPICOM.

## <a name="members"></a>Membres



| Membre                                                 | Description                                                                                                                                                                                                                                                                                | Valeur      |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **\_propid propid \_ inconnu**                           | Le type de la propriété n’est pas connu.<br/>                                                                                                                                                                                                                                          | 0          |
| **CAPICOM-handle de clé de l’ID de la \_ \_ \_ preuve \_**                 | Handle d’un conteneur de clé dans un [*fournisseur de services de chiffrement*](../secgloss/c-gly.md) (CSP).<br/>                                                                                        | 1          |
| **CAPICOM- \_ \_ \_ informations sur la clé \_ de l’ID de la clé**                   | Informations sur un conteneur de clé dans un fournisseur de services de chiffrement.<br/>                                                                                                                                                                                                                                 | 2          |
| **\_ \_ Hachage SHA1 du CAPICOM \_**                        | Objet de hachage SHA1.<br/>                                                                                                                                                                                                                                                             | 3          |
| **\_Prop. ID de \_ hachage de CAPICOM \_**                        | Propriétés d’un objet de hachage.<br/>                                                                                                                                                                                                                                                | 3          |
| **\_ \_ Hachage MD5 du CAPICOM \_**                         | Objet de hachage MD5.<br/>                                                                                                                                                                                                                                                             | 4          |
| **contexte de clé de l’ID de la \_ \_ clé CAPICOM \_**                      | [*Contexte*](../secgloss/c-gly.md)de clé.<br/>                                                                                                                                                                                                | 5          |
| **spécification de clé de CAPICOM \_ propid \_ \_**                         | Spécifications pour une clé.<br/>                                                                                                                                                                                                                                                   | 6          |
| **\_Ie30 propid propid \_ \_ réservé**                    | Informations indiquant si l’objet est réservé dans Internet Explorer 3,0.<br/>                                                                                                                                                                                                      | 7          |
| **CAPICOM PUBKEY de \_ \_ \_ hachage \_ réservé**            | Informations indiquant si le hachage de la clé publique est réservé.<br/>                                                                                                                                                                                                               | 8          |
| **\_utilisation de ENHKEY propid \_ propid \_**                     | [*Utilisation améliorée*](../secgloss/e-gly.md) de la clé (EKU).<br/>                                                                                                                                                              | 9          |
| **\_ \_ utilisation CTL de CAPICOM propid \_**                        | Utilisation d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL).<br/>                                                                                                                                             | 9          |
| **\_ \_ \_ emplacement de mise à jour suivant \_ de CAPICOM propid**            | Emplacement de la prochaine mise à jour de la [*liste de révocation de certificats*](../secgloss/c-gly.md) (CRL).<br/>                                                                                               | 10         |
| **\_ \_ nom convivial de l’propid \_ CAPICOM**                    | Nom explicite.<br/>                                                                                                                                                                                                                                                          | 11         |
| **\_fichier baproper propid \_ pvk \_**                         | Fichier qui contient une clé privée.<br/>                                                                                                                                                                                                                                             | 12         |
| **Description de l' \_ propid \_ CAPICOM**                       | Description explicite.<br/>                                                                                                                                                                                                                                                   | 13         |
| **\_ \_ État d’accès à CAPICOM \_ propid**                     | État de l’accès.<br/>                                                                                                                                                                                                                                                        | 14         |
| **hachage de la \_ signature propid de CAPICOM \_ \_**                   | Hachage de la signature.<br/>                                                                                                                                                                                                                                                        | 15         |
| **\_ \_ données de carte à puce \_ de CAPICOM propid \_**                 | Données de carte à puce.<br/>                                                                                                                                                                                                                                                                | 16         |
| **CAPICOM \_ ID prop \_ EFS**                               | Un [*système de fichiers EFS*](../secgloss/e-gly.md) (EFS).<br/>                                                                                                                                                  | 17         |
| **informations de l' \_ ID de l’propid \_ \_**                    | Données créées à l’aide des protocoles et algorithmes de chiffrement détenus par le [*National Institute of Standards and Technology*](../secgloss/n-gly.md) (NIST).<br/> | 18         |
| **\_propid propid \_ Archivé**                          | Informations indiquant si l’objet est archivé.<br/>                                                                                                                                                                                                                               | 19         |
| **identificateur de clé de l’ID de la \_ \_ clé CAPICOM \_**                   | Identificateur de clé.<br/>                                                                                                                                                                                                                                                               | 20         |
| **\_ \_ inscription automatique de CAPICOM propid \_**                      | Informations d’inscription automatique pour un certificat.<br/>                                                                                                                                                                                                                                  | 21         |
| **\_ \_ PUBKEY \_ ALG- \_ parase propid**                 | Paramètres d’un algorithme de clé publique.<br/>                                                                                                                                                                                                                                          | 22         |
| **les points de \_ \_ distribution du \_ CERT \_ de \_ CAPICOM**         | Informations utilisées pour mettre à jour les certificats croisés dynamiques.<br/>                                                                                                                                                                                                                          | 23         |
| **\_Hachage MD5 de la \_ \_ \_ clé publique \_ \_ de l’émetteur du propid-CAPICOM**    | Hachage MD5 de la clé publique de l’émetteur.<br/>                                                                                                                                                                                                                                        | 24         |
| **\_Hachage MD5 de la \_ \_ clé publique du sujet \_ \_ de CAPICOM \_**   | Hachage MD5 de la clé publique du sujet.<br/>                                                                                                                                                                                                                                       | 25         |
| **inscription à l' \_ ID d' \_ inscription CAPICOM**                        | Informations sur l’inscription du certificat.<br/>                                                                                                                                                                                                                                 | 26         |
| **horodatage de la date d’affectation CAPICOM \_ \_ \_**                       | Marqueur de date.<br/>                                                                                                                                                                                                                                                                   | 27         |
| **\_ \_ \_ \_ Hachage MD5 du numéro de série \_ de l’émetteur \_ CAPICOM** | Hachage MD5 du numéro de série de l’émetteur.<br/>                                                                                                                                                                                                                                     | 28         |
| **\_ \_ \_ Hachage MD5 du nom d’objet \_ de l’ID de l’objet CAPICOM \_**          | Hachage MD5 du nom du sujet.<br/>                                                                                                                                                                                                                                             | 29         |
| **\_ \_ informations d’erreur étendues de l’propid de \_ CAPICOM \_**             | Informations étendues sur une erreur.<br/>                                                                                                                                                                                                                                            | 30         |
| **Renouvellement de l’propid d’un CAPICOM \_ \_**                           | Informations sur le renouvellement d’une [*autorité de certification*](../secgloss/c-gly.md).<br/>                                                                                                                     | 64         |
| **hachage de la \_ \_ clé archivée de l’ID de la \_ clé \_ CAPICOM**               | Hachage archivé d’une clé.<br/>                                                                                                                                                                                                                                                      | 65         |
| **Réservation d’une \_ propid d' \_ abord pour \_ CAPICOM**                   | Informations sur la première réservation.<br/>                                                                                                                                                                                                                                        | 66         |
| **Réservation de l' \_ ID de la \_ dernière \_ réservation CAPICOM**                    | Informations sur la réservation la plus récente.<br/>                                                                                                                                                                                                                                  | 0x00007FFF |
| **CAPICOM d’un \_ \_ premier \_ utilisateur**                       | Informations sur le premier utilisateur.<br/>                                                                                                                                                                                                                                               | 0x00008000 |
| **CAPICOM \_ propr propid \_ dernier \_ utilisateur**                        | Informations sur l’utilisateur le plus récent.<br/>                                                                                                                                                                                                                                         | 0x0000FFFF |



## <a name="remarks"></a>Notes

Cette énumération est utilisée par les propriétés CAPICOM suivantes :

-   [**ExtendedProperty. PropID**](extendedproperty-propid.md)
-   [**ExtendedProperties. Remove**](extendedproperties-remove.md)

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|----------------------------|--------------------------------------------------------------------------------------|
| Composant redistribuable<br/> | CAPICOM 2,0 ou version ultérieure sur Windows Server 2003 et Windows XP<br/>                |
| En-tête<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
