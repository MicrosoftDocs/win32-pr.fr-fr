---
description: L’interface SSPI (Security Service Provider Interface) fournit une interface universelle et standard pour les applications distribuées sécurisées.
ms.assetid: c3cebb9d-9094-493f-96d3-763a0c282dfb
title: Fournisseurs de services de sécurité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2121940337d0f4e06c53981cf30f0125180c466
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413656"
---
# <a name="security-service-providers"></a>Fournisseurs de services de sécurité

L’interface SSPI (Security Service Provider Interface) fournit une interface universelle et standard pour les applications distribuées sécurisées. L’API graphique d’homologues offre aux applications un moyen de sécuriser les liens dans un graphique en spécifiant un fournisseur de services de sécurité (SSP), qui est une DLL qui implémente une interface SSPI. Une application spécifie un fournisseur de services partagés lors de la création d’un graphique à l’aide de [**PeerGraphCreate**](/windows/desktop/api/P2P/nf-p2p-peergraphcreate).

Pour plus d’informations sur la création de votre propre fournisseur de services partagés, consultez le lien de la documentation SSPI dans la liste des [liens de référence](graphing-reference-links.md)sur les graphiques.

## <a name="programming-considerations-for-implementing-an-ssp"></a>Considérations relatives à la programmation pour l’implémentation d’un SSP

Soyez prudent lors de l’appel à une application à partir d’un SSP. Les considérations suivantes s’appliquent aux rappels de fournisseur de services partagés :

-   Le retour des rappels ne doit pas prendre beaucoup de temps, car ils sont appelés pendant la négociation de la connexion. S’il faut trop de temps pour établir une connexion, la connexion peut être supprimée.
-   L’API de représentation graphique des homologues ajuste dynamiquement les valeurs de délai d’attente de connexion, en fonction de la charge réelle d’un système. La valeur du délai d’expiration le plus bas est de 20 secondes.
-   Pour éviter les situations de blocage potentielles, une application ne doit pas accéder à la base de données graphique des homologues à partir d’un rappel. Si une application requiert des informations de la base de données de graphiques, l’application peut mettre en cache les informations nécessaires, puis faire référence au cache à partir du rappel. La mise en cache peut également contribuer à réduire le temps de connexion.

Lors de l’appel des points d’entrée SSPI, l’infrastructure de représentation graphique des homologues requiert des valeurs spécifiques pour des paramètres spécifiques de cinq (5) fonctions. Vous ne pouvez pas modifier ces valeurs de paramètre fournies au fournisseur SSP et le SSP peut ignorer les valeurs des cinq paramètres ou les gérer correctement. La liste suivante identifie ces paramètres spécifiques et les valeurs requises :

-   [**AcquireCredentialsHandle**](graphing-reference-links.md)

    Spécifiez un (1) pour le paramètre *pvGetKeyArgument* . Spécifie la **valeur null** pour les paramètres *pszPrincipal*, *pvLogonID* et *pGetKeyFn* .

-   [**InitializeSecurityContext**](graphing-reference-links.md)

    Spécifiez les indicateurs suivants pour le paramètre *fContextReq* : ISC req-authentification mutuelle d’ISC req-confidentialité ISC req req intégrité de la séquence de demande ISC req req du flux ISC req **\_ \_ \_ \| \_ \_ \| \_ \_ \| \_ \_ \_ \| \_ \_ \| \_ \_ allouer \_** de la mémoire.

-   [**AcceptSecurityContext**](graphing-reference-links.md)

    Spécifiez les indicateurs suivants pour le paramètre *fContextReq* : **ASC \_ req \_ Mutual \_ auth \| ASC req \_ \_ Confidential \| ASC \_ req \_ intégrité \| ASC \_ req \_ Sequence \_ détecter \| ASC \_ req \_ Stream \| ASC \_ req \_ allouer \_** de la mémoire.

-   [**EncryptMessage**](graphing-reference-links.md)

    Spécifiez zéro (0) pour les paramètres *fQOP* et *MessageSeqNo* .

-   [**DecryptMessage**](graphing-reference-links.md)

    Spécifiez zéro (0) pour le paramètre *MessageSeqNo* et **null** pour le paramètre *pfQOP* .

Lors de l’appel de [**EncryptMessage**](graphing-reference-links.md), quatre mémoires tampons sont passées dans la structure **SecBufferDesc** . Le tableau suivant identifie l’ordre de transmission des mémoires tampons.

| Structure spécifique au fournisseur de services partagés         | Description                                                                                                                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_ \_ en-tête de flux SECBUFFER**  | Contient les données d’en-tête de sécurité. La taille de la mémoire tampon d’en-tête est obtenue en appelant [**QueryContextAttributes**](graphing-reference-links.md) et en spécifiant l’attribut de **\_ \_ \_ tailles de flux attr SECPKG** .  |
| **\_données SECBUFFER**            | Contient le message en texte brut à chiffrer.                                                                                                                                                                  |
| **Code de fin de \_ flux SECBUFFER \_** | Contient les données de code de fin de sécurité. La taille de la mémoire tampon d’en-tête est obtenue en appelant [**QueryContextAttributes**](graphing-reference-links.md) et en spécifiant l’attribut de **\_ \_ \_ tailles de flux attr SECPKG** . |
| **SECBUFFER \_ vide**           | Non initialisé. La taille de cette mémoire tampon est égale à zéro (0).                                                                                                                                                             |



 

Lors de l’appel de [**DecryptMessage**](graphing-reference-links.md), l’API de représentation graphique d’homologue passe exactement quatre structures **SecBuffer** . La première mémoire tampon est **SECBUFFER \_ Data** et contient un message chiffré. Les mémoires tampons restantes sont utilisées pour la sortie et sont de type **SECBUFFER \_ vide**.

Le SSP doit prendre en charge le chiffrement et le déchiffrement des tampons de données utilisateur avec des tailles de 16 Ko et plus dans un appel.

 

 



