---
description: Le champ de chiffrement est grand et croissant.
ms.assetid: ec50d6f1-999d-4ce9-85b4-816afb17550e
title: Types de fournisseur de chiffrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5aaeee585ff9c11e2a20a201f541f3cd147aef6e9b50c37d60156e75a1b9fd94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876209"
---
# <a name="cryptographic-provider-types"></a>Types de fournisseur de chiffrement

Le champ de [*chiffrement*](../secgloss/c-gly.md) est grand et croissant. Il existe de nombreux formats et protocoles de données standard différents. Ils sont généralement organisés en groupes ou en familles, chacun ayant son propre ensemble de formats de données et la manière de faire des choses. Même si deux familles utilisent le même algorithme (par exemple, le [*chiffrement par blocs*](../secgloss/b-gly.md) [*RC2*](../secgloss/r-gly.md) ), elles utilisent souvent des schémas de [*remplissage*](../secgloss/p-gly.md) différents, des [*longueurs de clé*](../secgloss/k-gly.md)et différents modes par défaut. CryptoAPI est conçu de sorte qu’un type de fournisseur CSP représente une famille particulière.

Quand une application se connecte à un fournisseur de services de chiffrement d’un type particulier, chacune des fonctions CryptoAPI fonctionnera par défaut de la manière prescrite par la famille qui correspond à ce type de CSP. Le choix d’une application pour le type de fournisseur spécifie les éléments suivants :



| Élément                                                                                                                                | Description                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*Algorithme d’échange de clés*](../secgloss/k-gly.md)                | Chaque type de fournisseur spécifie un et un seul algorithme d’échange de clés. Chaque CSP d’un type particulier doit implémenter cet algorithme. Les applications spécifient l’algorithme d’échange de clés à utiliser en sélectionnant un CSP du type de fournisseur approprié.                                                        |
| [*Algorithme de signature numérique*](../secgloss/d-gly.md) | Chaque type de fournisseur spécifie un et un seul algorithme de signature numérique. Chaque CSP d’un type particulier doit implémenter cet algorithme. Les applications spécifient l’algorithme de signature numérique à utiliser en sélectionnant un CSP du type de fournisseur approprié.                                              |
| Formats BLOB de clé                                                                                                                    | Le type fourni détermine le format de l' [*objet blob de clé*](../secgloss/k-gly.md) utilisé pour exporter des clés à partir du [*CSP*](../secgloss/c-gly.md) et pour importer des clés dans un CSP. |
| Format de signature numérique                                                                                                            | Le type de fournisseur détermine le format de signature numérique. Cela garantit qu’une signature produite par un CSP d’un type de fournisseur donné peut être vérifiée par n’importe quel CSP du même type de fournisseur.                                                                                                              |
| Schéma de dérivation de clé de session                                                                                                       | Le type de fournisseur détermine la méthode utilisée pour dériver une [*clé de session*](../secgloss/s-gly.md) d’un [*hachage*](../secgloss/h-gly.md).                                                                                   |
| [*Longueur de clé*](../secgloss/k-gly.md)                                                    | Certains types de fournisseurs spécifient la longueur des [*paires de clés publiques/privées*](../secgloss/p-gly.md) et les clés de session.                                                                                                               |
| Modes par défaut                                                                                                                       | Le type de fournisseur spécifie souvent des modes par défaut pour diverses options, telles que le [*mode*](../secgloss/c-gly.md) de chiffrement par bloc de chiffrement ou la méthode de [*remplissage*](../secgloss/p-gly.md) de chiffrement par bloc.          |



 

Certaines applications avancées peuvent se connecter à plusieurs CSP à la fois, mais la plupart des applications n’utilisent généralement qu’un seul CSP.

Il existe actuellement un certain nombre de types de fournisseurs prédéfinis. Les sections suivantes fournissent des informations sur les types de fournisseurs suivants :

-   [PROUVER \_ RSA \_ Full](prov-rsa-full.md)
-   [\_RSA \_ AES Prov.](prov-rsa-aes.md)
-   [PROUVER \_ RSA \_ SIG](prov-rsa-sig.md)
-   [PROUVER \_ RSA \_ Schannel](prov-rsa-schannel.md)
-   [DSS PROVen \_](prov-dss.md)
-   [PROVen \_ DSS \_](prov-dss-dh.md)
-   [PROUVER \_ DH \_ Schannel](prov-dh-schannel.md)
-   [\_Fortezza-Fortezza](prov-fortezza.md)
-   [PROUVER \_ MS \_ Exchange](prov-ms-exchange.md)
-   [SSL PROV. \_](prov-ssl.md)

Même si certains types de CSP peuvent être partiellement compatibles avec d’autres, au moins deux applications qui doivent [*échanger des clés*](../secgloss/e-gly.md) et des messages chiffrés doivent utiliser des fournisseurs de services de chiffrement du même type.

Un enregistreur CSP personnalisé peut définir un nouveau type de fournisseur. Toutefois, le rédacteur CSP est ensuite chargé de distribuer le nouveau type de fournisseur aux auteurs des applications qui l’utilisent. Pour plus d’informations sur l’écriture de [fournisseurs de services de chiffrement personnalisés, consultez Cryptographic Service Providers](cryptographic-service-providers.md).

 

 
